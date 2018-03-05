patternLock
===========

A light weight plugin to simulate android like pattern lock mechanism for your hybrid app or for a website. It's easy to configure and style so you can have different type of pattern lock according to your need. Is also provide some methods to use this plugin securely.
This repository includes implementations for both jQuery and AngularJS.

<strong>jQuery - How to use?</strong><br>
Include jquery and patternLock.js and patternLock.css to your page.
<pre class="brush: xml;">
&lt;link href=&quot;patternLock.css&quot;  rel=&quot;stylesheet&quot; type=&quot;text/css&quot; /&gt;
&lt;script src=&quot;jquery.js&quot;&gt;&lt;/script&gt;
&lt;script src=&quot;patternLock.js&quot;&gt;&lt;/script&gt;
</pre>
Than with simple initialization you have your pattern lock.
<pre class="brush: js;">
var lock = new PatternLock("#patternContainer");
</pre>
<br/>
<strong>AngularJS - How to use?</strong><br>
This implementation presents the pattern lock as an angular directive, `pattern-lock`. JQuery is not needed, the directive makes use of AngularJS's JQLite.
Include angularPatternLock.js and patternLock.css to your page.
<pre class="brush: xml;">
&lt;link href=&quot;patternLock.css&quot;  rel=&quot;stylesheet&quot; type=&quot;text/css&quot; /&gt;
&lt;script src=&quot;angularPatternLock.js&quot;&gt;&lt;/script&gt;
</pre>
Include the module `angular-pattern-lock` in your app and include the directive in your HTML. Your `on-init` function will receive the pattern lock object as `lock`. Add each option as an attribute.
<pre class="brush: js;">
<pattern-lock on-init="myLockInit(lock)" on-draw="myOnDraw" matrix="[4,4]"></pattern-lock>
</pre>
<br/>

Check demo and documentation on <a href="http://ignitersworld.com/lab/patternLock.html">http://ignitersworld.com/lab/patternLock.html</a>

<h3>Major updates</h3>

<strong>v1.0.2</strong>
- Added angular directive implementation.

<strong>v1.0.1</strong>
- Added a option to allow repeating over dots.
- Added on npm.
- Fixed setPattern bug for larger matrix.
- Fixed invalid pattern #15, #3
- Fixed direction classes issue while directly moving to non near dots.

<strong>v0.6.0</strong>
- UMD (AMD, CommonJS) support.

<strong>v0.5.0</strong>
- Added directional classes, dir, n,s,e,w,n-e,n-w,s-e,s-w.

<strong>v0.4.0</strong>
- Added setPattern, disable, enable methods.

<strong>v0.3.0</strong>
- Fixed patternlock support on devices having both mouse and touch input.
