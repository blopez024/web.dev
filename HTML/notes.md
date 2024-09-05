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

- Anchor Tag (`<a>`): Used to create hyperlinks when paired with the `href` attribute. Links are the foundation of the internet.

- Elements That Create Links: Links can be created using the following elements: `<a>`, `<area>`, `<form>`, and `<link>`.

- `href` Attribute: Used to link to locations within the current page, other pages, or external sites. It can also be used for downloading files or sending emails.

  - Examples:
    - `href="#top"`: Link to an element with the `id="top"`.
    - `href="mailto:hal9000@gmail.com"`: Open an email client to send an email.
    - `href="tel:2131112222"`: Initiate a phone call.
    - Downloadable Resources: Add the `download` attribute to an `<a>` tag to specify a file for download, e.g., `<a href="image.svg" download="name.svg">`.

- Browsing Contexts:

  - `_self`: Opens the link in the current window (default).
  - `_blank`: Opens the link in a new tab.
  - `_parent`: Opens the link in the parent frame (useful for nested objects like iframes).
  - `_top`: Opens the link in the topmost frame.
  - Note: Opening multiple `_blank` links creates multiple tabs; to reuse the same tab, provide a "tab context" (using the `target` attribute).

- **MIME** Types: MIME types are advisory and inform the user about the type of document being opened. Providing context about the linked resource helps users manage their expectations.

- Tracking Link Clicks: To track user interactions, the `ping` attribute can be used to send data to secure URLs when a link is clicked. This attribute contains a space-separated list of URLs to ping.

- User Experience:

  - Provide clear information about the linked resources so users know what they are clicking on.
  - Ensure that links are visually distinct from surrounding text.
  - Include focus styles for accessibility.
  - Avoid placing interactive content (e.g., buttons or forms) inside a link.

---

# Lists

- List Types: HTML offers three types of lists:

  - Ordered List (`<ol>`): Displays items in a numbered or lettered sequence.
  - Unordered List (`<ul>`): Displays items with bullet points.
  - Description List (`<dl>`): Contains terms (`<dt>`) and their descriptions (`<dd>`).

- List Items:

  - `<li>`: Represents a list item. It must be nested within an `<ol>`, `<ul>`, or `<menu>`.
  - It can have a single attribute (`value`), typically an integer, that can be used when the list is nested to set a specific starting point.

- Ordered List Attributes:

  - `type`: Specifies the type of marker (numbers, letters, etc.) used in the list.
  - `reversed`: Reverses the order of the list items.
  - `start`: Specifies the starting point for the list numbering.

- Styling Lists:

  - The bullet or numbering style of lists can be defined using the `list-style-type` property in CSS or the `type` attribute for ordered lists.

- Description List:

  - A description list (`<dl>`) contains description terms (`<dt>`) and their corresponding descriptions (`<dd>`), forming term-description pairs.

---

# Navigation

- Types of Navigation:

  - Local Navigation: Links to other pages within the same website, including named anchors within text.
  - Breadcrumb Navigation: Shows the path the user followed to reach the current page.
  - Table of Contents: Provides an outline of a page’s sections, allowing users to navigate to different parts of the page.
  - Site Map: Contains hierarchical links to every page on a website.
  - Global Navigation: Links to the top-level pages of the website, typically present on every page.

- Best Practices: Ensure users can navigate to any page on your site with minimal clicks without overwhelming them with too many options.

- HTML Element: The `<nav>` element is the most appropriate tag for defining sections of navigation within a webpage.

---

- Tables

---

- Forms

---

- Images

---

- Audio and Video

---

- Template, slot, and shadow

---

- HTML APIs

---

- Focus

---

- Other inline text elements

---

- Details and summary

---

- Dialog
