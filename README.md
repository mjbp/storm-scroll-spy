#Storm Scroll Spy

[![Build Status](https://travis-ci.org/mjbp/storm-scroll-spy.svg?branch=master)](https://travis-ci.org/mjbp/storm-scroll-spy)
[![codecov.io](http://codecov.io/github/mjbp/storm-scroll-spy/coverage.svg?branch=master)](http://codecov.io/github/mjbp/storm-scroll-spy?branch=master)
[![npm version](https://badge.fury.io/js/storm-scroll-spy.svg)](https://badge.fury.io/js/storm-scroll-spy)

Automated scroll position related navigation state management 

##Usage
HTML
```
<nav class="js-scroll-spy">
    <a href="#section1">Section 1</a>
    <a href="#section2">Section 2</a>
    <a href="#section3">Section 3</a>
</nav>
<section id="section1">
    ...
</section>
<section id="section2">
    ...
</section>
<section id="section3">
    ...
</section>
```

JS
```
npm i -S storm-scroll-spy
```
either using es6 import
```
import TabAccordion from 'storm-scroll-spy';

ScrollSpy.init('.js-scroll-spy');
```
aynchronous browser loading (use the .standalone version in the /dist folder)
```
import Load from 'storm-load';

Load('/content/js/async/storm-scroll-spyn.standalone.js')
    .then(() => {
        ScrollSpy.init('.js-scroll-spy');
    });
```
or es5 commonjs  (legacy, use the .standalone version in the /dist folder)
```
var ScrollSpy = require('./libs/storm-scroll-spy');

ScrollSpy.init('.js-scroll-spy');
```


##Example
[https://mjbp.github.io/storm-scroll-spy](https://mjbp.github.io/storm-scroll-spy)


##Options
```
    {
		offset: 0,
		activeClassName: 'active',
		callback: null
    }
```

e.g.
```
ScrollSpy.init('.js-scrollspy', {
		offset: 50%
});
```


##API
####`ScrollSpy.init(selector, opts)`
Initialise the module with a DOM selector and  options object


##Tests
```
npm run test
```

##Browser support
This is module has both es6 and es5 distributions. The es6 version should be used in a workflow that transpiles.

The es5 version depends unpon Object.assign, element.classList, and Promises so all evergreen browsers are supported out of the box, ie9+ is supported with polyfills. ie8+ will work with even more polyfils for Array functions and eventListeners.

##Dependencies
None

##License
MIT

##Credits
Adapted from an initial fork of cferdinandi's gumshoe