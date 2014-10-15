---
layout: docs
navgroup: docs
navactive: docsjs
title: JavaScript

meta:
  description: Understand how we use Javascript in Kickoff

next:
 - title: Kickoff's CSS
   body: Find out how Kickoff's CSS works
   link: css.html
 - title: The Kickoff Grid
   body: Find out how the default Kickoff grid works
   link: grid.html
---

Kickoff has a very simple base JavaScript structure.

We appreciate that everyone has a preferred way of writing and structuring their JavaScript and so we have made it easy to get up and running, while also making it easy to switch out Kickoff’s JavaScript structure should you want to do something more complex.

While not included in the default Kickoff branch, Kickoff now includes a base setup for using Browserify.  This version of Kickoff is maintained in a separate branch, more information on which can be [found in the following documentation]().

## JavaScript Structure

As mentioned above, Kickoff’s JavaScript is very non prescriptive.  Here we look at how we structure Kickoff’s JavaScript by default as well as how this can be adapted for your own needs.

### script.js

This file can be used to contain or reference your site/app JavaScript code.

For larger projects, we recommend using [Browserify](#js-browserify) to manage your projects JavaScript dependencies.

By default, Kickoff defines all of it’s JavaScript in the `KO` namespace, but this can be changed to anything you like, perhaps the name of the project. We tend to use the [singleton pattern](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#singletonpatternjavascript).

### Folder Structure

Kickoff has a very simple folder structure for it’s JavaScript.

The **js/helpers** directory………

The **js/libs** directory…………

<a name="js-browserify"></a>
## Browserify

TO BE WRITTEN

<a name="js-bower"></a>
## Bower

Kickoff leverages Bower to manage the packages that………….

A few bower packages are included with Kickoff by default, these can be found by viewing the [bower.json file](https://github.com/tmwagency/kickoff/blob/master/bower.json):

* [Swiftclick](https://github.com/tmwagency/swiftclick) - Developed by our own Ivan Hayes, SwiftClick is a library created to eliminate the 300ms click event delay on touch devices.
* [Trak.js](https://github.com/tmwagency/trak.js) - Developed by our own Zander Martineau, trak.js is a universal analytics event tracking API
* [Cookies](https://github.com/ScottHamper/Cookies/) - Developed by Scott Hamper, Cookies is a great Cookie manipulation library

These packages aren’t hard dependencies and can be removed by removing them from the `config.js.fileList` [found in the grunt config](grunt.html#config-js).


## Shims

To manage JavaScript Shims, we use a Grunt plugin called [Shimly](https://github.com/nicbell/Shimly), created by  Nic Bell.  To find out more about Shimly, [check out our Grunt task documentation](grunt.html#task-shimly).


## Libraries

If you need to add any 3rd party library code, we suggest placing them in the [js/libs/](https://github.com/tmwagency/kickoff/tree/master/js/libs) folder. The latest jQuery and Modernizr libraries are included by default. You may wish to create your own [custom Modernizr build](http://www.modernizr.com/download/). Other recommended libraries include:

