# Week 2

- [Cascading Style Sheets Basics](#cascading-style-sheets-basics)
  - [Power of CSS](#power-of-css)
  - [Anatomy of a CSS Rule](#anatomy-of-a-css-rule)
  - [Element, Class and ID selector](#element-class-and-id-selector)
  - [Combining Selectors](#combining-selectors)
  - [Pseudo-Class Selectors](#pseudo-class-selectors)
- [CSS Rules COnflinct Resolution and Text Styling](#css-rules-conflinct-resolution-and-text-styling)
- [Text Box Model and Layout](#text-box-model-and-layout)
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

## Text Box Model and Layout

## Introduction to Responsive Design

## Introduction to Twitter Bootstrap
