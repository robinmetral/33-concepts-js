<h1 align="center">
<br>
  <a href="https://github.com/robinmetral/33-concepts-js"><img src="https://i.imgur.com/dsHmk6H.jpg" alt="33 concepts que tout développeur JavaScript devrait connaître" width=200"></a>
  <br>
    <br>
    33 concepts que tout développeur JavaScript devrait connaître.
  <br><br>
</h1>

<p align="center">
  <a href="https://opensource.guide/fr/how-to-contribute/#ouvrir-une-pull-request">
    <img src="https://img.shields.io/badge/PRs-bienvenues-brightgreen.svg?style=flat-square" alt="PRs bienvenues">
  </a>
  <a href="https://opensource.org/licenses/MIT">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License MIT">
  </a>
</p>

## Introduction

Cette repo est une traduction de [33-js-concepts](https://github.com/leonardomso/33-js-concepts) par [Leonardo Madonaldo](https://twitter.com/leonardomso).

Elle a été créée dans le but d'aider les développeurs à maîtriser les concepts fondamentaux du JavaScript, et fonctionne comme un guide pour continuer à apprendre. Elle est basée sur un article écrit par [Stephen Curtis](https://twitter.com/stephenthecurt), que vous pouvez lire [ici](https://medium.com/@stephenthecurt/33-fundamentals-every-javascript-developer-should-know-13dd720a90d1) (en anglais :gb:).

:rocket: **La version en anglais de cette repo est considérée par GitHub comme étant l'un des [meilleurs projets open-source de 2018 !](https://blog.github.com/2018-12-13-new-open-source-projects/)**

:information_source: _Les ressources mentionnées sont principalement en anglais. Si vous connaissez une ressource en français, n'hésitez pas à faire un pull request !_

---

## Table des matières

1. **[Call Stack](#1-call-stack)**
2. **[Primitive Types](#2-primitive-types)**
3. **[Value Types and Reference Types](#3-value-types-and-reference-types)**
4. **[Implicit, Explicit, Nominal, Structuring and Duck Typing](#4-implicit-explicit-nominal-structuring-and-duck-typing)**
5. **[== vs === vs typeof](#5--vs--vs-typeof)**
6. **[Function Scope, Block Scope and Lexical Scope](#6-function-scope-block-scope-and-lexical-scope)**
7. **[Expression vs Statement](#7-expression-vs-statement)**
8. **[IIFE, Modules and Namespaces](#8-iife-modules-and-namespaces)**
9. **[Message Queue and Event Loop](#9-message-queue-and-event-loop)**
10. **[setTimeout, setInterval and requestAnimationFrame](#10-settimeout-setinterval-and-requestanimationframe)**
11. **[JavaScript Engines](#11-javascript-engines)**
12. **[Bitwise Operators, Type Arrays and Array Buffers](#12-bitwise-operators-type-arrays-and-array-buffers)**
13. **[DOM and Layout Trees](#13-dom-and-layout-trees)**
14. **[Factories and Classes](#14-factories-and-classes)**
15. **[this, call, apply and bind](#15-this-call-apply-and-bind)**
16. **[new, Constructor, instanceof and Instances](#16-new-constructor-instanceof-and-instances)**
17. **[Prototype Inheritance and Prototype Chain](#17-prototype-inheritance-and-prototype-chain)**
18. **[Object.create and Object.assign](#18-objectcreate-and-objectassign)**
19. **[map, reduce, filter](#19-map-reduce-filter)**
20. **[Pure Functions, Side Effects and State Mutation](#20-pure-functions-side-effects-and-state-mutation)**
21. **[Closures](#21-closures)**
22. **[High Order Functions](#22-high-order-functions)**
23. **[Recursion](#23-recursion)**
24. **[Collections and Generators](#24-collections-and-generators)**
25. **[Promises](#25-promises)**
26. **[async/await](#26-asyncawait)**
27. **[Data Structures](#27-data-structures)**
28. **[Expensive Operation and Big O Notation](#28-expensive-operation-and-big-o-notation)**
29. **[Algorithms](#29-algorithms)**
30. **[Inheritance, Polymorphism and Code Reuse](#30-inheritance-polymorphism-and-code-reuse)**
31. **[Design Patterns](#31-design-patterns)**
32. **[Partial Applications, Currying, Compose and Pipe](#32-partial-applications-currying-compose-and-pipe)**
33. **[Clean Code](#33-clean-code)**


---

## 1. Call Stack

### Articles

 * :scroll: [Understanding Javascript Call Stack, Event Loops — Gaurav Pandvia](https://medium.com/@gaurav.pandvia/understanding-javascript-function-executions-tasks-event-loop-call-stack-more-part-1-5683dea1f5ec)
 * :scroll: [Understanding the JavaScript Call Stack — Charles Freeborn](https://medium.freecodecamp.org/understanding-the-javascript-call-stack-861e41ae61d4)
 * :scroll: [Javascript: What Is The Execution Context? What Is The Call Stack? — Valentino Gagliardi](https://www.valentinog.com/blog/js-execution-context-call-stack/)
 * :scroll: [What is the JS Event Loop and Call Stack? — Jess Telford](https://gist.github.com/jesstelford/9a35d20a2aa044df8bf241e00d7bc2d0)
 * :scroll: [Call Stack — MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
 * :scroll: [Understanding Execution Context and Execution Stack in Javascript — Sukhjinder Arora](https://blog.bitsrc.io/understanding-execution-context-and-execution-stack-in-javascript-1c9ea8642dd0)
 * :scroll: [How JavaScript Works: An Overview of the Engine, the Runtime, and the Call Stack — Alexander Zlatkov](https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf)
 * :scroll: [The Ultimate Guide to Execution Contexts, Hoisting, Scopes, and Closures in JavaScript — Tyler McGinnis](https://tylermcginnis.com/ultimate-guide-to-execution-contexts-hoisting-scopes-and-closures-in-javascript/)

### Vidéos

 * :movie_camera: [Javascript: the Call Stack explained — Coding Blocks India](https://www.youtube.com/watch?v=w6QGEiQceOM)
 * :movie_camera: [The JS Call Stack Explained In 9 Minutes — Colt Steele](https://www.youtube.com/watch?v=W8AeMrVtFLY)
 * :movie_camera: [JavaScript Execution Stack — Codecademy](https://www.youtube.com/watch?v=jT0USJeNFEA)
 * :movie_camera: [What is the Call Stack? — Eric Traub](https://www.youtube.com/watch?v=w7QWQlkLY_s)
 * :movie_camera: [The Call Stack — Kevin Drumm](https://www.youtube.com/watch?v=Q2sFmqvpBe0)
 * :movie_camera: [Understanding JavaScript Execution — Codesmith](https://www.youtube.com/watch?v=Z6a1cLyq7Ac&list=PLWrQZnG8l0E4kd1T_nyuVoxQUaYEWFgcD)
 * :movie_camera: [Call Stack & Event Loop — movies com](https://www.youtube.com/watch?v=mk0lu9MKBto)
 * :movie_camera: [The Ultimate Guide to Execution Contexts, Hoisting, Scopes, and Closures in JavaScript — Tyler McGinnis](https://www.youtube.com/watch?v=Nt-qa_LlUH0)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 2. Primitive Types

### Articles

 * :scroll: [How numbers are encoded in JavaScript — Dr. Axel Rauschmayer](http://2ality.com/2012/04/number-encoding.html)
 * :scroll: [What You Need to Know About JavaScript Number Type — Max Wizard K](https://medium.com/dailyjs/javascripts-number-type-8d59199db1b6)
 * :scroll: [What Every JavaScript Developer Should Know About Floating Point Numbers — Chewxy](https://blog.chewxy.com/2014/02/24/what-every-javascript-developer-should-know-about-floating-point-numbers/)
 * :scroll: [The Secret Life of JavaScript Primitives — Angus Croll](https://javascriptweblog.wordpress.com/2010/09/27/the-secret-life-of-javascript-primitives/)
 * :scroll: [Primitive Types — Flow](https://flow.org/en/docs/types/primitives/)
 * :scroll: [(Not) Everything in JavaScript is an Object - Daniel Li](http://blog.brew.com.hk/not-everything-in-javascript-is-an-object/)
 * :scroll: [JavaScript data types and data structures - MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Primitive_values)

### Vidéos

 * :movie_camera: [JavaScript Reference vs Primitive Types — Academind](https://www.youtube.com/watch?v=9ooYYRLdg_g)
 * :movie_camera: [JavaScript Primitive Types — Simon Sez IT](https://www.youtube.com/watch?v=HsbWQsSCE5Y)
 * :movie_camera: [Value Types and Reference Types in JavaScript — Programming with Mosh](https://www.youtube.com/watch?v=e-_mDyqm2oU)
 * :movie_camera: [JavaScript Primitive Data Types — Avelx](https://www.youtube.com/watch?v=qw3j0A3DIzQ)
 * :movie_camera: [Everything you never wanted to know about JavaScript numbers — Bartek Szopka](https://www.youtube.com/watch?v=MqHDDtVYJRI)
 * :movie_camera: [What are variables in Javascript? — JS For Everyone](https://www.youtube.com/watch?v=B4Bbmei_thw)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 3. Value Types and Reference Types

### Articles

 * :scroll: [Explaining Value vs. Reference in Javascript — Arnav Aggarwal](https://codeburst.io/explaining-value-vs-reference-in-javascript-647a975e12a0)
 * :scroll: [Understand Value and Reference Types in JavaScript — Zsolt Nagy](https://www.zsoltnagy.eu/understand-value-and-reference-types-in-javascript/)
 * :scroll: [Primitive Types & Reference Types in JavaScript — Bran van der Meer](https://gist.github.com/branneman/7fb06d8a74d7e6d4cbcf75c50fec599c)
 * :scroll: [Value Types, Reference Types and Scope in JavaScript — Ben Aston](https://medium.com/@benastontweet/lesson-1b-javascript-fundamentals-380f601ba851)
 * :scroll: [Back to roots: JavaScript Value vs Reference — Miro Koczka](https://medium.com/dailyjs/back-to-roots-javascript-value-vs-reference-8fb69d587a18)
 * :scroll: [Grasp “By Value” and “By Reference” in JavaScript — Léna Faure](https://hackernoon.com/grasp-by-value-and-by-reference-in-javascript-7ed75efa1293)
 * :scroll: [JavaScript Reference and Copy Variables — Vítor Capretz](https://hackernoon.com/javascript-reference-and-copy-variables-b0103074fdf0)
 * :scroll: [JavaScript Primitive vs Reference Values](http://www.javascripttutorial.net/javascript-primitive-vs-reference-values/)
 * :scroll: [JavaScript by Reference vs. by Value — nrabinowitz](https://stackoverflow.com/questions/6605640/javascript-by-reference-vs-by-value)

### Vidéos

 * :movie_camera: [Javascript Pass by Value vs Pass by Reference — techsith](https://www.youtube.com/watch?v=E-dAnFdq8k8)
 * :movie_camera: [JavaScript Value vs Reference Types — Programming with Mosh](https://www.youtube.com/watch?v=fD0t_DKREbE)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 4. Implicit, Explicit, Nominal, Structuring and Duck Typing

### Articles

 * :scroll: [What you need to know about Javascript's Implicit Coercion — Promise Tochi](https://dev.to/promhize/what-you-need-to-know-about-javascripts-implicit-coercion-e23)
 * :scroll: [JavaScript Type Coercion Explained — Alexey Samoshkin](https://medium.freecodecamp.org/js-type-coercion-explained-27ba3d9a2839)
 * :scroll: [Javascript Coercion Explained — Ben Garrison](https://hackernoon.com/javascript-coercion-explained-545c895213d3)
 * :scroll: [What exactly is Type Coercion in Javascript? - Stack Overflow](https://stackoverflow.com/questions/19915688/what-exactly-is-type-coercion-in-javascript)
 * :scroll: [You Don't Know JS: Types & Grammar [Book] — Kyle Simpson](https://www.oreilly.com/library/view/you-dont-know/9781491905159/ch04.html)
 * :scroll: [(Not) Everything in JavaScript is an Object - Daniel Li](http://blog.brew.com.hk/not-everything-in-javascript-is-an-object/)
 * :scroll: [Type Coercion in JavaScript, and why everyone gets it wrong.](https://thedevs.network/blog/type-coercion-in-javascript-and-why-everyone-gets-it-wrong)

### Vidéos

 * :movie_camera: [== ? === ??? ...#@^% - Shirmung Bielefeld](https://www.youtube.com/watch?v=qGyqzN0bjhc&t)
 * :movie_camera: [Coercion in Javascript - Hitesh Choudhary](https://www.youtube.com/watch?v=b04Q_vyqEG8)
 * :movie_camera: [JavaScript Questions: What is Coercion? - Steven Hancock](https://www.youtube.com/watch?v=z4-8wMSPJyI)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 5. == vs === vs typeof

### Articles

 * :scroll: [JavaScript Double Equals vs. Triple Equals — Brandon Morelli](https://codeburst.io/javascript-double-equals-vs-triple-equals-61d4ce5a121a)
 * :scroll: [What is the difference between =, ==, and === in JS? — Codecademy](https://www.codecademy.com/en/forum_questions/558ea4f5e39efed371000508)
 * :scroll: [Should I use === or == equality comparison operator in JavaScript? — Panu Pitkamaki](https://bytearcher.com/articles/equality-comparison-operator-javascript/)
 * :scroll: [== vs === JavaScript: Double Equals and Coercion — AJ Meyghani](https://www.codementor.io/javascript/tutorial/double-equals-and-coercion-in-javascript)
 * :scroll: [Why Use the Triple-Equals Operator in JavaScript? — Louis Lazaris](https://www.impressivewebs.com/why-use-triple-equals-javascipt/)
 * :scroll: [What is the difference between == and === in JavaScript? — Craig Buckler](https://www.oreilly.com/learning/what-is-the-difference-between-and-in-javascript)
 * :scroll: [Why javascript's typeof always return "object"? — Stack Overflow](https://stackoverflow.com/questions/3787901/why-javascripts-typeof-always-return-object)
 * :scroll: [Checking Types in Javascript — Toby Ho](http://tobyho.com/2011/01/28/checking-types-in-javascript/)
 * :scroll: [How to better check data types in JavaScript — Webbjocke](https://webbjocke.com/javascript-check-data-types/)
 * :scroll: [Checking for the Absence of a Value in JavaScript — Tomer Aberbach](https://tomeraberba.ch/html/post/checking-for-the-absence-of-a-value-in-javascript.html)

### Vidéos

 * :movie_camera: [JavaScript - The typeof operator — Java Brains](https://www.youtube.com/watch?v=ol_su88I3kw)
 * :movie_camera: [Javascript typeof operator — DevDelight](https://www.youtube.com/watch?v=qPYhTPt_SbQ)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 6. Function Scope, Block Scope and Lexical Scope

### Articles

 * :scroll: [You Don't Know JS: Scope & Closures [Book] — Kyle Simpson](https://github.com/getify/You-Dont-Know-JS/blob/master/scope%20%26%20closures/ch3.md)
 * :scroll: [JavaScript Functions — Understanding The Basics — Brandon Morelli](https://codeburst.io/javascript-functions-understanding-the-basics-207dbf42ed99)
 * :scroll: [The battle between Function Scope and Block Scope — Marius Herring](http://www.deadcoderising.com/2017-04-11-es6-var-let-and-const-the-battle-between-function-scope-and-block-scope/)
 * :scroll: [Emulating Block Scope in JavaScript — Josh Clanton](http://adripofjavascript.com/blog/drips/emulating-block-scope-in-javascript.html)
 * :scroll: [The Difference Between Function and Block Scope in JavaScript — Joseph Cardillo](https://medium.com/@josephcardillo/the-difference-between-function-and-block-scope-in-javascript-4296b2322abe)
 * :scroll: [Function Scopes and Block Scopes in JavaScript — Samer Buna](https://edgecoders.com/function-scopes-and-block-scopes-in-javascript-25bbd7f293d7)
 * :scroll: [Understanding Scope and Context in JavaScript | Ryan Morr](http://ryanmorr.com/understanding-scope-and-context-in-javascript/)
 * :scroll: [JavaScript Scope and Closures — Zell Liew](https://css-tricks.com/javascript-scope-closures/)
 * :scroll: [Understanding Scope in JavaScript — Wissam Abirached](https://developer.telerik.com/topics/web-development/understanding-scope-in-javascript/)
 * :scroll: [Speaking JavaScript - Variables: Scopes, Environments, and Closures — Dr. Axel Rauschmayer](http://speakingjs.com/es5/ch16.html)
 * :scroll: [Understanding Scope in JavaScript ― Hammad Ahmed](https://scotch.io/tutorials/understanding-scope-in-javascript)

### Vidéos

 * :movie_camera: [What Makes Javascript Weird ... and Awesome pt. 4 — LearnCode.academy](https://www.youtube.com/watch?v=SBwoFkRjZvE)
 * :movie_camera: [Variable Scope in JavaScript — Kirupa Chinnathambi](https://www.youtube.com/watch?v=dhp57T3p760)
 * :movie_camera: [JavaScript Block Scope and Function Scope — mmtuts](https://www.youtube.com/watch?v=aK_nuUAdr8E)
 * :movie_camera: [What the Heck is Lexical Scope? — NWCalvank](https://www.youtube.com/watch?v=GhNA0r10MmA)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 7. Expression vs Statement

### Articles

 * :scroll: [All you need to know about Javascript's Expressions, Statements and Expression Statements — Promise Tochi](https://dev.to/promhize/javascript-in-depth-all-you-need-to-know-about-expressions-statements-and-expression-statements-5k2)
 * :scroll: [Function Expressions vs Function Declarations — Paul Wilkins](https://www.sitepoint.com/function-expressions-vs-declarations/)
 * :scroll: [JavaScript Function — Declaration vs Expression — Ravi Roshan](https://medium.com/@raviroshan.talk/javascript-function-declaration-vs-expression-f5873b8c7b38)
 * :scroll: [Function Declarations vs. Function Expressions — Mandeep Singh](https://medium.com/@mandeep1012/function-declarations-vs-function-expressions-b43646042052)
 * :scroll: [Function Declarations vs. Function Expressions — Anguls Croll](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/)

### Vidéos

 * :movie_camera: [Expressions vs. Statements in JavaScript — Hexlet](https://www.youtube.com/watch?v=WVyCrI1cHi8)
 * :movie_camera: [JavaScript - Expression vs. Statement — WebTunings](https://www.youtube.com/watch?v=3jDpNGJkupA)
 * :movie_camera: [Function Statements and Function Expressions — Codeacademy](https://www.youtube.com/watch?v=oB5rH_9bqAI)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 8. IIFE, Modules and Namespaces

### Articles

 * :scroll: [Mastering Immediately-Invoked Function Expressions ― Chandra Gundamaraju](https://medium.com/@vvkchandra/essential-javascript-mastering-immediately-invoked-function-expressions-67791338ddc6)
 * :scroll: [Do ES6 Modules make the case of IIFEs obsolete?](https://hashnode.com/post/do-es6-modules-make-the-case-of-iifes-obsolete-civ96wet80scqgc538un20es0)
 * :scroll: [A 10 minute primer to JavaScript modules, module formats, module loaders and module bundlers ― Jurgen Van de Moere](https://www.jvandemo.com/a-10-minute-primer-to-javascript-modules-module-formats-module-loaders-and-module-bundlers/)
 * :scroll: [Modules ― Exploring JS](http://exploringjs.com/es6/ch_modules.html)
 * :scroll: [ES modules: A cartoon deep-dive — Lin Clark](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)
 * :scroll: [Understanding ES6 Modules — Craig Buckler](https://www.sitepoint.com/understanding-es6-modules/)
 * :scroll: [An overview of ES6 Modules in JavaScript — Brent Graham](https://blog.cloud66.com/an-overview-of-es6-modules-in-javascript/)
 * :scroll: [ES6 Modules in Depth — Nicolás Bevacqua](https://ponyfoo.com/articles/es6-modules-in-depth)
 * :scroll: [ES6 modules, Node.js and the Michael Jackson Solution — Alberto Gimeno](https://medium.com/dailyjs/es6-modules-node-js-and-the-michael-jackson-solution-828dc244b8b)
 * :scroll: [JavaScript Modules: A Beginner’s Guide — Preethi Kasireddy](https://medium.freecodecamp.org/javascript-modules-a-beginner-s-guide-783f7d7a5fcc)

### Vidéos

 * :movie_camera: [Immediately Invoked Function Expression - Beau teaches JavaScript — freeCodeCamp](https://www.youtube.com/watch?v=3cbiZV4H22c)
 * :movie_camera: [Understanding JavaScript IIFE](https://www.youtube.com/watch?v=I5EntfMeIIQ)
 * :movie_camera: [JavaScript Modules: ES6 Import and Export — Kyle Robinson](https://www.youtube.com/watch?v=_3oSWwapPKQ)
 * :movie_camera: [ES6 - Modules — Ryan Christiani](https://www.youtube.com/watch?v=aQr2bV1BPyE)
 * :movie_camera: [ES6 Modules in the Real World — Sam Thorogood](https://www.youtube.com/watch?v=fIP4pjAqCtQ)
 * :movie_camera: [ES6 Modules — TempleCoding](https://www.youtube.com/watch?v=5P04OK6KlXA)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 9. Message Queue and Event Loop

### Articles

 * :scroll: [JavaScript Event Loop Explained — Anoop Raveendran](https://medium.com/front-end-hacking/javascript-event-loop-explained-4cd26af121d4)
 * :scroll: [The JavaScript Event Loop: Explained — Erin Sweson-Healey](https://blog.carbonfive.com/2013/10/27/the-javascript-event-loop-explained/)
 * :scroll: [What is the Event Loop in Javascript — WP Tutor.io](https://www.wptutor.io/web/js/javascript-event-loop)
 * :scroll: [Understanding JS: The Event Loop — Alexander Kondov](https://hackernoon.com/understanding-js-the-event-loop-959beae3ac40)
 * :scroll: [Understanding the JavaScript Event Loop — Ashish Gupta](https://www.zeolearn.com/magazine/understanding-the-javascript-event-loop)
 * :scroll: [Event Loop in Javascript — Manjula Dube](https://code.likeagirl.io/what-the-heck-is-event-loop-1e414fccef49)
 * :scroll: [The JavaScript Event Loop — Flavio Copes](https://flaviocopes.com/javascript-event-loop/)
 * :scroll: [How JavaScript works: Event loop — Alexander Zlatkov](https://blog.sessionstack.com/how-javascript-works-event-loop-and-the-rise-of-async-programming-5-ways-to-better-coding-with-2f077c4438b5)
 * :scroll: [Visualising the JavaScript Event Loop with a Pizza Restaurant analogy — Priyansh Jain](https://dev.to/presto412/visualising-the-javascript-event-loop-with-a-pizza-restaurant-analogy-47a8)

### Vidéos

 * :movie_camera: [What the heck is the event loop anyway? | JSConf EU — Philip Roberts](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
 * :movie_camera: [JavaScript Event Loop — ComScience Simplified](https://www.youtube.com/watch?v=XzXIMZMN9k4)
 * :movie_camera: [I'm stuck in an Event Loop — Philip Roberts](https://www.youtube.com/watch?v=6MXRNXXgP_0)
 * :movie_camera: [In The Loop - Jake Archibald | JSConf.Asia 2018](https://www.youtube.com/watch?v=cCOL7MC4Pl0)
 * :movie_camera: [Desmitificando el Event Loop (Spanish)](https://www.youtube.com/watch?v=Eqq2Rb7LzYE)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 10. setTimeout, setInterval and requestAnimationFrame

### Articles

 * :scroll: [setTimeout and setInterval — JavaScript.Info](https://javascript.info/settimeout-setinterval)
 * :scroll: [Why not to use setInterval — Akanksha Sharma](https://dev.to/akanksha_9560/why-not-to-use-setinterval--2na9)
 * :scroll: [setTimeout VS setInterval — Develoger](https://develoger.com/settimeout-vs-setinterval-cff85142555b)
 * :scroll: [Using requestAnimationFrame — Chris Coyier](https://css-tricks.com/using-requestanimationframe/)
 * :scroll: [Understanding JavaScript's requestAnimationFrame() — JavaScript Kit](http://www.javascriptkit.com/javatutors/requestanimationframe.shtml)
 * :scroll: [Handling time intervals in JavaScript - Amit Merchant](https://www.amitmerchant.com/Handling-Time-Intervals-In-Javascript/)

### Vidéos

 * :movie_camera: [Javascript: How setTimeout and setInterval works — Coding Blocks India](https://www.youtube.com/watch?v=6bPKyl8WYWI)
 * :movie_camera: [setTimeout and setInterval in JavaScript — techsith](https://www.youtube.com/watch?v=TbCgGWe8LN8)
 * :movie_camera: [JavaScript Timers — Steve Griffith](https://www.youtube.com/watch?v=0VVJSvlUgtg)
 * :movie_camera: [JavaScript setTimeout, setInterval & clearInterval — DoingITeasyChannel](https://www.youtube.com/watch?v=BVALvvy5bZY)
 * :movie_camera: [JavaScript setTimeOut and setInterval Explained — Theodore Anderson](https://www.youtube.com/watch?v=mVKfrWCOB60)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 11. JavaScript Engines

### Articles

 * :scroll: [JavaScript Engines — Jen Looper](http://www.softwaremag.com/javascript-engines/)
 * :scroll: [Understanding How the Chrome V8 Engine Translates JavaScript into Machine Code — DroidHead](https://medium.freecodecamp.org/understanding-the-core-of-nodejs-the-powerful-chrome-v8-engine-79e7eb8af964)
 * :scroll: [Understanding V8’s Bytecode — Franziska Hinkelmann](https://medium.com/dailyjs/understanding-v8s-bytecode-317d46c94775)
 * :scroll: [How the V8 engine works? — Thibault Laurens](http://thibaultlaurens.github.io/javascript/2013/04/29/how-the-v8-engine-works/)
 * :scroll: [A Brief History of Google’s V8 Javascript Engine — Clair Smith](https://www.mediacurrent.com/blog/brief-history-googles-v8-javascript-engine/)
 * :scroll: [JavaScript essentials: why you should know how the engine works - Rainer Hahnekamp](https://medium.freecodecamp.org/javascript-essentials-why-you-should-know-how-the-engine-works-c2cc0d321553)


### Vidéos

 * :movie_camera: [JavaScript Engines: The Good Parts™ — Mathias Bynens & Benedikt Meurer](https://www.youtube.com/watch?v=5nmpokoRaZI)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 12. Bitwise Operators, Type Arrays and Array Buffers

### Articles

 * :scroll: [Programming with JS: Bitwise Operations — Alexander Kondov](https://hackernoon.com/programming-with-js-bitwise-operations-393eb0745dc4)
 * :scroll: [Using JavaScript’s Bitwise Operators in Real Life — ian m](https://codeburst.io/using-javascript-bitwise-operators-in-real-life-f551a731ff5)
 * :scroll: [JavaScript Bitwise Operators — w3resource](https://www.w3resource.com/javascript/operators/bitwise-operator.php)
 * :scroll: [Bitwise Operators in Javascript — Joe Cha](https://medium.com/bother7-blog/bitwise-operators-in-javascript-65c4c69be0d3)
 * :scroll: [A Comprehensive Primer on Binary Computation and Bitwise Operators in Javascript — Paul Brown](https://medium.com/techtrument/a-comprehensive-primer-on-binary-computation-and-bitwise-operators-in-javascript-81acf8341f04)

### Vidéos

 * :movie_camera: [JavaScript Bitwise Operators — Programming with Mosh](https://www.youtube.com/watch?v=mesu75PTDC8)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 13. DOM and Layout Trees

### Articles

 * :scroll: [How To Understand and Modify the DOM in JavaScript — Tania Rascia](https://www.digitalocean.com/community/tutorials/introduction-to-the-dom)
 * :scroll: [What’s the Document Object Model, and why you should know how to use it — Leonardo Maldonado](https://medium.freecodecamp.org/whats-the-document-object-model-and-why-you-should-know-how-to-use-it-1a2d0bc5429d)
 * :scroll: [JavaScript DOM Tutorial with Example — Guru99](https://www.guru99.com/how-to-use-dom-and-events-in-javascript.html)
 * :scroll: [What is the DOM? — Chris Coyier](https://css-tricks.com/dom/)
 * :scroll: [Traversing the DOM with JavaScript — Zell Liew](https://zellwk.com/blog/dom-traversals/)
 * :scroll: [Eloquent JavaScript [Book] — The Document Object Model](https://eloquentjavascript.net/14_dom.html)
 * :scroll: [DOM Tree](https://javascript.info/dom-nodes)
 * :scroll: [How to traverse the DOM in Javascript — Vojislav Grujić](https://medium.com/javascript-in-plain-english/how-to-traverse-the-dom-in-javascript-d6555c335b4e)
 * :scroll: [Render Tree Construction — Ilya Grigorik](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction)

### Vidéos

 * :movie_camera: [JavaScript DOM — The Net Ninja](https://www.youtube.com/watch?v=FIORjGvT0kk)
 * :movie_camera: [JavaScript DOM Crash Course — Traversy Media](https://www.youtube.com/watch?v=0ik6X4DJKCc)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 14. Factories and Classes

### Articles

 * :scroll: [How To Use Classes in JavaScript — Tania Rascia](https://www.digitalocean.com/community/tutorials/understanding-classes-in-javascript)
 * :scroll: [Javascript Classes — Under The Hood — Majid](https://medium.com/tech-tajawal/javascript-classes-under-the-hood-6b26d2667677)
 * :scroll: [ES6 Classes — Nathaniel Foster](https://www.javascriptjanuary.com/blog/es6-classes)
 * :scroll: [Better JavaScript with ES6, Pt. II: A Deep Dive into Classes ― Peleke Sengstacke](https://scotch.io/tutorials/better-javascript-with-es6-pt-ii-a-deep-dive-into-classes)
 * :scroll: [Understand the Factory Design Pattern in Plain JavaScript — Aditya Agarwal](https://medium.com/front-end-hacking/understand-the-factory-design-pattern-in-plain-javascript-20b348c832bd)
 * :scroll: [Factory Functions in JavaScript — Josh Miller](https://atendesigngroup.com/blog/factory-functions-javascript)
 * :scroll: [The Factory Pattern in JS ES6 — SnstsDev](https://medium.com/@SntsDev/the-factory-pattern-in-js-es6-78f0afad17e9)
 * :scroll: [Class vs Factory function: exploring the way forward — Cristi Salcescu](https://medium.freecodecamp.org/class-vs-factory-function-exploring-the-way-forward-73258b6a8d15)
 * :scroll: [How ES6 classes really work and how to build your own — Robert Grosse](https://medium.com/@robertgrosse/how-es6-classes-really-work-and-how-to-build-your-own-fd6085eb326a)

### Vidéos

 * :movie_camera: [JavaScript Factory Functions — Programming with Mosh](https://www.youtube.com/watch?v=jpegXpQpb3o)
 * :movie_camera: [Factory Functions in JavaScript — Fun Fun Function](https://www.youtube.com/watch?v=ImwrezYhw4w)
 * :movie_camera: [Javascript Tutorial Function Factories — Crypto Chan](https://www.youtube.com/watch?v=R7-IwpH80UE)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 15. this, call, apply and bind

### Articles

 * :scroll: [How-to: call() , apply() and bind() in JavaScript — Niladri Sekhar Dutta](https://www.codementor.io/niladrisekhardutta/how-to-call-apply-and-bind-in-javascript-8i1jca6jp)
 * :scroll: [JavaScript’s Apply, Call, and Bind Methods are Essential for JavaScript Professionals — Richard Bovell](http://javascriptissexy.com/javascript-apply-call-and-bind-methods-are-essential-for-javascript-professionals/)
 * :scroll: [WTF is this - Understanding the this keyword, call, apply, and bind in JavaScript — Tyler McGinnis](https://tylermcginnis.com/this-keyword-call-apply-bind-javascript/)
 * :scroll: [Javascript: call(), apply() and bind() — Omer Goldberg](https://medium.com/@omergoldberg/javascript-call-apply-and-bind-e5c27301f7bb)
 * :scroll: [The difference between call / apply / bind — Ivan Sifrim](https://medium.com/@ivansifrim/the-differences-between-call-apply-bind-276724bb825b)
 * :scroll: [call(), apply() and bind() methods in JavaScript](https://tech.io/playgrounds/9799/learn-solve-call-apply-and-bind-methods-in-javascript)
 * :scroll: [Mastering 'this' in JavaScript: Callbacks and bind(), apply(), call() — Michelle Gienow](https://thenewstack.io/mastering-javascript-callbacks-bind-apply-call/)
 * :scroll: [JavaScript’s apply, call, and bind explained by hosting a cookout — Kevin Kononenko](https://dev.to/kbk0125/javascripts-apply-call-and-bind-explained-by-hosting-a-cookout-32jo)
 * :scroll: [How AND When to use bind, call, and apply in Javascript — Eigen X](https://www.eigenx.com/blog/https/mediumcom/eigen-x/how-and-when-to-use-bind-call-and-apply-in-javascript-77b6f42898fb)
 * :scroll: [JavaScript .bind() vs .apply() and .call() — Hack Sparrow](https://www.hacksparrow.com/javascript-bind-vs-apply-and-call.html)
 * :scroll: [call() — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call)
 * :scroll: [bind() — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)
 * :scroll: [apply() — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/apply)
 * :scroll: [What is 'this' in JavaScript? — Daniel Li](http://blog.brew.com.hk/what-is-this-in-javascript/)
 * :scroll: [Let me explain to you what is `this`. (Javascript) — Jason Yu](https://dev.to/ycmjason/let-me-explain-to-you-what-is-this-javascript-44ja)
 * :scroll: [Understanding the “this” Keyword in JavaScript — Pavan](https://medium.com/quick-code/understanding-the-this-keyword-in-javascript-cb76d4c7c5e8)

### Vidéos

 * :movie_camera: [JavaScript call, apply and bind — techsith](https://www.youtube.com/watch?v=c0mLRpw-9rI)
 * :movie_camera: [JavaScript Practical Applications of Call, Apply and Bind functions— techsith](https://www.youtube.com/watch?v=AYVYxezrMWA)
 * :movie_camera: [JavaScript (call, bind, apply) — curious aatma](https://www.youtube.com/watch?v=Uy0NOXLBraE)
 * :movie_camera: [Understanding Functions and 'this' In The World of ES2017 — Bryan Hughes](https://www.youtube.com/watch?v=AOSYY1_np_4)
 * :movie_camera: [bind and this - Object Creation in JavaScript - FunFunFunction](https://www.youtube.com/watch?v=GhbhD1HR5vk)
 * :movie_camera: [JavaScript Practical Applications of Call, Apply and Bind functions — techsith](https://www.youtube.com/watch?v=AYVYxezrMWA)
 * :movie_camera: [JS Function Methods call(), apply(), and bind() — Steve Griffith](https://www.youtube.com/watch?v=uBdH0iB1VDM)
 
<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 16. new, Constructor, instanceof and Instances

### Articles

 * :scroll: [JavaScript For Beginners: the ‘new’ operator — Brandon Morelli](https://codeburst.io/javascript-for-beginners-the-new-operator-cee35beb669e)
 * :scroll: [Let’s demystify JavaScript’s ‘new’ keyword — Cynthia Lee](https://medium.freecodecamp.org/demystifying-javascripts-new-keyword-874df126184c)
 * :scroll: [Constructor, operator "new" — JavaScript.Info](https://javascript.info/constructor-new)
 * :scroll: [Understanding JavaScript Constructors — Faraz Kelhini](https://css-tricks.com/understanding-javascript-constructors/)
 * :scroll: [Use Constructor Functions — Openclassrooms](https://openclassrooms.com/en/courses/3523231-learn-to-code-with-javascript/4379006-use-constructor-functions)
 * :scroll: [Beyond `typeof` and `instanceof`: simplifying dynamic type checks — Dr. Axel Rauschmayer](http://2ality.com/2017/08/type-right.html)
 * :scroll: [What Is the Instanceof Operator in JavaScript — appendTo](https://appendto.com/2016/10/what-is-the-instanceof-operator-in-javascript/)
 * :scroll: [JavaScript instanceof vs typeof — Gary Rafferty](http://garyrafferty.com/2012/12/07/JavaScript-instanceof-vs-typeof.html)
 * :scroll: [Function and Object, instances of each other — Kiro Risk](https://javascriptrefined.io/function-and-object-instances-of-each-other-1e1095d5faac)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 17. Prototype Inheritance and Prototype Chain

### Articles

 * :scroll: [Javascript : Prototype vs Class — Valentin PARSY](https://medium.com/@parsyval/javascript-prototype-vs-class-a7015d5473b)
 * :scroll: [JavaScript engine fundamentals: optimizing prototypes — Mathias Bynens](https://mathiasbynens.be/notes/prototypes)
 * :scroll: [JavaScript Prototype — NC Patro](https://codeburst.io/javascript-prototype-cb29d82b8809)
 * :scroll: [Prototype in Javascript — Sandeep Ranjan](https://www.codementor.io/sandeepranjan2007/prototype-in-javascipt-knbve0lqo)
 * :scroll: [Prototypes in JavaScript — Rupesh Mishra](https://hackernoon.com/prototypes-in-javascript-5bba2990e04b)
 * :scroll: [Prototype in JavaScript: it’s quirky, but here’s how it works — Pranav Jindal](https://medium.freecodecamp.org/prototype-in-js-busted-5547ec68872)
 * :scroll: [Inheritance and the prototype chain — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
 * :scroll: [Understanding JavaScript: Prototype and Inheritance — Alexander Kondov](https://hackernoon.com/understanding-javascript-prototype-and-inheritance-d55a9a23bde2)
 * :scroll: [Prototypal Inheritance — JavaScript.Info](https://javascript.info/prototype-inheritance)
 * :scroll: [How To Work with Prototypes and Inheritance in JavaScript — Tania Rascia](https://www.digitalocean.com/community/tutorials/understanding-prototypes-and-inheritance-in-javascript)
 * :scroll: [Master JavaScript Prototypes & Inheritance — Arnav Aggarwal](https://codeburst.io/master-javascript-prototypes-inheritance-d0a9a5a75c4e)
 * :scroll: [You Don't Know JS [Book] Chapter 5: Prototypes — Kyle Simpson](https://github.com/getify/You-Dont-Know-JS/blob/master/this%20%26%20object%20prototypes/ch5.md)
 * :scroll: [JavaScript’s Prototypal Inheritance Explained Using CSS — Nash Vail](https://medium.freecodecamp.org/understanding-prototypal-inheritance-in-javascript-with-css-93b2fcda75e4)
 * :scroll: [Prototypal Inheritance in JavaScript — Jannis Redmann](https://gist.github.com/derhuerst/a585c4916b1c361cc6f0)
 * :scroll: [Classical and Prototypical Inheritance in JavaScript — Danny Cornelisse](http://www.competa.com/blog/classical-prototypical-inheritance-javascript/)
 * :scroll: [Demystifying ES6 Classes And Prototypal Inheritance ― Neo Ighodaro](https://scotch.io/tutorials/demystifying-es6-classes-and-prototypal-inheritance)
 * :scroll: [Intro To Prototypal Inheritance — Dharani Jayakanthan](https://dev.to/danny/intro-to-prototypal-inheritance---js-9di)
 * :scroll: [Classes in JavaScript - Explained — Daniel Li](http://blog.brew.com.hk/classes-in-javascript-explained/)
 * :scroll: [You Don't Know JS: this & Object Prototypes — Kyle Simpson](https://github.com/getify/You-Dont-Know-JS/blob/master/this%20%26%20object%20prototypes/ch4.md)

### Vidéos

 * :movie_camera: [Javascript Prototype Inheritance — Avelx](https://www.youtube.com/watch?v=sOrtAjyk4lQ)
 * :movie_camera: [JavaScript Prototype Inheritance Explained pt. I — techsith](https://www.youtube.com/watch?v=7oNWNlMrkpc)
 * :movie_camera: [JavaScript Prototype Inheritance Explained pt. II — techsith](https://www.youtube.com/watch?v=uIlj6_z_wL8)
 * :movie_camera: [JavaScript Prototype Inheritance Explained — Kyle Robinson](https://www.youtube.com/watch?v=qMO-LTOrJaE)
 * :movie_camera: [Advanced Javascript - Prototypal Inheritance In 1 Minute](https://www.youtube.com/watch?v=G6l5CHl67HQ)
 * :movie_camera: [An Overview Of Classical Javascript Classes and Prototypal Inheritance — Pentacode](https://www.youtube.com/watch?v=phwzuiJJPpQ)
 * :movie_camera: [Object Oriented JavaScript - Prototype — The Net Ninja](https://www.youtube.com/watch?v=4jb4AYEyhRc)
 * :movie_camera: [Prototype in JavaScript — kudvenkat](https://www.youtube.com/watch?v=2rkEbcptR64)
 * :movie_camera: [JavaScript Using Prototypes — O'Reilly](https://www.youtube.com/watch?v=oCwCcNvaXAQ)
 * :movie_camera: [A Beginner's Guide to Javascript's Prototype — Tyler Mcginnis](https://www.youtube.com/watch?v=XskMWBXNbp0)
 * :movie_camera: [Prototypes in Javascript - p5.js Tutorial — The Coding Train](https://www.youtube.com/watch?v=hS_WqkyUah8)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 18. Object.create and Object.assign

### Articles

 * :scroll: [Object.create() — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/create)
 * :scroll: [Object.create in JavaScript — Rupesh Mishra](https://hackernoon.com/object-create-in-javascript-fa8674df6ed2)
 * :scroll: [Object.create(): the New Way to Create Objects in JavaScript — Rob Gravelle](https://www.htmlgoodies.com/beyond/javascript/object.create-the-new-way-to-create-objects-in-javascript.html)
 * :scroll: [Basic Inheritance with Object.create — Joshua Clanton](http://adripofjavascript.com/blog/drips/basic-inheritance-with-object-create.html)
 * :scroll: [Object.create() In JavaScript — GeeksforGeeks](https://www.geeksforgeeks.org/object-create-javascript/)
 * :scroll: [Understanding the difference between Object.create() and the new operator — Jonathan Voxland](https://medium.com/@jonathanvox01/understanding-the-difference-between-object-create-and-the-new-operator-b2a2f4749358)
 * :scroll: [JavaScript Object Creation: Patterns and Best Practices — Jeff Mott](https://www.sitepoint.com/javascript-object-creation-patterns-best-practises/)
 * :scroll: [Dealing With Objects in JavaScript With Object.assign, Object.keys and hasOwnProperty](https://alligator.io/js/dealing-with-objects/)
 * :scroll: [Copying Objects in JavaScript ― Orinami Olatunji](https://scotch.io/bar-talk/copying-objects-in-javascript)
 * :scroll: [Object.assign() — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)
 * :scroll: [JavaScript: Object.assign() — Thiago S. Adriano](https://codeburst.io/javascript-object-assign-bc9696dcbb6e)
 * :scroll: [How to deep clone a JavaScript Object — Flavio Copes](https://flaviocopes.com/how-to-clone-javascript-object/)

### Vidéos

 * :movie_camera: [Object.assign() explained — Aaron Writes Code](https://www.youtube.com/watch?v=aw7NfYhR5rc)
 * :movie_camera: [Object.assign() Method — techsith](https://www.youtube.com/watch?v=9Ky4X6inpi4)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 19. map, reduce, filter

### Articles

 * :scroll: [JavaScript Functional Programming — map, filter and reduce — Bojan Gvozderac](https://medium.com/jsguru/javascript-functional-programming-map-filter-and-reduce-846ff9ba492d)
 * :scroll: [Learn map, filter and reduce in Javascript — João Miguel Cunha](https://medium.com/@joomiguelcunha/learn-map-filter-and-reduce-in-javascript-ea59009593c4)
 * :scroll: [JavaScript’s Map, Reduce, and Filter — Dan Martensen](https://danmartensen.svbtle.com/javascripts-map-reduce-and-filter)
 * :scroll: [How to Use Map, Filter, & Reduce in JavaScript — Peleke Sengstacke](https://code.tutsplus.com/tutorials/how-to-use-map-filter-reduce-in-javascript--cms-26209)
 * :scroll: [JavaScript — Learn to Chain Map, Filter, and Reduce — Brandon Morelli](https://codeburst.io/javascript-learn-to-chain-map-filter-and-reduce-acd2d0562cd4)
 * :scroll: [Javascript data structure with map, reduce, filter and ES6 — Deepak Gupta](https://codeburst.io/write-beautiful-javascript-with-%CE%BB-fp-es6-350cd64ab5bf)
 * :scroll: [Understanding map, filter and reduce in Javascript — Luuk Gruijs](https://hackernoon.com/understanding-map-filter-and-reduce-in-javascript-5df1c7eee464)
 * :scroll: [Functional Programming in JS: map, filter, reduce (Pt. 5) — Omer Goldberg](https://hackernoon.com/functional-programming-in-js-map-filter-reduce-pt-5-308a205fdd5f)
 * :scroll: [JavaScript: Map, Filter, Reduce — William S. Vincent](https://wsvincent.com/functional-javascript-map-filter-reduce/)
 * :scroll: [Arrow Functions: Fat and Concise Syntax in JavaScript — Kyle Pennell](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript/)
 * :scroll: [JavaScript: Arrow Functions for Beginners — Brandon Morelli](https://codeburst.io/javascript-arrow-functions-for-beginners-926947fc0cdc)
 * :scroll: [When (and why) you should use ES6 arrow functions — and when you shouldn’t — Cynthia Lee](https://medium.freecodecamp.org/when-and-why-you-should-use-es6-arrow-functions-and-when-you-shouldnt-3d851d7f0b26)
 * :scroll: [JavaScript — Learn & Understand Arrow Functions — Brandon Morelli](https://codeburst.io/javascript-learn-understand-arrow-functions-fe2083533946)
 * :scroll: [(JavaScript )=> Arrow functions — sigu](https://medium.com/podiihq/javascript-arrow-functions-27d4c3334b83)
 * :scroll: [A possibility to use Async/Await for filter(), find(), forEach(), map() and reduce() methods in Array — Ruwan Geeganage](https://www.linkedin.com/pulse/possibility-use-asyncawait-filter-find-foreach-map-reduce-geeganage/)
 * :scroll: [Javascript.reduce() — Paul Anderson](https://medium.com/@panderson.dev/javascript-reduce-79aab078da23)
 * :scroll: [Why you should replace forEach with map and filter in JavaScript — Roope Hakulinen](https://gofore.com/en/why-you-should-replace-foreach/)
 * :scroll: [Simplify your JavaScript – Use .map(), .reduce(), and .filter() — Etienne Talbot](https://medium.com/poka-techblog/simplify-your-javascript-use-map-reduce-and-filter-bd02c593cc2d)
 * :scroll: [JavaScript’s Reduce Method Explained By Going On a Diet — Kevin Kononenko](https://blog.codeanalogies.com/2018/07/24/javascripts-reduce-method-explained-by-going-on-a-diet/)

### Vidéos

 * :movie_camera: [Map, Filter and Reduce — Lydia Hallie](https://www.youtube.com/watch?v=UXiYii0Y7Nw)
 * :movie_camera: [Functional JavaScript: Map, forEach, Reduce, Filter — Theodore Anderson](https://www.youtube.com/watch?v=vytzLlY_wmU)
 * :movie_camera: [JavaScript Array superpowers: Map, Filter, Reduce (part I) — Michael Rosata](https://www.youtube.com/watch?v=qTeeVd8hOFY)
 * :movie_camera: [JavaScript Array superpowers: Map, Filter, Reduce (part 2) — Michael Rosata](https://www.youtube.com/watch?v=gIm9xLYudL0)
 * :movie_camera: [JavaScript Higher Order Functions - Filter, Map, Sort & Reduce — Epicop](https://www.youtube.com/watch?v=zYBeEPxNSbw)
 * :movie_camera: [[Array Methods 2/3] .filter + .map + .reduce — CodeWithNick](https://www.youtube.com/watch?v=4qWlqD0yYTU)
 * :movie_camera: [Arrow functions in JavaScript - What, Why and How — Fun Fun Function](https://www.youtube.com/watch?v=6sQDTgOqh-I)
 * :movie_camera: [Learning Functional Programming with JavaScript — Anjana Vakil - JSUnconf](https://www.youtube.com/watch?v=e-5obm1G_FY&t=1521s)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 20. Pure Functions, Side Effects and State Mutation

### Articles

 * :scroll: [Javascript and Functional Programming — Pure Functions — Omer Goldberg](https://hackernoon.com/javascript-and-functional-programming-pt-3-pure-functions-d572bb52e21c)
 * :scroll: [Master the JavaScript Interview: What is a Pure Function? — Eric Elliott](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976)
 * :scroll: [JavaScript: What Are Pure Functions And Why Use Them? — James Jeffery](https://medium.com/@jamesjefferyuk/javascript-what-are-pure-functions-4d4d5392d49c)
 * :scroll: [Pure functions in JavaScript — @nicoespeon](http://www.nicoespeon.com/en/2015/01/pure-functions-javascript/)
 * :scroll: [Functional Programming: Pure Functions — Arne Brasseur](https://www.sitepoint.com/functional-programming-pure-functions/)
 * :scroll: [Pure Functions In Javascript — Krunal](https://appdividend.com/2017/04/10/pure-functions-in-javascript/)
 * :scroll: [Making your JavaScript Pure — Jack Franklin](https://alistapart.com/article/making-your-javascript-pure)
 * :scroll: [To mutate, or not to mutate, in JavaScript](https://slemgrim.com/mutate-or-not-to-mutate/)
 * :scroll: [Arrays, Objects and Mutations — Federico Knüssel](https://medium.com/@fknussel/arrays-objects-and-mutations-6b23348b54aa)
 * :scroll: [The State of Immutability — Maciej Sikora](https://medium.com/dailyjs/the-state-of-immutability-169d2cd11310)
 * :scroll: [How to deal with dirty side effects in your pure functional JavaScript — James Sinclair](https://jrsinclair.com/articles/2018/how-to-deal-with-dirty-side-effects-in-your-pure-functional-javascript/)
 * :scroll: [Preventing Side Effects in JavaScript — David Walsh](https://davidwalsh.name/preventing-sideeffects-javascript)
 * :scroll: [Wielding Pure Functions in JavaScript and Function Composition — Peleke Sengstacke
](https://scotch.io/tutorials/wielding-pure-functions-in-javascript-and-function-composition)
 * :scroll: [JavaScript: Pure Functions — William S. Vincent](https://wsvincent.com/javascript-pure-functions/)
 * :scroll: [Functional programming paradigms in modern JavaScript: Pure functions — Alexander Kondov](https://hackernoon.com/functional-programming-paradigms-in-modern-javascript-pure-functions-797d9abbee1)

### Vidéos

 * :movie_camera: [Pure Functions — Hexlet](https://www.youtube.com/watch?v=dZ41D6LDSBg)
 * :movie_camera: [Pure Functions - Functional Programming in JavaScript — Paul McBride](https://www.youtube.com/watch?v=Jh_Uzqzz_wM)
 * :movie_camera: [JavaScript Pure Functions — Seth Alexander](https://www.youtube.com/watch?v=frT3H-eBmPc)
 * :movie_camera: [JavaScript Pure vs Impure Functions Explained — Theodore Anderson](https://www.youtube.com/watch?v=AHbRVJzpB54)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 21. Closures

### Articles

 * :scroll: [Closures — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
 * :scroll: [I never understood JavaScript closures — Olivier De Meulder](https://medium.com/dailyjs/i-never-understood-javascript-closures-9663703368e8)
 * :scroll: [Closure — JavaScript.Info](https://javascript.info/closure)
 * :scroll: [Understand JavaScript Closures With Ease — Richard Bovell](http://javascriptissexy.com/understand-javascript-closures-with-ease/)
 * :scroll: [Understanding JavaScript Closures — Codesmith](https://codeburst.io/understanding-javascript-closures-da6aab330302)
 * :scroll: [Understand Closures in JavaScript — Brandon Morelli](https://codeburst.io/understand-closures-in-javascript-d07852fa51e7)
 * :scroll: [A simple guide to help you understand closures in JavaScript — Prashant Ram](https://medium.freecodecamp.org/javascript-closures-simplified-d0d23fa06ba4)
 * :scroll: [Understanding JavaScript Closures: A Practical Approach — Paul Upendo](https://scotch.io/tutorials/understanding-javascript-closures-a-practical-approach)
 * :scroll: [Understanding JavaScript: Closures — Alexander Kondov](https://hackernoon.com/understanding-javascript-closures-4188edf5ea1b)
 * :scroll: [How to use JavaScript closures with confidence — Léna Faure](https://hackernoon.com/how-to-use-javascript-closures-with-confidence-85cd1f841a6b)
 * :scroll: [JavaScript closures by example — tyler](https://howchoo.com/g/mge2mji2mtq/javascript-closures-by-example)
 * :scroll: [JavaScript — Closures and Scope — Alex Aitken](https://codeburst.io/javascript-closures-and-scope-3784c75b9290)
 * :scroll: [Discover the power of closures in JavaScript — Cristi Salcescu](https://medium.freecodecamp.org/discover-the-power-of-closures-in-javascript-5c472a7765d7)
 * :scroll: [Simplified JavaScript: Getting Started with Closures — Code Like A Girl](https://code.likeagirl.io/simplified-javascript-getting-started-with-closures-f40f65317d00)
 * :scroll: [The Ultimate Guide to Hoisting, Scopes, and Closures in JavaScript — Tyler McGinnis](https://tylermcginnis.com/ultimate-guide-to-execution-contexts-hoisting-scopes-and-closures-in-javascript/)

### Vidéos

 * :movie_camera: [Javascript Closure — techsith](https://www.youtube.com/watch?v=71AtaJpJHw0)
 * :movie_camera: [Closures — Fun Fun Function](https://www.youtube.com/watch?v=CQqwU2Ixu-U)
 * :movie_camera: [Closures in JavaScript — techsith](https://www.youtube.com/watch?v=-xqJo5VRP4A)
 * :movie_camera: [JavaScript Closures 101: What is a closure? — JavaScript Tutorials](https://www.youtube.com/watch?v=yiEeiMN2Khs)
 * :movie_camera: [Closures — freeCodeCamp](https://www.youtube.com/watch?v=1JsJx1x35c0)
 * :movie_camera: [JavaScript Closures — CodeWorkr](https://www.youtube.com/watch?v=-rLrGAXK8WE)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 22. High Order Functions

### Articles

 * :scroll: [Higher-Order Functions — Eloquent JavaScript [Book]](https://eloquentjavascript.net/05_higher_order.html)
 * :scroll: [Higher-Order Functions in JavaScript — M. David Green](https://www.sitepoint.com/higher-order-functions-javascript/)
 * :scroll: [Higher Order Functions: Using Filter, Map and Reduce for More Maintainable Code — Guido Schmitz](https://medium.freecodecamp.org/higher-order-functions-in-javascript-d9101f9cf528)
 * :scroll: [First-class and Higher Order Functions: Effective Functional JavaScript — Hugo Di Francesco](https://hackernoon.com/effective-functional-javascript-first-class-and-higher-order-functions-713fde8df50a)
 * :scroll: [Higher Order Functions in JavaScript — John Hannah](https://www.lullabot.com/articles/higher-order-functions-in-javascript)
 * :scroll: [Higher-order Functions — Richard Bovell](http://javascriptissexy.com/tag/higher-order-functions/)
 * :scroll: [Higher Order Functions in JavaScript — Zsolt Nagy](http://www.zsoltnagy.eu/higher-order-functions-in-javascript/)
 * :scroll: [Fun With Higher Order Functions In JavaScript — Derick](https://derickbailey.com/2015/10/21/fun-with-higher-order-functions-in-javascript/)
 * :scroll: [Just a reminder on how to use high order functions — Pedro Filho](https://github.com/pedroapfilho/high-order-functions)
 * :scroll: [Understanding Higher-Order Functions in JavaScript — Sukhjinder Arora](https://blog.bitsrc.io/understanding-higher-order-functions-in-javascript-75461803bad)

### Vidéos

 * :movie_camera: [JavaScript Higher Order Functions & Arrays — Traversy Media](https://www.youtube.com/watch?v=rRgD1yVwIvE)
 * :movie_camera: [Higher Order Functions — Fun Fun Function](https://www.youtube.com/watch?v=BMUiFMZr7vk)
 * :movie_camera: [Higher Order Functions in Javascript — Raja Yogan](https://www.youtube.com/watch?v=dTlpYnmBW9I)
 * :movie_camera: [Higher Order Iterators in JavaScript — Fun Fun Function](https://www.youtube.com/watch?v=GYRMNp1SKXA)
 * :movie_camera: [Higher Order Functions in JavaScript — The Coding Train](https://www.youtube.com/watch?v=H4awPsyugS0)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 23. Recursion

### Articles

 * :scroll: [Recursion in JavaScript — Kevin Ennis](https://medium.freecodecamp.org/recursion-in-javascript-1608032c7a1f)
 * :scroll: [Understanding Recursion in JavaScript — Zak Frisch](https://medium.com/@zfrisch/understanding-recursion-in-javascript-992e96449e03)
 * :scroll: [Learn and Understand Recursion in JavaScript — Brandon Morelli](https://codeburst.io/learn-and-understand-recursion-in-javascript-b588218e87ea)
 * :scroll: [Recursion in Functional JavaScript — M. David Green](https://www.sitepoint.com/recursion-functional-javascript/)
 * :scroll: [Programming with JS: Recursion — Alexander Kondov](https://hackernoon.com/programming-with-js-recursion-31371e2bf808)
 * :scroll: [Anonymous Recursion in JavaScript — simo](https://dev.to/simov/anonymous-recursion-in-javascript)
 * :scroll: [Recursion, iteration and tail calls in JS — loverajoel](http://www.jstips.co/en/javascript/recursion-iteration-and-tail-calls-in-js/)
 * :scroll: [Understanding Recursion in JavaScript with Confidence — Jay](https://www.thecodingdelight.com/understanding-recursion-javascript/)

### Vidéos

 * :movie_camera: [Recursion In JavaScript — techsith](https://www.youtube.com/watch?v=VtG0WAUvq2w)
 * :movie_camera: [Recursion — Fun Fun Function](https://www.youtube.com/watch?v=k7-N8R0-KY4)
 * :movie_camera: [Recursion and Recursive Functions — Hexlet](https://www.youtube.com/watch?v=vLhHyGTkjCs)
 * :movie_camera: [Recursion: Recursion() — JS Monthly — Lucas da Costa](https://www.youtube.com/watch?v=kGXVsd8pBLw)
 * :movie_camera: [Recursive Function in JavaScript — kudvenkat](https://www.youtube.com/watch?v=uyjsR9eNTIw)
 * :movie_camera: [What on Earth is Recursion? — Computerphile](https://www.youtube.com/watch?v=Mv9NEXX1VHc)
 * :movie_camera: [Javascript Tutorial 34: Introduction To Recursion — codedamn](https://www.youtube.com/watch?v=9NO5dXSlbv8)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 24. Collections and Generators

### Articles

 * :scroll: [ES6 In Depth: Collections — Jason Orendorff](https://hacks.mozilla.org/2015/06/es6-in-depth-collections/)
 * :scroll: [ES6 Collections: Using Map, Set, WeakMap, WeakSet — Kyle Pennell](https://www.sitepoint.com/es6-collections-map-set-weakmap-weakset/)
 * :scroll: [ES6 WeakMaps, Sets, and WeakSets in Depth — Nicolás Bevacqua](https://ponyfoo.com/articles/es6-weakmaps-sets-and-weaksets-in-depth)
 * :scroll: [Introduction to Sets in JavaScript — Alligator.io](https://alligator.io/js/sets-introduction/)
 * :scroll: [Introduction to Maps in JavaScript — Alligator.io](https://alligator.io/js/maps-introduction/)
 * :scroll: [Map, Set, WeakMap and WeakSet — JavaScript.Info](https://javascript.info/map-set-weakmap-weakset)
 * :scroll: [Maps in ES6 - A Quick Guide — Ben Mildren](https://dev.to/mildrenben/maps-in-es6---a-quick-guide-35pk)
 * :scroll: [ES6 — Set vs Array — What and when? — Maya Shavin](https://medium.com/front-end-hacking/es6-set-vs-array-what-and-when-efc055655e1a)
 * :scroll: [ES6 — Map vs Object — What and when? — Maya Shavin](https://medium.com/front-end-hacking/es6-map-vs-object-what-and-when-b80621932373)
 * :scroll: [ES6: Working with Sets in JavaScript — Dead Code Rising](http://www.deadcoderising.com/es6-working-with-sets-in-javascript/)
 * :scroll: [Array vs Set vs Map vs Object — Real-time use cases in Javascript (ES6/ES7) — Rajesh Babu](https://codeburst.io/array-vs-set-vs-map-vs-object-real-time-use-cases-in-javascript-es6-47ee3295329b)
 * :scroll: [How to create an array of unique values in JavaScript using Sets — Claire Parker-Jones](https://dev.to/claireparker/how-to-create-an-array-of-unique-values-in-javascript-using-sets-5dg6)
 * :scroll: [What You Should Know About ES6 Maps — Just Chris](https://hackernoon.com/what-you-should-know-about-es6-maps-dc66af6b9a1e)
 * :scroll: [ES6 Maps in Depth — Nicolás Bevacqua](https://ponyfoo.com/articles/es6-maps-in-depth)
 * :scroll: [Generator — MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator)
* :scroll: [What are JavaScript Generators and how to use them — Vladislav Stepanov](https://codeburst.io/what-are-javascript-generators-and-how-to-use-them-c6f2713fd12e)
* :scroll: [Understanding JavaScript Generators With Examples  — Arfat Salman](https://codeburst.io/understanding-generators-in-es6-javascript-with-examples-6728834016d5)
* :scroll: [The Basics of ES6 Generators — Kyle Simpson](https://davidwalsh.name/es6-generators)

### Vidéos

 * :movie_camera: [JavaScript ES6 / ES2015 Set, Map, WeakSet and WeakMap — Traversy Media](https://www.youtube.com/watch?v=ycohYSx5h9w)
 * :movie_camera: [The Differences between ES6 Maps and Sets — Steve Griffith](https://www.youtube.com/watch?v=m4abICrldQI)
 * :movie_camera: [Javascript Generators - THEY CHANGE EVERYTHING - ES6 Generators Harmony Generators — LearnCode.academy](https://www.youtube.com/watch?v=QO07THdLWQo)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 25. Promises

### Articles

 * :scroll: [Promise — MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
 * :scroll: [JavaScript Promises for Dummies ― Jecelyn Yeen](https://scotch.io/tutorials/javascript-promises-for-dummies)
 * :scroll: [Understanding promises in JavaScript — Gokul N K](https://hackernoon.com/understanding-promises-in-javascript-13d99df067c1)
 * :scroll: [Master the JavaScript Interview: What is a Promise? — Eric Elliott](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)
 * :scroll: [An Overview of JavaScript Promises — Sandeep Panda](https://www.sitepoint.com/overview-javascript-promises/)
 * :scroll: [How to use Promises in JavaScript — Prashant Ram](https://medium.freecodecamp.org/promises-in-javascript-explained-277b98850de)
 * :scroll: [Implementing Promises In JavaScript — Maciej Cieslar](https://medium.freecodecamp.org/how-to-implement-promises-in-javascript-1ce2680a7f51)
 * :scroll: [JavaScript: Promises explained with simple real life analogies — Shruti Kapoor](https://codeburst.io/javascript-promises-explained-with-simple-real-life-analogies-dd6908092138)
 * :scroll: [Promises for Asynchronous Programming — Exploring JS](http://exploringjs.com/es6/ch_promises.html)
 * :scroll: [JavaScript Promises Explained By Gambling At A Casino — Kevin Kononenko](https://blog.codeanalogies.com/2018/08/26/javascript-promises-explained-by-gambling-at-a-casino/)
 * :scroll: [ES6 Promises: Patterns and Anti-Patterns — Bobby Brennan](https://medium.com/datafire-io/es6-promises-patterns-and-anti-patterns-bbb21a5d0918)
 * :scroll: [A Simple Guide to ES6 Promises — Brandon Morelli](https://codeburst.io/a-simple-guide-to-es6-promises-d71bacd2e13a)
 * :scroll: [The ES6 Promises — Manoj Singh Negi](https://codeburst.io/the-es6-promises-87a979ab27e4)
 * :scroll: [ES6 Promises in Depth — Nicolás Bevacqua](https://ponyfoo.com/articles/es6-promises-in-depth)
 * :scroll: [Playing with Javascript Promises: A Comprehensive Approach — Rajesh Babu](https://codeburst.io/playing-with-javascript-promises-a-comprehensive-approach-25ab752c78c3)

### Vidéos

 * :movie_camera: [Let's Learn ES6 - Promises — Ryan Christiani](https://www.youtube.com/watch?v=vQ3MoXnKfuQ)
 * :movie_camera: [JavaScript ES6 / ES2015 Promises — Traversy Media](https://www.youtube.com/watch?v=XJEHuBZQ5dU)
 * :movie_camera: [Promises — Fun Fun Function](https://www.youtube.com/watch?v=2d7s3spWAzo)
 * :movie_camera: [Error Handling Promises in JavaScript — Fun Fun Function](https://www.youtube.com/watch?v=f8IgdnYIwOU)
 * :movie_camera: [Promises Part 1 - Topics of JavaScript/ES6 — The Coding Train](https://www.youtube.com/watch?v=QO4NXhWo_NM)
 
<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 26. async/await

### Articles

 * :scroll: [async/await — JavaScript.Info](https://javascript.info/async-await)
 * :scroll: [Understanding async/await in Javascript — Gokul N K](https://hackernoon.com/understanding-async-await-in-javascript-1d81bb079b2c)
 * :scroll: [Asynchronous Programming — Eloquent JavaScript](https://eloquentjavascript.net/11_async.html)
 * :scroll: [Exploring Async/Await Functions in JavaScript — Alligator.io](https://alligator.io/js/async-functions/)
 * :scroll: [Asynchronous Javascript using async/await — Joy Warugu](https://scotch.io/tutorials/asynchronous-javascript-using-async-await)
 * :scroll: [Modern Asynchronous JavaScript with async/await — Flavio Copes](https://flaviocopes.com/javascript-async-await/)
 * :scroll: [Asynchronous JavaScript: From Callback Hell to Async and Await — Demir Selmanovic](https://www.toptal.com/javascript/asynchronous-javascript-async-await-tutorial)
 * :scroll: [Javascript — ES8 Introducing async/await Functions — Ben Garrison](https://medium.com/@_bengarrison/javascript-es8-introducing-async-await-functions-7a471ec7de8a)
 * :scroll: [How to escape async/await hell — Aditya Agarwal](https://medium.freecodecamp.org/avoiding-the-async-await-hell-c77a0fb71c4c)
 * :scroll: [Understanding JavaScript’s async await — Nicolás Bevacqua](https://ponyfoo.com/articles/understanding-javascript-async-await)
 * :scroll: [JavaScript Async/Await: Serial, Parallel and Complex Flow — TechBrij](https://techbrij.com/javascript-async-await-parallel-sequence)
 * :scroll: [Asynchronous Programming — Exploring JS](http://exploringjs.com/es6/ch_async.html)
 * :scroll: [From JavaScript Promises to Async/Await: why bother? — Chris Nwamba](https://blog.pusher.com/promises-async-await/)
 * :scroll: [Flow Control in Modern JS: Callbacks to Promises to Async/Await — Craig Buckler](https://www.sitepoint.com/flow-control-callbacks-promises-async-await/)
 * :scroll: [JavaScript: Promises and Why Async/Await Wins the Battle — Nick Parsons](https://dzone.com/articles/javascript-promises-and-why-asyncawait-wins-the-ba)

### Vidéos

 * :movie_camera: [Async + Await — Wes Bos](https://www.youtube.com/watch?v=9YkUCxvaLEk)
 * :movie_camera: [Asynchrony: Under the Hood — Shelley Vohr](https://www.youtube.com/watch?v=SrNQS8J67zc)
 * :movie_camera: [async/await in JavaScript - What, Why and How — Fun Fun Function](https://www.youtube.com/watch?v=568g8hxJJp4&index=3&list=PL0zVEGEvSaeHJppaRLrqjeTPnCH6)
 * :movie_camera: [async/await Part 1 - Topics of JavaScript/ES8 — The Coding Train](https://www.youtube.com/watch?v=XO77Fib9tSI&index=3&list=PLRqwX-V7Uu6bKLPQvPRNNE65kBL62mVfx)
 * :movie_camera: [async/await Part 2 - Topics of JavaScript/ES8 — The Coding Train](https://www.youtube.com/watch?v=chavThlNz3s&index=4&list=PLRqwX-V7Uu6bKLPQvPRNNE65kBL62mVfx)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 27. Data Structures

### Articles

 * :scroll: [Data Structures in JavaScript — Thon Ly](https://medium.com/siliconwat/data-structures-in-javascript-1b9aed0ea17c)
 * :scroll: [Algorithms and Data Structures in JavaScript — Oleksii Trekhleb](https://itnext.io/algorithms-and-data-structures-in-javascript-a71548f902cb)
 * :scroll: [Data Structures: Objects and Arrays ― Chris Nwamba](https://scotch.io/courses/10-need-to-know-javascript-concepts/data-structures-objects-and-arrays)
 * :scroll: [Data structures in JavaScript — Benoit Vallon](http://blog.benoitvallon.com/data-structures-in-javascript/data-structures-in-javascript/)
 * :scroll: [Playing with Data Structures in Javascript — Anish K.](https://blog.cloudboost.io/playing-with-data-structures-in-javascript-stack-a55ebe50f29d)
 * :scroll: [The Little Guide of Queue in JavaScript — Germán Cutraro](https://hackernoon.com/the-little-guide-of-queue-in-javascript-4f67e79260d9)
 * :scroll: [All algorithms writing with JavaScript in the book 'Algorithms Fourth Edition'](https://github.com/barretlee/algorithms)
 * :scroll: [Collection of classic computer science paradigms in JavaScript](https://github.com/nzakas/computer-science-in-javascript)
 * :scroll: [All the things you didn't know you wanted to know about data structures](https://github.com/jamiebuilds/itsy-bitsy-data-structures)

### Vidéos

 * :movie_camera: [Algorithms in JavaScript — Seth Koch](https://www.youtube.com/watch?v=PylQlISSH8U&list=PLujX4CIdBGCa-65N3uN8CDbUMrYsHBrz-)
 * :movie_camera: [Algorithms In Javascript | Ace Your Interview — Eduonix Learning Solutions](https://www.youtube.com/watch?v=H_EBPZgiAas&list=PLDmvslp_VR0zYUSth_8O69p4_cmvZEgLa)
 * :movie_camera: [Data Structures and Algorithms in JavaScript — freeCodeCamp](https://www.youtube.com/watch?v=Gj5qBheGOEo&list=PLWKjhJtqVAbkso-IbgiiP48n-O-JQA9PJ)
 * :movie_camera: [Learning JavaScript Data Structures and Algorithms: Sorting — Packt Video](https://www.youtube.com/watch?v=Ymh_AurrMbA)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 28. Expensive Operation and Big O Notation

### Articles

 * :scroll: [Big O Notation in Javascript — César Antón Dorantes](https://medium.com/cesars-tech-insights/big-o-notation-javascript-25c79f50b19b)
 * :scroll: [Time Complexity/Big O Notation — Tim Roberts](https://medium.com/javascript-scene/time-complexity-big-o-notation-1a4310c3ee4b)
 * :scroll: [Big O in JavaScript — Gabriela Medina](https://medium.com/@gmedina229/big-o-in-javascript-36ff67766051)
 * :scroll: [Big O Search Algorithms in JavaScript — Bradley Braithwaite](http://www.bradoncode.com/blog/2012/04/big-o-algorithm-examples-in-javascript.html)
 * :scroll: [Time Complexity Analysis in JavaScript — Jennifer Bland](https://www.jenniferbland.com/time-complexity-analysis-in-javascript/)
 * :scroll: [Algorithms in plain English: time complexity and Big-O Notation — Michael Olorunnisola](https://medium.freecodecamp.org/time-is-complex-but-priceless-f0abd015063c)

### Vidéos

 * :movie_camera: [JavaScript: Intro to Big O Notation and Function Runtime — Eric Traub](https://www.youtube.com/watch?v=HgA5VOFan5E)
 * :movie_camera: [Essential Big O for JavaScript Developers — Dave Smith](https://www.youtube.com/watch?v=KatlvCFHPRo)
 * :movie_camera: [Big O Notation - Time Complexity Analysis — WebTunings](https://www.youtube.com/watch?v=ALl86xJiTD8)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 29. Algorithms

### Articles

 * :scroll: [Data Structures and Algorithms using ES6](https://github.com/Crizstian/data-structure-and-algorithms-with-ES6)
 * :scroll: [Algorithms and data structures implemented in JavaScript with explanations and links to further readings](https://github.com/trekhleb/javascript-algorithms)
 * :scroll: [JS: Interview Algorithm](http://www.thatjsdude.com/interview/js1.html)
 * :scroll: [Algorithms in JavaScript — Thon Ly](https://medium.com/siliconwat/algorithms-in-javascript-b0bed68f4038)
 * :scroll: [JavaScript Objects, Square Brackets and Algorithms — Dmitri Grabov](https://medium.freecodecamp.org/javascript-objects-square-brackets-and-algorithms-e9a2916dc158)
 * :scroll: [Atwood's Law applied to CS101 - Classic algorithms and data structures implemented in JavaScript](https://github.com/felipernb/algorithms.js)
 * :scroll: [Data Structures and Algorithms library in JavaScript](https://github.com/yangshun/lago)
 * :scroll: [Collection of computer science algorithms and data structures written in JavaScript](https://github.com/idosela/algorithms-in-javascript)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 30. Inheritance, Polymorphism and Code Reuse

### Articles

 * :scroll: [Class inheritance, super — JavaScript.Info](https://javascript.info/class-inheritance)
 * :scroll: [Inheritance in JavaScript — MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Inheritance)
 * :scroll: [Inheritance in JavaScript — Rupesh Mishra](https://hackernoon.com/inheritance-in-javascript-21d2b82ffa6f)
 * :scroll: [Simple Inheritance with JavaScript — David Catuhe](https://www.sitepoint.com/simple-inheritance-javascript/)
 * :scroll: [JavaScript — Inheritance, delegation patterns and Object linking — NC Patro](https://codeburst.io/javascript-inheritance-25fe61ab9f85)
 * :scroll: [Object Oriented JavaScript: Polymorphism with examples — Knoldus Blogs](https://blog.knoldus.com/object-oriented-javascript-polymorphism-with-examples/)
 * :scroll: [Program Like Proteus — A beginner’s guide to polymorphism in Javascript — Sam Galson](https://medium.com/yld-engineering-blog/program-like-proteus-a-beginners-guide-to-polymorphism-in-javascript-867bea7c8be2)
 * :scroll: [Object-oriented JavaScript: A Deep Dive into ES6 Classes — Jeff Mott](https://www.sitepoint.com/object-oriented-javascript-deep-dive-es6-classes/)

### Vidéos

 * :movie_camera: [Inheritance in JavaScript — kudvenkat](https://www.youtube.com/watch?v=yXlFR81tDBM)
 * :movie_camera: [JavaScript ES6 Classes and Inheritance — Traversy Media](https://www.youtube.com/watch?v=RBLIm5LMrmc)
 * :movie_camera: [Polymorphism in JavaScript — kudvenkat](https://www.youtube.com/watch?v=zdovG9cuEBA)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 31. Design Patterns

### Articles

 * :scroll: [4 JavaScript Design Patterns You Should Know — Devan Patel](https://scotch.io/bar-talk/4-javascript-design-patterns-you-should-know)
 * :scroll: [JavaScript Design Patterns – Beginner's Guide to Mobile Web Development — Soumyajit Pathak](https://medium.com/beginners-guide-to-mobile-web-development/javascript-design-patterns-25f0faaaa15)
 * :scroll: [JavaScript Design Patterns — Akash Pal](https://medium.com/front-end-hacking/javascript-design-patterns-ed9d4c144c81)
 * :scroll: [Javascript Design Patterns: What They Are & How To Use Them — Patrick Simpson](https://seesparkbox.com/foundry/javascript_design_patterns)
 * :scroll: [JavaScript Design Patterns: Understanding Design Patterns in JavaScript - Sukhjinder Arora](https://blog.bitsrc.io/understanding-design-patterns-in-javascript-13345223f2dd)
 * :scroll: [All the 23 (GoF) design patterns implemented in Javascript — Felipe Beline](https://github.com/fbeline/Design-Patterns-JS)
 * :scroll: [Learning JavaScript Design Patterns — Addy Osmani ](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)

### Vidéos

 * :movie_camera: [JavaScript Design Patterns — Udacity](https://www.udacity.com/course/javascript-design-patterns--ud989)
 * :movie_camera: [JavaScript Patterns for 2017 — Scott Allen](https://www.youtube.com/watch?v=hO7mzO83N1Q)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 32. Partial Applications, Currying, Compose and Pipe

### Articles

 * :scroll: [Use function composition in JavaScript — Rémi](https://www.codementor.io/michelre/use-function-composition-in-javascript-gkmxos5mj)
 * :scroll: [Currying in JavaScript ES6 — Adam Bene](https://blog.benestudio.co/currying-in-javascript-es6-540d2ad09400)
 * :scroll: [Composition and Currying Elegance in JavaScript — Pragyan Das](https://medium.com/@pragyan88/writing-middleware-composition-and-currying-elegance-in-javascript-8b15c98a541b)
 * :scroll: [Functional JavaScript: Function Composition For Every Day Use — Joel Thoms](https://hackernoon.com/javascript-functional-composition-for-every-day-use-22421ef65a10)
 * :scroll: [Functional Composition: compose() and pipe() — Anton Paras](https://medium.com/@acparas/what-i-learned-today-july-2-2017-ab9a46dbf85f)
 * :scroll: [Why The Hipsters Compose Everything: Functional Composing In JavaScript — A. Sharif](http://busypeoples.github.io/post/functional-composing-javascript/)
 * :scroll: [A Gentle Introduction to Functional JavaScript pt III: Functions for making functions — James Sinclair](https://jrsinclair.com/articles/2016/gentle-introduction-to-functional-javascript-functions/)
 * :scroll: [Curry And Compose (why you should be using something like ramda in your code) — jsanchesleao](https://jsleao.wordpress.com/2015/02/22/curry-and-compose-why-you-should-be-using-something-like-ramda-in-your-code/)
 * :scroll: [Function Composition in JavaScript with Pipe — Andy Van Slaars](https://vanslaars.io/post/create-pipe-function/)
 * :scroll: [Practical Functional JavaScript with Ramda — Andrew D'Amelio, Yuri Takhteyev](https://developer.telerik.com/featured/practical-functional-javascript-ramda/)
 * :scroll: [The beauty in Partial Application, Currying, and Function Composition — Joel Thoms](https://hackernoon.com/the-beauty-in-partial-application-currying-and-function-composition-d885bdf0d574)
 * :scroll: [Curry or Partial Application? — Eric Elliott](https://medium.com/javascript-scene/curry-or-partial-application-8150044c78b8)
 * :scroll: [Partial Application in JavaScript — Ben Alman](http://benalman.com/news/2012/09/partial-application-in-javascript/)
 * :scroll: [Partial Application of Functions — Functional Reactive Ninja](https://hackernoon.com/partial-application-of-functions-dbe7d9b80760)
 * :scroll: [Currying vs Partial Application — Deepak Gupta](https://codeburst.io/javascript-currying-vs-partial-application-4db5b2442be8)
 * :scroll: [Partial Application in ECMAScript 2015 — Ragan Wald](http://raganwald.com/2015/04/01/partial-application.html)
 * :scroll: [Functional Composition in Javascript — Joe Cortopassi](https://joecortopassi.com/articles/functional-composition-in-javascript/)
 * :scroll: [So You Want to be a Functional Programmer pt. I — Charles Scalfani](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-1-1f15e387e536)
 * :scroll: [So You Want to be a Functional Programmer pt. II — Charles Scalfani](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-2-7005682cec4a)
 * :scroll: [So You Want to be a Functional Programmer pt. III — Charles Scalfani](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-3-1b0fd14eb1a7)
 * :scroll: [So You Want to be a Functional Programmer pt. IV — Charles Scalfani](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-4-18fbe3ea9e49)
 * :scroll: [So You Want to be a Functional Programmer pt. V — Charles Scalfani](https://medium.com/@cscalfani/so-you-want-to-be-a-functional-programmer-part-5-c70adc9cf56a)
 * :scroll: [Functional-Light JavaScript Chapter 3: Managing Function Inputs — Kyle Simpson](https://github.com/getify/Functional-Light-JS/blob/master/manuscript/ch3.md)
 * :scroll: [An introduction to the basic principles of Functional Programming — TK](https://medium.freecodecamp.org/an-introduction-to-the-basic-principles-of-functional-programming-a2c2a15c84)
 * :scroll: [Concepts of Functional Programming in Javascript — TK](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

### Vidéos

 * :movie_camera: [Compose vs Pipe: Functional Programming in JavaScript — Chyld Studios](https://www.youtube.com/watch?v=Wl2ejJOqHUU)
 * :movie_camera: [JavaScript Functional Programing: Compose — Theodore Anderson](https://www.youtube.com/watch?v=jigHxo9YR30)
 * :movie_camera: [Function Composition - Functional JavaScript — NWCalvank](https://www.youtube.com/watch?v=mth5WpEc4Qs)
 * :movie_camera: [JavaScript Function Composition Explained — Theodore Anderson](https://www.youtube.com/watch?v=Uam37AlzPYw)
 * :movie_camera: [Let's code with function composition — Fun Fun Function](https://www.youtube.com/watch?v=VGB9HbL1GHk)
 * :movie_camera: [Partial Application vs. Currying — NWCalvank](https://www.youtube.com/watch?v=DzLkRsUN2vE)
 * :movie_camera: [JavaScript Partial Application — Theodore Anderson](https://www.youtube.com/watch?v=jkebgHEcvac)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>

---

## 33. Clean Code

### Articles

 * :scroll: [Clean Code concepts adapted for JavaScript — Ryan McDermott](https://github.com/ryanmcdermott/clean-code-javascript)
 * :scroll: [JavaScript Clean Coding Best Practices — András Tóth](https://blog.risingstack.com/javascript-clean-coding-best-practices-node-js-at-scale/)
 * :scroll: [Function parameters in JavaScript Clean Code — Kevin Peters](https://medium.com/@kevin_peters/function-parameters-in-javascript-clean-code-4caac109159b)
 * :scroll: [Clean Code JavaScript — Sarah Drasner](https://css-tricks.com/clean-code-javascript/)
 * :scroll: [Keeping your code clean — Samuel James](https://codeburst.io/keeping-your-code-clean-d30bcffd1a10)
 * :scroll: [Best Practices for Using Modern JavaScript Syntax — M. David Green](https://www.sitepoint.com/modern-javascript-best-practices/)

### Vidéos
*  :movie_camera: [JavaScript Pro Tips - Code This, NOT That](https://www.youtube.com/watch?v=Mus_vwhTCq0)

<p align="center">
:arrow_up: <strong><a href="#table-des-matières">Table des matières</a></strong> :arrow_up:
</p>
