---
layout: post
title:  "How to html5 game?"
date:   2015-07-31 15:00:00
categories: programming warmup
---
Just so we know, what we are up against, we take a quick glance what solutions are readily available:

### Super viable options

Currently the best you can do imho, is to use a proper game engine and use its html5 export capabilities.

Some options are

* [Unity][unity]
* [Unreal Engine][unreal]
* [Godot Engine][godot]

In the ideal game you create your game, with all the sweet interactivity and assistance provided by the engine, and then you export your game to html5 with no added pain.

### Generally viable options

* Plain old JavaScript
  * But you may need to apply some trickery to get the performance just right. Luckily there are lots of resources readily available to provide valuable advice in this respect.
* [asm.js][asmjs] / [emscripten][emscripten]
  * Take a well proven non-html5 toolkit and cross compile to html/asm.js with comparable to native performance
    * But do keep in mind portability issues!

### Viable within specific contexts

* Pick your favorite language/technique and find a context it suits
  * Just play to the strengths of your choice!
* For me I am especially impressed with [ClojureScript][clojurescript]
  * Notably because its highly interactive style of programming
    * Normal mode of operation is to have your code loaded, whilst creating the programming:
      You hook an interactive console ("repl" = read eval print loop) to your running environment and use it to inject arbitrary code.
      * E.g. for debugging, adding new code, changing state, etc.
    * And even more awesome: You may use [figwheel][figwheel] to apply your code changes to a live running instance without any interaction, besides saving your source file.
  * For me the big caveat is that in my impression, you often need to invest considerable effort to get the performance right (and I am not convinced yet, ClojureScript can be used in a high performance scenario in its current state). 
    So far as I know there are also no established best practices for ensuring or tuning performance.

### Is there something similar to Clojure, but more suited to soft real time scenarios?

I am not sure, how such a thing should look like. Therefore the _only_ logical conclusion of course is to experiment with a custom lisp implementation. As previously stated, it is still questionable, whether in the end, we get something usable in this regard, but in the spirit of [Laozi][laozi]: _the journey is the reward_.

Stay tuned for the next post, where we will explore different memory management strategies and lisp's opinion in this regard.

[unity]: https://unity3d.com
[unreal]: https://unity3d.com
[godot]: http://www.godotengine.org
[asmjs]: http://asmjs.org
[emscripten]: http://kripken.github.io/emscripten-site
[clojurescript]: https://github.com/clojure/clojurescript
[figwheel]: https://github.com/bhauman/lein-figwheel
[laozi]: https://en.wikipedia.org/wiki/Laozi
