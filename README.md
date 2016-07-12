## Scope/purpose of training.
- Limit the recurring work with html developer.
- Limit the mistakes.
- Remove the blame game and work as team.
- learn Html / Css
- self training (http://www.w3schools.com/html/)


### Common mistake in html
-  Assuming that all the versions of HTML are the same(doctype).
-  Never forget to close a tag in HTML5 that requires to be closed.
-  Using Inline CSS 
-  Not writing Comments for html.
-  using Same Id for multiple elements
-  Indenting of code.
-  creating complicated element structure and css structure.
-  using table for every section.
-  using complicated class naming.

### What is HTML?
- HTML, HyperText Markup Language, gives content structure , for example, headings, paragraphs, or images
- we are using HTML5


### Document structure
	
	<!DOCTYPE html>
	   	<html>
	   	<head>
	   	  <meta charset="utf-8">
	   	  <meta name="viewport" content="width=device-width">
	   	  <title>JS Bin</title>
	   	</head>
	   	<body>
	
	</body>
	</html>

### Meta tag for responsive
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
### Render  site in IE
    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />
    - this will render ie browser to its latest.
> It forces the browser the render at whatever the most recent version's standards are. Just like using the latest version of jQuery on Google's CDN, this is the most recent, but also can potentially break your code since its not a fixed version.
[help Link](http://stackoverflow.com/questions/14611264/x-ua-compatible-content-ie-9-ie-8-ie-7-ie-edge)

### html5 for tag support for older browser.
<!--[if lte IE 8]><script src="assets/js/ie/html5shiv.js"></script><![endif]-->

### Modernizr for browser detection and its feature
https://modernizr.com/
- It adds classes indicating feature support, allowing you to apply different styling to elements depending on what features they support.
-  It allows you to run feature detection to decide whether to run a script/run a polyfill or not.
- It injects html5shiv, which allows old browsers to understand HTML5 elements.

> If you don't use any of these features, then there's no point in including Modernizr at all. If you only use it for the html5shiv then you could probably just include that instead to save a few bytes, although I doubt there's a relevant size difference at all.

    
### Understanding Common HTML Terms
	Elements :-  a, hr , h1 , h2
	Tags :- <a>...</a>
	Attributes: <a href="http://shayhowe.com/">Shay Howe</a>
--------------------
## Type of elements
### Self-Closing Elements
	area, base, br, col, embed, hr, img, input, 
	keygen, link, meta, param, source, track, wbr	

### Closing Elements
	
    <div></div>
   	<h1></h1>
   	<section></section>
   	<article></article>
   	
### Block Elements

	<div>
	<h1> <h6>
	<p>
	<ul>, <ol>, <dl>
	<li>, <dt>, <dd>
	<table>
	<blockquote>
	<pre>
	<form>

### Inline elements

	<span>
	<a>
	<strong>
	<em>
	<img />
	<br>
	<input>
------------------------------------

### common used elements
### dl list
	<dl>
	  <dt>study</dt>
	  <dd>The devotion of time </dd>
	  <dt>design</dt>
	  <dd>A plan or drawing produced</dd>
	</dl>

### navigation structure

	<nav class="nav">
	  <ul>
	    <li><a href="index.html">Home</a></li>
	    <li><a href="speakers.html">Speakers</a></li>
	    <li><a href="schedule.html">Schedule</a></li>
	    <li><a href="venue.html">Venue</a></li>
	  </ul>
	  </nav>

### table structure
    <table>
      <thead>
        <tr>
          <th>Element</th>
          <th>Empty</th>
          <th>Tag omission</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th><code>pre</code></th>
          <td>No</td>
          <td>Neither tag is omissible</td>
        </tr>
        <tr>
          <th><code>img</code></th>
          <td>Yes</td>
          <td>No end tag</td>
        </tr>
      </tbody>
    </table>
## Relative and Absolute Paths
### Relative Paths
    index.html
    /graphics/image.png
    /help/articles/how-do-i-set-up-a-webpage.html
### Absolute Paths
    http://www.mysite.com
    http://www.mysite.com/graphics/image.png
    http://www.mysite.com/help/articles/how-do-i-set-up-a-webpage.html

# New Semantic Elements in HTML5
    <article>
    <aside>
    <details>
    <figcaption>
    <figure>
    <footer>
    <header>
    <main>
    <mark>
    <nav>
    <section>
    <summary>
    <time>

![image](http://www.w3schools.com/html/img_sem_elements.gif)


# HTML Best Practices
### Don't use legacy or obsolete DOCTYPE

`DOCTYPE` is not for DTD anymore, be simple.

Bad:

    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
      "http://www.w3.org/TR/html4/strict.dtd">

Good:

    <!DOCTYPE html>
    
### Don't omit closing tag

Bad:

    <html>
      <body>
        ...

Good:

    <html>
      <body>
        ...
      </body>
    </html>

### Don't mix character cases

It gives a consistency also.

Bad:

    <a HREF="#general">General</A>

Good:

    <a href="#general">General</a>

### Don't mix quotation marks

Same as above.

Bad:

    <img alt="HTML Best Practices" src='/img/logo.jpg'>

Good:

    <img alt="HTML Best Practices" src="/img/logo.jpg">


### Add `lang` attribute

`lang` attribute will help translating an HTML document.

Bad:

    <html>

Good:

    <html lang="en-US">

### Add `title` element

A value for `title` element is used by various application not only a browser.

Bad:

    <head>
      <meta charset="UTF-8">
    </head>

Good:

    <head>
      <meta charset="UTF-8">
      <title>HTML Best Practices</title>
    </head>
### Specify MIME type of minor linked resources

This is a hint how application handles this resource.

Bad:

    <link href="/pdf" rel="alternate">
    <link href="/feed" rel="alternate">
    <link href="/css/screen.css" rel="stylesheet">

Good:

    <link href="/pdf" rel="alternate" type="application/pdf">
    <link href="/feed" rel="alternate" type="application/rss+xml">
    <link href="/css/screen.css" rel="stylesheet">
    
### Use `address` element only for contact information

`address` element is for email address, social network account, street address,
telephone number, or something you can get in touch with.

Bad:

    <address>No rights reserved.</address>

Good:

    <address>Contact: <a href="https://twitter.com/hail2u_">Kyo Nagashima</a></address>


### Write one list item per line

Looooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooong
line is hard toooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo read.

Bad:

    <ul>
      <li>General</li><li>The root Element</li><li>Sections</li>...
    </ul>

Good:

    <ul>
      <li>General</li>
      <li>The root Element</li>
      <li>Sections</li>
      ...
    </ul>
    
### Use `main` element

`main` element can be used wrapping contents.

Bad:

    <div id="content">
      ...
    </div>

Good:

    <main>
      ...
    </main>

### Avoid `div` element as much as possible

`div` element is an element of last resort.

Bad:

    <div class="chapter">
      ...
    </div>

Good:

    <section>
      ...
    </section
    
### Don't split same link that can be grouped

`a` element can wrap almost all elements (except interactive elements like form controls and `a` element itself).

Bad:

    <h1><a href="https://whatwg.org/">WHATWG</a></h1>
    
    <p><a href="https://whatwg.org/">A community maintaining and evolving HTML since 2004.</a></p>

Good:

    <a href="https://whatwg.org/">
      <h1>WHATWG</h1>
    
      <p>A community maintaining and evolving HTML since 2004.</p>
    </a>

### Use `download` attribute for downloading a resource

It will force browsers to download linked resource to the storage.

Bad:

    <a href="/downloads/offline.zip">offline version</a>

Good:

    <a download href="/downloads/offline.zip">offline version</a>

### Use `rel`, `hreflang`, and `type` attribute if needed

These hints helps applications how handle linked resource.

Bad:

    <a href="/ja/pdf">Japanese PDF version</a>

Good:

    <a href="/ja/pdf" hreflang="ja" rel="alternate" type="application/pdf">Japanese PDF version</a>
    
## Important Link
- [html5 structure outliner ](https://hoyois.github.io/html5outliner/)
- [schema rich snippets](https://www.youtube.com/watch?v=N2PjWtybDOs)
- [schema Genrator](http://schema-creator.org/)
- [W3C Validator](https://validator.w3.org/)
- [Html5 template Genrator](http://www.initializr.com/)
- [bootstrap snippets](http://bootsnipp.com/)
- [css tricks for html5](https://css-tricks.com/snippets/html/)









	





