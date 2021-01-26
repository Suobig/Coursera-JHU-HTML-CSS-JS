# Week 2

- [Cascading Style Sheets Basics](#cascading-style-sheets-basics)
  - [Power of CSS](#power-of-css)
  - [Anatomy of a CSS Rule](#anatomy-of-a-css-rule)
  - [Element, Class and ID selector](#element-class-and-id-selector)
  - [Combining Selectors](#combining-selectors)
  - [Pseudo-Class Selectors](#pseudo-class-selectors)
- [CSS Rules COnflinct Resolution and Text Styling](#css-rules-conflinct-resolution-and-text-styling)
  - [Style Placement](#style-placement)
  - [Conflict Resulution](#conflict-resulution)
  - [Styling Text](#styling-text)
- [Text Box Model and Layout](#text-box-model-and-layout)
  - [The Box Model](#the-box-model)
- [Introduction to Responsive Design](#introduction-to-responsive-design)
- [Introduction to Twitter Bootstrap](#introduction-to-twitter-bootstrap)

## Cascading Style Sheets Basics

### Power of CSS

Content is kind, but presentation is very important. Structure alone is not enough.

CSS (Cascading Style Sheets) provide styling capabilities.

Nice website to represent CSS capabilities is [csszengarden](http://csszengarden.com). Designers submit different CSS styles for this website, but they can't change the HTML.

CSS not only styles the content, but creates a particular user experience.

### Anatomy of a CSS Rule

CSS works by applying CSS rules to HTML elements.

CSS rule consists of:

- selector
- curly braces
- css declaration(-s), that consists of:
  - property
  - `:`
  - value
  - `;`

Collection of CSS rules is called a Style Sheet.

Document elements may contain default styles that comes from a browser. Every browser has some default styles.

### Element, Class and ID selector

Crafting CSS selectors is a great skill not only for creating CSS. Many Javascript libraries utilize browser selector API to attach behavior and data to HTML elements.

Types of selectors:

1. Element selector
2. Class selector
3. ID selector

We can group selectors, listing them separated with commas.

### Combining Selectors

Ways to combine selectors:

- element with class selector: `selector.class {  }`;
- direct child selector: `selector > selector`;
- descendant selector: `selector selector`;
- adjacent sibling selector: `selector + selector`
- general sibling selector: `selector ~ selector`

### Pseudo-Class Selectors

Pseudo-class selectors address targeting elements of structure that can't be targeted by combinations of regular selectors (`first-child`, `last-child`, `nth-child`) or targeting the ability to style elements based on user's intercations with them (i.e. when the element is hovered over or clicked).

Syntax: `selector:pseudo-class`

Some pseudo-classes:

- `:link`
- `:visited`
- `:hover`
- `:active`
- `:nth-child(...)`

It's usual to combine `a:link` and `a:visited` selectors.

## CSS Rules COnflinct Resolution and Text Styling

### Style Placement

Style placement defines not only how reusable those styles are, but also what styles will be applied.

### Conflict Resulution

Cascading is the core feature of CSS. It's and algorithm that defines which rule will be applied to each element.

Some concepts related to cascading algorithm:

- origin - if declarations conflict and there's no  other way to resolve it, the last declaration wins
- merge - if declarations don't conflict, they merge regardless of their origin.  
- inheritance - all child elements inherit parent's properties on all levels of inheritance. 
- specificity - most specific selector wins.

Origin means that "the last declaration wins". For external CSS it's declared where it's linked to the document.

If the declarations don't conflict but the target the same element, they merge.

Specificity score:

- inline style
- id
- class, pseudo-class, attribute
- \# of elements

### Styling Text

font-family - семейство шрифта
font-style (normal, italic, etc.) - стиль шрифта
font-weight (100, 200, bold) - жирность
font-size (24px, 16px etc.) - размер шрифта
text-transform (lowercase, uppercase, capitalize) - транформация текст
text-aligh (left, right, center, justify) - положение текста в элементе.

`em` - is a relative style that is equal to the size of the letter 'm' of a parent element.

## Text Box Model and Layout

### The Box Model

Good idea when creating layout is to change `box-sizing` to be `border-box` instead of default `content-box`.

Box sizing is not intehited. So you should use

    * {
      box-sizing: border-box; 
    }

Top and bottom margins collapse to the larger maring.

If we won't set the height of the box explicitly, the box will rize accordingly.

If we set the height explicitly, the content that won't fill will spill outside of the box. The property to deal with it is `overflow`. Values:
- `visilbe`. Default. Spill if doesn't fit
- `hidden`. Clip if doesn't fit
- `auto` - scroll if doesn't fit
- `scroll` - always scroll

Users *hate* double scroll. 

### The background property

- `backround-color` - set as solid color.
- `background-image: url("<path>")` - set an image by URL. It should be relative to the way the CSS file is served to the browser.
- `background-repeat`:
  - `repeat`
  - `no-repeat`
- `background position` defaults to `center center`
- `background url(<url>) <repeat> <position> <color>` - combined property

### Positioning Elements by Floating

`float` - takes element out of the regular document flow. Float element margins never collapse.
`clear` (`left`, `right`, `both`) - disallows browser to have any floating elements to the left.

### Relative and Absolute Element positioning

Static positioning - normal document flow. Default for all except html.
22
Relative positioning - positioned relative to its normal document flow. Relatively positioned element is not taken out of HTML flow. Its position is conserved.

All offsets are relative to the positioning of the nearest ancestor  that has non-static positioning.

`<html>` element has its position set to `relative` by default.

## Introduction to Responsive Design

### Media queries

Syntax:

    @media (<media feature>) AND|OR (<media feature>) {
      <set of CSS rules>
    }

`,` is equivalent to `OR`

Each media feature resolves as `true` or `false` and can be combined by logical operators

Examples of media features:

- `max-width: 800px`
- `min-width: 300px`
- `max-height: 500px`
- `orientation: portrait`
- `screen`
- `print`

Be careful to not overlap range boundaries of media features.

### Responsive design

The backbone of almost every responsive website is 12-column grid. Why 12 columns? Because it has a lot of factors: 2, 3, 4, 6.

We can have nested grids - each element has it's own 12-column grid.



## Introduction to Twitter Bootstrap
