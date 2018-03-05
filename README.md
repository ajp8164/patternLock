patternLock
===========

A light weight plugin to simulate android like pattern lock mechanism for your hybrid app or for a website. It's easy to configure and style so you can have different types of pattern lock according to your need.

This repository includes implementations for both jQuery and AngularJS.

##Use with jQuery

Include jquery and patternLock.js and patternLock.css in your page.

```sh
<link href="patternLock.css" rel="stylesheet" type="text/css" />
<script src="jquery.js"></script>
<script src="patternLock.js"><;/script>;
```

Include an identified HTML component in your page.

```sh
<div id="#patternContainer"></div>
```

Initialize pattern lock to obtain the object.

```sh
var lock = new PatternLock("#patternContainer");
```

##Use with AngularJS

This implementation presents the pattern lock as an angular directive, `<pattern-lock>`. JQuery is not needed, the directive makes use of AngularJS's JQLite.
Include angularPatternLock.js and patternLock.css to your page.

```sh
<link href="patternLock.css" rel="stylesheet" type="text/css" />
<script src="angularPatternLock.js"></script>
```

Include the module `angular-pattern-lock` in your app.

```sh
angular.module('myApp', ['angular-pattern-lock', ...]);
```

Include the directive in your HTML. Your `on-init` function will receive the pattern lock object as `lock`. Add each pattern lock option as an attribute.

```sh
<pattern-lock on-init="myLockInit(lock)" on-draw="myOnDraw" matrix="[4,4]"></pattern-lock>
```

In your controller create the callback for handling `on-init` and `on-draw` events.

```sh
var patternLock;
$scope.myLockInit = function(lock) {
	// lock is the pattern lock object on which methods may be called; e.g., lock.disable()
	patternLock = lock;
}

$scope.myOnDraw = function(pattern) {
	// pattern is the string value drawn
}
```

##Demo

Check the demo and documentation at <a href="http://ignitersworld.com/lab/patternLock.html">http://ignitersworld.com/lab/patternLock.html</a>

##Major updates

###v1.0.2
- Added angular directive implementation.

###v1.0.1
- Added a option to allow repeating over dots.
- Added on npm.
- Fixed setPattern bug for larger matrix.
- Fixed invalid pattern #15, #3
- Fixed direction classes issue while directly moving to non near dots.

###v0.6.0
- UMD (AMD, CommonJS) support.

###v0.5.0
- Added directional classes, dir, n,s,e,w,n-e,n-w,s-e,s-w.

###v0.4.0
- Added setPattern, disable, enable methods.

###v0.3.0
- Fixed patternlock support on devices having both mouse and touch input.
