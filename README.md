# About

This is a [plugin](https://github.com/hakimel/reveal.js/wiki/Plugins,-Tools-and-Hardware) for the [reveal.js HTML presentation framework](https://github.com/hakimel/reveal.js).

It uses the JavaScript library [Type.js](https://github.com/mattboldt/typed.js/) to create a typewriter effect.

# References
- [Hakim El Hattab](https://hakim.se/)
- [Matt Boltd](https://mattboldt.com/)

# Installation

Step 1 - In your .html file

Add the below code between the Section Tag and adjust the P tag to suit.
```
<section>
	<div id="typed-strings">
	<!-- enter custom text below here -->
	<h1>Reveal.js</h1>
	<h3>The HTML Presentation Framework</h3>
	<p>
		<small>Created by <a href="http://hakim.se">Hakim El Hattab</a> / <a href="http://twitter.com/hakimel">@hakimel</a></small>
	</p>
	<!-- enter custom text above here -->
	</div>
	<span id="typed"></span>
</section>
```
Step 2 - Dependencies

Add this code to your dependencies
```
{ src: 'plugin/typed/typed.js', async: false , callback: function() { callTypedJs(); }}
```
Step 3 - Plugin Folder

The Plugin folder should have a folder called Typed and the typed.js file inside. You can get type.js with 
```
npm i typed-js
```
# Enhancements
Add the Type.js configuration options under Reveal.initialize in the .html file. Right now, some custom settings have been used

# How it works
1. The script to setup and call Typed js was placed into the typed.js file itself. See plugin folder.

```function callTypedJs(){
	var typed = new Typed('#typed', {
		stringsElement: '#typed-strings',
		loop: true,
		startDelay: 500,
		typeSpeed: 50,
		backSpeed: 35
	});
}
```
# Licence
MIT licensed

Copyright (C) 2018 Peter Doherty <peter@computationhub.com>

# Star
Please star this repo!