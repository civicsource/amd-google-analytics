# Google Analytics AMD Loading

> AMD loading for google analytics that doesn't block the page waiting for the analytics.js script.

## Install with [Bower](http://bower.io/)

```
bower install amd-google-analytics --save
```

Then add `ga.js` to your project.

## How to Use

Require it like so:

```js
define(['ga'], function(ga) {
    ga('create', 'UA-********-*', 'example.com');
	ga('send', 'pageview');
})
```

## Advantages Over Similar Solutions

The `ga` function returned by the script is the same function you get when [loading the script manually with Google's recommended code](https://developers.google.com/analytics/devguides/collection/analyticsjs/). In fact, take a look at the source of [ga.js](ga.js) yourself and see that it is a one-for-one copy of that code. Thus, you still get the advantages of that script (e.g. the non-blocking loading of `analytics.js` from Google's servers) while still enjoying the benefits of using it via AMD.
