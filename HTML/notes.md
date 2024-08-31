# Overview of HTML

## Elements

- Elements are written using angle brackets (`< >`).
- Example:
  - Opening tag: `<p>`
  - Closing tag: `</p>`

### Non-Replaced Elements

- Elements that cannot contain text content or nested elements.
- Examples: `<p>`, `<header>`, `<list>`

### Replaced and Void Elements

- **Replaced Elements**:
  - These can contain alternative content, such as media.
  - Examples: `<video>`, `<picture>`, `<object>`, `<iframe>`
- **Void Elements**:
  - These self-close and do not contain nested elements or text content.
  - Examples: `<br>`, `<col>`, `<embed>`, `<hr>`, `<img>`, `<input>`, `<link>`, `<meta>`, `<source>`, `<track>`, `<wbr>`

### Attributes

- Attributes provide information about the element and appear only in the opening tag.
- They define behavior, linkages, and functionality. Using quotes for attribute values is recommended.
- Some attributes are case-sensitive.
- Example:
  ```html
  <a href="#register" target="_self">Registration</a>
  ```

### Appearance:

- The appearance of HTML elements is controlled by CSS.
- Certain tags, such as `<strong>` and `<em>`, have semantic meaning that implies visual styling and emphasis.

---

# Document Structure

### Structure

- HTML documents start with a type declaration and include the `<html>` root element, which is the parent of `<head>` and `<body>`.
- Example:

```html
<!DOCTYPE html>
<html lang="en-US"></html>
```

### Head and Body Elements

- The `<head>` and `<body>` tags are nested between the opening and closing `<html>` tags.
- The first element in the `<head>` should be the character set:

```html
<meta charset="utf-8" />
```

-The document title is displayed in the browser tab, list of open windows, history, and search results.

### Viewport

-The viewport meta tag helps with site responsiveness:

```html
<meta name="viewport" content="width=device-width" />
```

### Styles and Links

-The `<head>` section is where styles are included for your HTML document, using either the `<link>`, `<style>`, or style attributes.
-It is recommended to use the `<link>` tag for linking external stylesheets, as it enhances both developer experience and site performance.

#### Other Uses of `<link>`

- The `<link>` tag also creates relationships between the HTML document and external resources.
  Example of a link to a favicon:

```html
<link
  rel="icon"
  sizes="16x16 32x32 48x48"
  type="image/png"
  href="/images/mlwicon.png"
/>
```

##### Alternate and Canonical Links

- Alternate: Used to represent alternative versions of a site (e.g., translations in French or Spanish).
- Canonical: Used to specify the authoritative source when several alternatives exist, often for SEO purposes.

---

# Scripts

- The `<script>` tag is used to include JavaScript files.
- Place scripts at the bottom of the document to ensure elements are loaded before the script runs.
- Script loading options:
  - **Default**: render -> download JS -> execute JS -> render
  - **Defer**: render -> download JS -> execute JS
  - **Async**: render -> download JS -> pause -> execute JS -> render

---

- Metadata
  Components you almost always find in the <head> tag

http-equiv can be used to refresh page, but you shouldn't

open graph meta tags are used to control how social media sites display content links

---

- Semantic
  Over 100 HTML elements exists'
  use HTML elements to structure content based on element meaning not appearance
  using semantic elements helps accessibility
  using the ROLE attribute you can give any element a role
  tags have semantic meaning, HTML should be used to structure content

  ***

- Headings and section
think about the purpose of the content
When <header> is top level, its the site banner or landmark role
  <nav> element identifies content as navigation
<footer> should contain the site information on every page such as copyright, contact info, and links to privacy and cookies

Holy Grail Layout:
Header, two sidebars, and a footer

 <main> element identifies the main content in the document.
 There should one be one per page

 <aside> is for content that is indirectly or tangentially related to the document.

 <article> represents a complete, or self-contained section of content

 <section> element is used to encompass generic standalone sections

Headings
There are six section headings, with h1 being the highest or most important and h6 being the lowest
Don't use heading to make text bold or large, use CSS instead

---

- Attributes
  make HTML so powerful
  are space-separated names and name/value pairs
  define behavior, linkages, and functionality
  quoting is always recommended
  some attributes are case-sensitive
  boolean attributes are always TRUE
  when toggling b/t true and false remove the attribute with JavaScript

30 Global Attributes, can be set on any HTML element
id, is used to define a unique identifier for an element
make it id first character a letter, and use only ASCII letters, digits, \_, and -
id should be unique to the document

fragment identifier is an anchor or bookmark to that element
when the user clicks to any link, the element scrolls into view

class provides an additional way of targeting elements with CSS and JavaScript, but serve no purpose in HTML
style attribute enables applying inline styles

Custom Attributes
create any custom attribute by adding the data- prefix

- Basics
- Links
- Lists
- Navigation
- Tables
- Forms
- Images
- Audio and Video
- Template, slot, and shadow
- HTML APIs
- Focus
- Inline text
- Details and summary
- Dialog

```

```
