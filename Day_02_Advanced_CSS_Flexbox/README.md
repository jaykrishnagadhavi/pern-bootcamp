# Day 2: Advanced CSS & Flexbox Layouts

Welcome to Day 2. Yesterday we built a structurally sound, semantic HTML skeleton. Today, we make it look like a professional application.

## 1. CSS: The Cascading Style Sheets
CSS is a rule-based language. You define rules that specify groups of styles that should be applied to particular elements or groups of elements on your web page.

### The Box Model
Every single element on a web page is a rectangular box. Understanding the Box Model is the most critical concept in CSS:
* **Content:** The actual content of the box, where text and images appear.
* **Padding:** Clears an area around the content. The padding is transparent and sits *inside* the border.
* **Border:** A border that goes around the padding and content.
* **Margin:** Clears an area outside the border. The margin is transparent and pushes other elements away.

**Important Rule:** By default, changing the padding or border of an element expands its physical size. To prevent this headache, professional developers *always* reset the box-sizing property at the top of their CSS:

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```
This forces the padding and border to be calculated *inside* the element's explicit width/height.

## 2. Flexbox (CSS Flexible Box Layout)
Before Flexbox, developers used floats, tables, and inline-blocks to lay out pages. It was a nightmare of hacks and clearfix classes.

Flexbox is designed specifically to lay out items in a single dimension—either in a row or a column.

### Activating Flexbox
You apply `display: flex;` to the **parent container**. The immediate children of that container automatically become "flex items".

```css
.container {
    display: flex;
}
```

### Core Flexbox Properties (on the Parent)
1. **flex-direction:** Controls the direction the items flow.
   * `row` (default): left to right.
   * `column`: top to bottom.
2. **justify-content:** Aligns items along the *main axis* (horizontally if `flex-direction: row`).
   * `flex-start` (default): items pack against the start.
   * `center`: items pack around the center.
   * `space-between`: items are evenly distributed; first item is on the start line, last is on the end line.
   * `space-around`: items are evenly distributed with equal space around them.
3. **align-items:** Aligns items along the *cross axis* (vertically if `flex-direction: row`).
   * `stretch` (default): items stretch to fill the container height.
   * `flex-start`: items align to the top.
   * `center`: items align to the vertical middle.

### Core Flexbox Properties (on the Children)
1. **flex-grow:** Dictates what amount of the available space inside the flex container the item should take up.
2. **align-self:** Allows the default alignment (or the one specified by `align-items`) to be overridden for individual flex items.

## 3. CSS Variables (Custom Properties)
Modern CSS allows us to define variables natively, vastly improving maintainability and ensuring design consistency (like color palettes and spacing). We typically declare these in the `:root` pseudo-class so they are globally accessible.

```css
:root {
    --primary-color: #2563eb;
    --text-color: #1f2937;
    --bg-color: #ffffff;
    --spacing-md: 16px;
}

body {
    background-color: var(--bg-color);
    color: var(--text-color);
}
```

---

## Today's Workflow
1. Read this documentation to understand the foundational mental models.
2. Ask any clarifying questions about the Box Model or Flexbox.
3. I will assign strict layout exercises focusing on positioning items with Flexbox.
4. We will connect a `style.css` file to your Day 1 Phase 1 project and apply professional, responsive styling using Flexbox and CSS Variables.
