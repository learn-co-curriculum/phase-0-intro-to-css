# Diving into the World of CSS (Cascading Stylesheets)

## Problem Statement
As you may have learned, browsers combine the content (HTML) and presentation 
(CSS) layers to display web pages. CSS is the standard language for styling 
web pages from these HTML elements, and had different syntax to achieve a 
specific look, feel, and level of functionality to sites and apps. If you 
have ever been impressed by how a website can be displayed on a desktop 
browser while the same content looks great on a mobile device, you have 
CSS to thank for it! We know now what CSS is and its purpose, so how does
it differ from HTML and how can we utilize it?

## Overview
1. Recognize the differences between HTML and CSS
2. List the basics of CSS
3. Declare CSS properties and values

## Recognize the differences between HTML and CSS

From a conceptual standpoint, we understand that HTML and CSS play two
inherently different roles. When we write HTML, we focus on structure, 
hierarchy, and meaning.When writing HTML, some of the questions you 
might consider would be:

- How many columns should this page have to display content?
- Is this content going to display in a list-style format? 
Is it ordered or unordered? Will it display text, images, 
or mixed media elements?
- Is this the most important header in the whole HTML document?

These questions deal with structure, hierarchy, and meaning, which are
are concerns of the content layer. What does this mean as we 
start to define the presentation layer? As you write CSS, these are 
some questions you might ask yourself in the process:

- Do we want the header menu to be stationary, or does it scroll with the 
browser window?
- How do we want the content to display inside of a container? For example, 
does it fill the whole area, edge-to-edge? Is there white space around 
the content and/or the container? 
- How large should an H1 be relative to an H2? What about an H3? 
- What properties should inline links have? Underline or no underline? 
Which color for the normal state vs. the hover state? Should the 
visited link state be different?
- How should the content appear when on a desktop machine vs. a 
mobile device?

As you ask yourself these questions, your focus is on the *aesthetic* 
and display considerations of the page. These are just a few examples 
of how writing HTML differs from writing CSS.

## List the Basics of CSS

For each style, there are 3 things to keep in mind:

1. What is the specific HTML you want to style?
2. What are the aesthetic characteristics you want to modify?
(eg. the properties of text in a paragraph)
3. How do we want to modify the aesthetic characteristics of the element?
(eg. font family, font color, font size, line height, letter spacing etc.)

Once you've decided what to modify and how, we can start writing CSS using
`selectors`. CSS selectors are a way of declaring which HTML elements you 
wish to style. Selectors can look a few different ways:
- The type of HTML element(`h1`, `p`, `div`, etc.)
- The value of an element's `id` or `class` (`<p id='idvalue'></p>`,
`<p class='classname'></p>`)
- The value of an element's attributes (`value="hello"`)
- The element's relationship with surrounding elements (a `p` within an
element with class of `.infobox`)

With global rules, targeting the type selector is preferred. Type selectors 
are used to select elements based on their HTML element type. For example if
you want the body of the page to have a black background, your selector syntax
may be `html` or `body`. For anchors, you selector would be `a`. A few more
examples are listed below:

```css
/*
The CSS comment syntax is text between "slash-star" and "star-slash"
*/

/*
selects all anchor tag elements in the document (e.g. <a href="page-link.html">Page Link</a>)
*/
a

/*
selects all headers of type h3 in the document (e.g. <h3>Type selectors</h3>)
*/
h3

/*
selects all paragraph elements in the document (e.g. <p>Type selectors are used
to...</p>)
*/
p
```
You can find more information about type selectors on the Mozilla Developer
Network [type selectors documentation][].

The element type `class` is a commonly used selector. Class selectors are 
used to **select all elements that share a given class
name**. The class selector syntax is: `.classname`. Prefix the class
name with a '.'(period).

```css
/*
select all elements that have the 'important-topic' classname (e.g. <h1 class='important-topic'>
and <h1 class='important-topic'>)
*/
.important-topic

/*
select all elements that have the 'welcome-message' classname (e.g. <p class='helpful-hint'>
and <p class='helpful-hint'>)
*/
.helpful-hint
```

You can also use the `id` selector to style elements. However **There
should be only one element with a given ID** in an HTML document. This
can make styling with the ID selector good for one-off styles. The ID
selector syntax is: `#idvalue`. Prefix the id attribute of an element
with a '#' (hashtag/pound sign). 

You can find more information about type selectors on the Mozilla Developer
Network [type selectors documentation][].

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

## Declare CSS properties and values

Each element has a finite list of characteristics that can be styled.
CSS "property" names identify those characteristics. For text styling, 
examples of property names include text `color`, `text-align` and `line-height`.

CSS Property Values are directly related to property names. If we are 
working with the `color` property, the value could be a named color 
such as `red`, or `#330000`.

A CSS property name paired with a CSS property value is a **CSS declaration**.
In order to apply a CSS declaration like `color: blue` to a specific HTML
element, you need to combine your CSS declaration with a CSS selector. The
association between one or more CSS declarations and a CSS selector is 
called a **CSS declaration block**. CSS declarations (one or more) that 
applied to a specific selector are wrapped by curly braces (`{ }`). 
Each declaration inside a declaration block **must** be separated 
by a semi-colon (`;`).

Below is a sample CSS declaration block.

```css
selector {
  color: blue;
} 
/*
This is a css declaration for a selector
'color' is a property name and 'blue' is a css property value
!!!!! CSS declarations must end with a semi-colon (;) !!!!!
*/
```

Let's write a full example declaration block.

```css
/*
The CSS declaration block below will apply to all `h1` elements and will change the
text color to blue and set the font family to Georgia.
*/
h1 {
  color: blue;
  font-family: Georgia;
}
```

## Conclusion
With the combination of HTML and CSS, you are able to define content, 
structure, and style to websites. Using a CSS selector like `h1` or `p`
paired with a property declaration and value will adjust the visual 
characteristics of that element. As you add styling to elements, 
you will see how it changes the way the HTML document is displayed 
in the browser.