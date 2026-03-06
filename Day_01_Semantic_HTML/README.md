# Day 1: The Semantic Web & HTML5 Architecture

## 1. The Core Triad of the Web
When we build for the web, we must enforce a strict separation of concerns. This is non-negotiable for professional engineering.
* **HTML (Structure):** Defines *what* the content is and its semantic meaning.
* **CSS (Presentation):** Defines *how* the content looks.
* **JavaScript (Behavior):** Defines what the content *does*.

Never mix these. No inline styles. No structural styling hacks like `<br><br>` for spacing. 

## 2. The Document Object Model (DOM)
When a browser reads your HTML document, it creates a tree-like representation of it called the Document Object Model (DOM). 
* The `<html>` tag is the root node.
* `<head>` and `<body>` are its children.
* Every element, attribute, and piece of text becomes a node in this tree.
Understanding the DOM is crucial because in Phase 2, we will use JavaScript to dynamically manipulate this tree. If your HTML is messy, your DOM is messy, and your JavaScript will be fragile.

## 3. Semantic HTML5: Meaning Over Appearance
Prior to HTML5, developers built websites using a "div soup" approach (e.g., `<div id="header">`, `<div class="main-content">`, `<div class="footer">`). This tells the browser *nothing* about the content.

Semantic tags carry meaning. They describe the payload to the browser, search engines (SEO), and assistive technologies (Screen Readers).

### Essential Semantic Tags:
* `<header>`: Introductory content or a set of navigational links for its nearest ancestor sectioning content.
* `<nav>`: A section of the page that links to other pages or to parts within the page.
* `<main>`: The dominant content of the `<body>`. There should only be one bare `<main>` per page.
* `<article>`: A self-contained composition that could be syndicated independently (e.g., a blog post, a news article).
* `<section>`: A thematic grouping of content, typically with a heading. Useful for dividing a page into logical chapters.
* `<aside>`: Content tangentially related to the content around it (like a sidebar).
* `<footer>`: The footer for its nearest ancestor sectioning content (often contains copyright, links, author info).

### Why do we care?
1. **Accessibility (a11y):** Screen readers use these tags to navigate. A blind user can jump straight to the `<nav>` or the `<main>` content. If you just use `<div>`s, you break the web for them. That is unacceptable.
2. **SEO:** Google's crawlers use semantic tags to understand the hierarchy and importance of your text. 
3. **Maintainability:** Semantic code is self-documenting. It is easier for the next engineer (or future you) to read.

## 4. Headings & Document Outline
Headings (`<h1>` through `<h6>`) are not for making text big and bold. They establish the document outline.
* You should have exactly one `<h1>` per page, representing the primary topic.
* Do not skip heading levels (don't jump from `<h2>` to `<h4>`).
* CSS handles the font size; HTML handles the hierarchy.

## 5. Forms and Inputs
Forms are how we get data from users. They must be accessible.
* Every `<input>` must have an associated `<label>`. 
* Use the `for` attribute on the `<label>` and map it to the `id` of the `<input>`.
* Use appropriate `type` attributes (`email`, `tel`, `password`) so mobile devices pull up the correct keyboard.

---

Read through these concepts. The difference between a junior developer and a senior developer starts right here: respecting the structure of the document.
