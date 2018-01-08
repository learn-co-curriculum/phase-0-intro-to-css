# Introduction

In the previous lesson, we introduced the distinction between content (the HTML
document) and presentation ("Cascading Style Sheets" or CSS). Browsers combine
the content and presentation layers to display HTML documents (web pages) to
the you. Now it's time to dive a little deeper into the presentation topic by
learning more about CSS, the standard language for styling and laying out HTML
elements.  If you have ever been delighted by how a website appears or have
been amazed how the same content looks great on a browser _and also_ great on a
mobile device, you have CSS to thank for it.

# How Does Writing CSS Differ From Writing HTML?

As we write CSS these are the type of questions we might ask ourselves:

- Should the layout of the text be in a single or double column?
- Should we use a different font color for the header?
- How should the same content appear differently on a desktop vs. a mobile
device?

All of the questions above deal with the *esthetic* considerations of the page.
These are the concerns of the presentation layer (CSS).

As a contrast, let's consider the type of questions we might ask ourselves as
we write HTML:

- Does the order of items within a list matter? Should it be a numbered list?
- Should we wrap a list of links inside a navigation tag?
- Is this the most important header in the whole HTML document?

The last few questions deal with structure, hierarchy, and meaning. These are
the concerns of the content layer (HTML).

When we write CSS, we focus on esthetic and display considerations. When we
write HTML, we focus on structure, hierarchy, and meaning.

# The Process of Styling

The process of styling HTML can be described in three steps:

1. Identify the specific HTML element we wish to style.
2. Determine what esthetic characteristics ("CSS properties") we wish to
   modify. In the case of text do we wish to change the color of
   the font?
3. Determine the desired state of esthetic characteristic ("CSS property"). In
   the case of text do we wish the color to appear red, blue, etc.?

# The Basics of CSS

How can we translate the process of styling into CSS?

1. **CSS selectors** are used to **identify HTML elements**
2. **CSS properties** are used to **express the esthetic characteristics we wish
   to style**
3. **CSS Values** are used to **express the desired states of the esthetic
   characteristics**

Below we will explore CSS selectors, CSS properties, and CSS values in more detail.

## CSS Selectors

CSS Selectors are a way of declaring which HTML element(s) we wish to style.
Selectors can be based on:

- the type of HTML element(`h1`, `p`, `div`, etc.)
- the value of an element's `id` or `class` (`<p id='idvalue'></p>`,
`<p class='classvalue'></p>`)
- the value of an element's attributes (`value="hello"`)
- the element's relationship with surrounding elements (a `p` within an
  `.infobox`)

The element type, `id`, and `class` are the most commonly used selectors. Let's
review a few examples of each selector.

### Type Selectors

Type selectors are used to select elements based on their HTML element type.
The type selector syntax is simply: `htmlelementname`.

```css
/*
selects all headers of type h3 in the document (e.g. <h3>Type selectors</h3>)
*/
h3

/*
selects all paragraph elements in the document (e.g. <p>TType selectors are used
to...</p>)
*/
p

/*
p.s. this the CSS comment syntax
*/

```

You can find more information about type selectors on the Mozilla Developer
Network [type selectors documentation][].

### ID Selectors

ID selectors are used to select elements based on their ID attribute value.
There should be only one element with a given ID in an HTML document. The ID
selector syntax is: `#idvalue`. Simply prefix the idvalue with a '#'.

```css
/*
selects the HTML element with the id 'main-header' (e.g. <h1 id='main-header'>)
*/
#main-header

/*
selects the HTML element with the id 'welcome-message' (e.g. <p id='welcome-message'>)
*/
#welcome-message
```

You can find more information about ID selectors on the Mozilla Developer Network
[id selectors documentation][].

### Class Selectors

Class selectors are used to select all elements that have a given class name. The
class selector syntax is: `.classname`. Simply prefix the classname with a '.'.

```css
/*
select all elements that have the 'main-headers' classname (e.g. <h1 class='main-headers'>
and <h1 class='main-headers'>)
*/
.main-headers

/*
select all elements that have the 'welcome-message' classname (e.g. <p class='welcome-messages'>
and <p class='welcome-messages'>)
*/
.welcome-messages
```

You can find more information about class selectors on the Mozilla Developer
Network [class selectors documentation][].

## CSS Property Names

Each element has a finite list of esthetic characteristics that can be styled.
CSS properties names identify those characteristics. Each element will have a
different set of property names. For text styling, examples of property names
include text `color`, `text-align` and `line-height`.

## CSS Values

Values are directly related to property names. If we are working with the `color`
property the value could be a named-color such as `red`.

## CSS Declaration

A property name paired with a value is a CSS declaration.

```css
color:blue;
/*
This is a css declaration
'color' is a property name and 'blue' is a value
CSS declaration should end with a semi-colon (;).
*/
```

## CSS Declaration Blocks

How can we apply the CSS declaration `color:blue` to a specific HTML element(s)?
We need to combine our CSS declaration with a CSS selector. The association
between one or more CSS declarations and a CSS selector is called a CSS declaration
block. CSS declarations (one o more) that applied to a specific selector are
wrapped by curly braces ({ }). Each declaration inside a declaration block has
to be separated by a semi-colon (;).

Below is a sample CSS declaration block.

```css
selector {
    property-name: value;
    property-name: value;
}
```

```css
/*
The CSS declaration block below will apply to all h1 elements and will change the
text color to blue and set the font family to Georgia.
*/
h1 {
    color:blue;
    font-family: Georgia;
}
```

## Applying CSS to an HTML Document
Enough reading about HTML and CSS. Let's move on to the next lesson to edit some
CSS code and see how it will change the way the HTML document is displayed in the
browser.

[type selectors documentation]: https://developer.mozilla.org/en-US/docs/Web/CSS/Type_selectors
[id selectors documentation]: https://developer.mozilla.org/en-US/docs/Web/CSS/ID_selectors
[class selectors documentation]: https://developer.mozilla.org/en-US/docs/Web/CSS/Class_selectors
