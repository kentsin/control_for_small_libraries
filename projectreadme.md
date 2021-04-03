---
title: Terms control for small libraries
---

# Data format

All data format supported by eleventy can be used. I find the [YAML](https://Fyaml.org) format best suited for librarians.  

# Chinese

By default, chinese matching use pinyin. 

# Fuzzy matching

   Fuzzy matching do not use Levenshtein-Demerau model, instead it adapt MichaelDay's method point to this [stackeroverflow post](https://stackoverflow.com/questions/23305000/javascript-fuzzy-search-that-makes-sense)
   
       Try this one: [subtexteditor.github.io/fuzzysearch.js](http://subtexteditor.github.io/fuzzysearch.js/) – michaelday Jan 19 '15 at 21:00
1
       @michaelday That doesn't take typos into account. In the demo, typing krole doesn't return Final Fantasy V: Krile, though I would like it to. It requires all characters in the query to be present in the same order in the result, which is pretty short-sighted. It seems the only way to have good fuzzy search is to have a database of common typos. – willlma Jan 20 '15 at 22:50
   
   [fuzzysort](https://github.com/farzher/fuzzysort)
   [reverse engine](https://www.forrestthewoods.com/blog/reverse_engineering_sublime_texts_fuzzy_match/) by Forrest Smith 
   [sublime text like fuzzy matching](https://www.willmcgugan.com/blog/tech/post/sublime-text-like-fuzzy-matching-in-javascript/)
   [another code](https://codesandbox.io/s/rll68lkn1q) of PAEz  I saw you post on reddit and it reminded me I did something like this once and wanted to remove the regex from it but never got round to it so yours interested me. Unfortunately I was interested in the word completion in the editor, didnt even realize it worked different else where. But made me do mine without regex which was fun, havent coded in ages. Was also interested in making it more unicode compatible coz we got new stuff in es6 that makes working with them better but not perfect. I made a version of yours that is very compatible if you use the grapheme splitter. Anywayz, all fun, heres some links...

       Yours with Unicode support
       https://codesandbox.io/s/rll68lkn1q
       Theres some checkboxs to turn grapheme splitting on and off. This allows you to handle stuff that es6 doesnt. Turn it of and copy and paste the yoga dude into the search box. Notice the entry in the list now has a symbol next to the first dude. Thats because of the es6 not handling a zero width joiner. Turn it on and it goes away. Look in the browsers console to see speed results.

       Article I got my unicode knowledge from....
       https://mathiasbynens.be/notes/javascript-unicode

       My Word Completion.....
       https://codesandbox.io/s/40125w9850

       My original word completion....
       https://groups.google.com/d/topic/google-chrome-developer-tools/3Zeuz_CmYZE/discussion
       
       [forked](https://codesandbox.io/s/fuzzy-matching-demo-forked-3tqnj)
