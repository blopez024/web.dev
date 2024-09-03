# Overview of HTML

### Elements

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

- HTML documents begin with a type declaration (`<!DOCTYPE html>`) and include the `<html>` root element.
- The `<html>` element is the parent of both `<head>` and `<body>`.
- Example:
  ```html
  <!DOCTYPE html>
  <html lang="en-US"></html>
  ```
- The lang attribute is typically a two- or three-letter ISO code followed by the region code (e.g., `en-US`).

### Head and Body Elements

- The `<head>` and `<body>` tags are nested between the opening and closing `<html>` tags.
- The first element in the `<head>` should be the character set:

  ```html
  <meta charset="utf-8" />
  ```

- The document title is displayed in the browser tab, list of open windows, history, and search results.

### Viewport

- The viewport meta tag helps with site responsiveness:

  ```html
  <meta name="viewport" content="width=device-width" />
  ```

### Styles and Links

- The `<head>` section is where styles are included for your HTML document, using either the `<link>`, `<style>`, or style attributes.
- It is recommended to use the `<link>` tag for linking external stylesheets, as it enhances both developer experience and site performance.

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
  - **Default**: `render -> download JS -> execute JS -> render`
  - **Defer**: `render & download JS -> execute JS`
  - **Async**: `render & download JS -> pause & execute JS -> render`

---

# Metadata

- Metadata components are commonly found in the `<head>` tag.
- Example of metadata:

  ```html
  <meta http-equiv="refresh" content="30" />
  ```

- The `http-equiv` attribute can refresh the page, but this practice is generally discouraged.

### Open Graph Meta Tags

- Open Graph meta tags control how social media platforms display content when a link is shared.

---

# Semantic HTML

### Semantic Elements

- Over 100 HTML elements exist, and they should be used to structure content based on meaning, not appearance.
- Using semantic elements improves accessibility.
- Example: Using the `role` attribute, you can give any element a specific role, helping assistive technologies better understand the content.

---

# Heading and sections

- Before adding content, consider its purpose.
- When the `<header>` element is top-level, it serves as the site banner or landmark.

  - The `<nav>` element identifies navigation content.
  - The `<footer>` should contain site information, such as copyright, contact info, and links to privacy policies or cookies. It is typically displayed on every page.

### Holy Grail Layout

- This common layout structure includes a header, two sidebars, main content, and a footer.

### Key Elements

- `<main>`: Identifies the primary content in the document. There should only be one <main> element per page.
- `<aside>`: Contains content that is indirectly related to the main content.
- `<article>`: Represents a complete or self-contained section of content.
- `<section>`: Used for grouping related content within the page.

### Headings

- There are six section headings (`<h1>` to` <h6>`), with 1 being the highest level of importance and `<h6>` the lowest.
- Do not use headings purely for styling purposes, such as making text bold or large—use CSS for that.

---

# Attributes

### Global Attributes

- `id`: Provides a unique identifier for an element. The first character should be a letter, and only ASCII letters, digits, underscores (`_`), and hyphens (`-`) should be used. The `id` should be unique within the document.

- Fragment Identifier: Acts as an anchor or bookmark to an element. When clicked, it scrolls the element into view.

- Class: Offers another way to target elements with CSS and JavaScript. It serves no intrinsic purpose in HTML.

- Style: Allows for inline CSS to be applied directly to the element.

### Boolean Attributes

- Boolean attributes are always considered `true`. When toggling between true and false, you can remove the attribute entirely with JavaScript.

### Custom Attributes

- You can create custom attributes by adding the `data-` prefix.

---

# Text Basics

- Heading Elements: HTML provides six heading elements (`<h1>` through `<h6>`), with `<h1>` being the most important and `<h6>` the least. Screen reader users often rely on headings to navigate content.

- Quotes and Citations:

  - `<blockquote>`: Defines a block-level quote.
  - `<q>`: Defines an inline quote.
  - `<cite>`: Refers to the title of a work (e.g., a book or article), _not_ the author.

- Line Breaks:

  - `<br>`: Inserts a line break within a block of text.

- HTML Entities: Represent special characters using escape sequences or named entities (e.g., `&amp;` for `&`).

---

# Links

---

- Lists

---

- Navigation

---

- Tables

---

- Forms

---

- Images
- Audio and Video
- Template, slot, and shadow
- HTML APIs
- Focus
- Other inline text elements
- Details and summary
- Dialog
