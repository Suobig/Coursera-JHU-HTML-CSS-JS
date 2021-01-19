# Week 1

## Welcome

## Setup

## HTML Basics

### What is HTML

HTML - HyperText Markup Language

**Hypertext** - text that contains links to other text. Nowadays it's not just text, but Hypermedia

**Markup** - is annotation of the content that tells what that content is.

HTML is human readable. You don't need an interpreter to understand it.

**Language** means that there's syntax you need to follow.

There're 3 technologies that drive web.

* HTML provides the structure of the document *without* telling anything about how it visually looks or how it behaves
* CSS provides style of the document`
* Javascript provides behavior, functionality.

### HTML History

Before 1997 there were no standards. Around 1997 W3C created HTML4 standards. It was lose and it was implemented differently.

Around 2000 there was XHTML 1.0, based on XML.

In 2004 browser vendors created WHATWG: HTML group. They drived HTML5.0 movement.

In 2007 W3C and WHATWG started working together.

In 2011 they created HTML5.0

All major browsers are evergreen, they silently update themselves.

Resources

* [w3.org](www.w3.org)
* [Can I use](https://caniuse.com)
* [Validator](https://validator.w3.org)
* [Browser statistics](www.w3schools.com)

### Anatomy of HTML tag

Usually html tag has opening and closing tags with content inside. tag name is called an "element".

There're tags like `<br>` or `<hr>` that don't have closing tags.

tags can have attributes.

No space allowed bwetween opening bracket and element name, no space allowed between opening bracket and `/` in closing tag. At least 1 space must be between element name and attribute name.

Attribute value isn't required to have quotes, but it's best practice to put attribute values in quotes.

A tag that doesn't have any content may be self-closing tag: `<p/>`

But in HTML5 if a tag *can* contain content, it *must* have opening and closing tag.

### Basic HTML document structure

Declaration

    <!doctype html>

tells browser to be ready to render HTML document. There's no real purpose to this declaration right now, because there's only 1 HTML type. But you can't omit this declaration or the browser would think that your page doesn't follow html standards.

    <html>
    </html>

is used to indicate the body of html document

    <head>
    </head>

is used to provide some infromation about the page. For example it's always a good idea to provide information about charset:

    <meta charset="utf-8">

`<meta>` is a stand-alone tag, there's no closing tag.

    <title></title>

`title` tag is mandatory. Without it html would be invalid.

    <body>
    </body>

`body` is the root tag for all the page's content. It's oftened referred to as a *viewport*.

The browser always reads and interprets the document from top to bottom.

### HTML content models

Content model refers to default behavior the browser applies to the elements belonging to this content model and the nesting rules of those elements - which elements are allowed to be nested inside which other elements.

Before HTML5 elements where either *block* or *inline*. In HTML5 there're 7 models:

In traditional model:

* block-level elements
  * render to begin on a new line
  * may contain inline or block elements
  * roughtly HTML5 *Flow Content*
* inline elements
  * render on the same line
  * may only contain other inline elements
  * roughtly HTML5 *Phrasing Content*

## Essential HTML5 Tags

*Semantic* element means that an element has some inherint meaning by itself and implies something to it's content.

Semantic elements help machienes and humans to better understand their content and also *may* help search engine ranking, i.e. SEO.

### Headings

There're 6 different tags rankend by importance from `<h1>` - the most important - to `<h6>` the least important.

Even though default browser styles makes those elements render differently, this should now be used for styling.

`<h1>` element is very important for SEO and should convey the main topic of the document.

    <header>
        header element - Some header information goes here. Usually consists of company logo, some tag line, etc. Sometimes, navigation is contained in the header as well.
        <nav>nav (short for navigation) element - Usually contains links to different parts of the web site.</nav>
    </header>
    <h1>Main Heading of the Page (hard not to have it)</h1>
    <section>
        Section 1
        <article>Article 1</article>
        <article>Article 2</article>
        <article>Article 3</article>
    </section>
    <section>
        Section 2
        <article>Article 4</article>
        <article>Article 5</article>
        <article>Article 6</article>
        <div>Regular DIV element</div>
    </section>
    <aside>
        ASIDE - Some information that relates to the main topic, i.e., related posts.
    </aside>

    <footer>
        JHU Copyright 2015
    </footer>

### HTML Lists

`<ul>` - unordered lists
`<ol>` - ordered lists.

`<ul>` and `<ol>` tags can only contain `<li>` elements inside them, nothing else.

### HTML Character Entity Reference

We have a way to escape HTML characters. 3 characters should always be escaped by replacing them with entity references:

* `<` - use `&lt;`
* `>` - use `&gt;`
* `&` - use `&amp;`

Some other useful characters:

* `&copy;` - copyright symbol
* `&nbsp;` - non-breaking space. Don't use it to create multiple spaces. This should be done with CSS.
* `&quot;` - quote character. Can be used for the page display properly in different charsets.

### Creating links

#### Internal links

If we provide no directory information:

    <a href="same-directory.html" title="Same dir link">Link to a file in 
    the same directory</a>

    <a href="same-directory.html" title="Same dir link">
        <div>DIV ink to a file in the same directory</div>
    </a>

Interestingly, `<a>` tag is both Flow Content element (block element) and Phrase Content element (inline) depending on the content of the element itself.

#### External link

    <a href="http://www.facebook.com/CourseraWebDev" 
    target="_blank" title="Like Our Page!">Course Facebook Page</a>

Target attribute is usually used with external links.

#### Link same page

    <a href="#section1">#section1</a>

Other way is to have an `<a>` tag with the `"name"` attribute:

    <a name="section6">(#section6) Section 6</a>

You can send a link with section identifier.

Now they're even more useful because they're used in SPA (Single-Page Applications).

### Displaying Images

Dispaling images:

    <img src="picture-with-quote.jpg" width="400" height="235" alt="Picture with a quote">

It's always a good idea to include `width` and `height` elements. In this case a browser would reserve space for the image.

`<img>` is an inline element by default
