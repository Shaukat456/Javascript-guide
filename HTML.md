# HTML + DOM: The Complete Foundation for React


The goal is not just to memorize HTML tags. Students should understand how a web page is structured, how the browser turns HTML into a DOM tree, how JavaScript interacts with that tree, and why React makes UI development easier.

## Learning roadmap

### Part 1 — HTML fundamentals
Elements, tags, attributes, page structure, headings, text, links, images, lists, and paths.

### Part 2 — Building real pages
Semantic HTML, tables, forms, input types, buttons, and accessibility basics.

### Part 3 — DOM and JavaScript
DOM tree, selecting elements, changing content, properties, events, forms, and event bubbling.

### Part 4 — Preparing for React
HTML versus JSX, attributes versus props, event handling, rendering lists, and the virtual DOM concept.

### Part 5 — Practice and projects
Topic-wise exercises, DOM challenges, debugging tasks, and a final mini-project.

## 1. First, understand how a website works

Before writing HTML, students need a simple mental model of a web page.

A website generally uses three core technologies:

| Technology | Responsibility | Example |
|---|---|---|
| HTML | Structure and meaning | A heading, form, button |
| CSS | Appearance and layout | Colors, spacing, responsive design |
| JavaScript | Behavior and logic | Clicking a button, validating a form |

Think of a house:

- HTML is the structure: walls, doors, rooms.
- CSS is the interior design: paint, furniture, decoration.
- JavaScript is the functionality: lights, switches, automatic doors.

**Teaching idea:** Ask students what a web page would look like if each of these three technologies were missing.

### What happens when a browser opens a page?

1. The browser receives an HTML document.
2. It parses the HTML and builds a tree-like representation called the **DOM (Document Object Model)**.
3. It processes CSS to determine how elements should look.
4. It executes JavaScript, which can respond to events and update the page.
5. The browser displays the result to the user.

This is a simplified model; browsers can process HTML, CSS, and JavaScript incrementally and in parallel.

**React connection:** React helps developers describe what the UI should look like for a given state. React then coordinates updates to the rendered DOM.

---

# Part 1 — HTML fundamentals

## 2. What is HTML?

HTML stands for **HyperText Markup Language**. It is a markup language used to describe the structure and meaning of web content.

HTML is not a programming language in the usual sense. It does not provide general-purpose loops, functions, or conditional logic by itself.

For example:

```html
<h1>Welcome to My Website</h1>
<p>I am learning web development.</p>
<button>Click Me</button>
```

Here:

- `<h1>` describes a main heading.
- `<p>` describes a paragraph.
- `<button>` describes an interactive button.

The browser interprets these elements and displays them accordingly.

## 3. Tags, elements, and attributes

These three terms are essential. Students often confuse them.

### 3.1 Tags

A tag is the markup written inside angle brackets.

```html
<p>Hello World</p>
```

- `<p>` is the opening tag.
- `</p>` is the closing tag.

### 3.2 Elements

An HTML element generally consists of an opening tag, its content, and a closing tag.

```html
<p>I love programming.</p>
```

The entire expression is a paragraph element.

Some elements are *void elements*, meaning they do not have closing tags or contain child content in the usual way:

```html
<img src="photo.jpg" alt="A mountain">
<br>
<hr>
<input type="text">
```

Do not write `</img>` or `</input>`.

### 3.3 Attributes

Attributes provide additional information about an element.

```html
<a href="https://example.com">Visit Website</a>
```

- `a` defines a link.
- `href` is an attribute that specifies the destination.
- `https://example.com` is its value.

Another example:

```html
<img src="student.jpg" alt="A student studying">
```

Here, `src` specifies the image location and `alt` describes the image.

### Quick comparison

| Term | Meaning | Example |
|---|---|---|
| Tag | Markup that starts or ends an element | `<p>` |
| Element | The complete HTML structure | `<p>Hello</p>` |
| Attribute | Additional information on an element | `href="page.html"` |
| Content | What appears inside an element | `Hello` |

### Practice 1

Identify the opening tag, closing tag, element, attribute, and content:

```html
<a href="https://google.com">Search the Web</a>
```

Then write an HTML element for a heading that displays your name.

---

## 4. The basic HTML document structure

Every student should know this template by heart.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Website</title>
</head>
<body>
    <h1>Hello, World!</h1>
    <p>This is my first web page.</p>
</body>
</html>
```

Let's understand every part.

| Element | Purpose |
|---|---|
| `<!DOCTYPE html>` | Tells the browser to use modern HTML parsing standards. |
| `<html>` | Root element of the document. |
| `lang="en"` | Declares the primary language as English. |
| `<head>` | Contains metadata and resource information, not the normal page content. |
| `<meta charset="UTF-8">` | Specifies the character encoding. |
| `<meta name="viewport" ...>` | Helps the page adapt to mobile screen widths. |
| `<title>` | Sets the browser tab title. |
| `<body>` | Contains the page's main content. |

**Important distinction:** The `<head>` is not the same as the visible header of a website. The visible header is usually represented by `<header>` inside the `<body>`.

### Practice 2

Create a file named `index.html`.

1. Add the full HTML structure.
2. Change the title to `Student Portal`.
3. Add your name as a heading.
4. Add a paragraph explaining what you are learning.
5. Open the file in your browser.

---

## 5. Headings, paragraphs, and text formatting

### Headings

HTML provides six heading levels, from `<h1>` to `<h6>`.

```html
<h1>Web Development</h1>
<h2>Frontend Development</h2>
<h3>HTML</h3>
<h4>HTML Elements</h4>
<h5>Inline Elements</h5>
<h6>Additional Notes</h6>
```

Think of headings as the sections and subsections of a book.

- `<h1>`: main page heading.
- `<h2>`: major section.
- `<h3>`: subsection under an `<h2>`.

Choose heading levels based on the document's logical hierarchy, not simply the font size you want.

### Paragraphs

```html
<p>HTML structures the content of a web page.</p>
<p>CSS controls how that content looks.</p>
```

Each paragraph is a separate block of text.

### Useful text elements

```html
<p>This is <strong>important</strong>.</p>
<p>This word is <em>emphasized</em>.</p>
<p>Price: <del>$100</del> $80</p>
<p>Water is H<sub>2</sub>O.</p>
<p>Two squared is 2<sup>2</sup>.</p>
<p>Press <code>npm run dev</code> to start the app.</p>
```

| Element | Meaning |
|---|---|
| `<strong>` | Strong importance |
| `<em>` | Emphasis |
| `<mark>` | Highlighted text |
| `<del>` | Deleted or removed text |
| `<ins>` | Inserted text |
| `<sub>` | Subscript |
| `<sup>` | Superscript |
| `<code>` | Code fragment |
| `<small>` | Side comments or small print |

Use `<strong>` and `<em>` for their meaning, not merely for bold and italic appearance.

### Line breaks and horizontal rules

```html
<p>First line<br>Second line</p>
<hr>
<p>A new section begins here.</p>
```

Use `<br>` for a meaningful line break, not to create large gaps between sections. Use CSS for spacing.

### Practice 3

Create an article containing:

- One main heading.
- Three section headings.
- At least four paragraphs.
- One important statement using `<strong>`.
- One mathematical expression using `<sup>` or `<sub>`.
- One code fragment using `<code>`.

---

## 6. Links and navigation

Links connect pages, documents, and external resources.

```html
<a href="https://developer.mozilla.org/">Learn HTML</a>
```

### Link to another local page

Suppose the project contains these files:

```text
website/
├── index.html
├── about.html
└── contact.html
```

Link from `index.html` to `about.html`:

```html
<a href="about.html">About Us</a>
<a href="contact.html">Contact Us</a>
```

### Open a link in a new tab

```html
<a
    href="https://developer.mozilla.org/"
    target="_blank"
    rel="noopener"
>
    Read Documentation
</a>
```

`target="_blank"` opens a new browsing context, usually a tab. `rel="noopener"` prevents the opened page from receiving access to the originating page through `window.opener`.

### Email and telephone links

```html
<a href="mailto:student@example.com">Email Us</a>
<a href="tel:+923001234567">Call Us</a>
```

### Link to a section on the same page

```html
<a href="#courses">View Courses</a>

<h2 id="courses">Our Courses</h2>
```

The browser navigates to the element whose `id` matches the fragment.

### Relative versus absolute paths

- Absolute URL: `https://example.com/about`
- Relative path: `about.html`
- Nested path: `pages/about.html`
- Parent-directory path: `../index.html`

A relative path is resolved from the current document's URL, not necessarily from where the browser window is located.

### Practice 4

Create a three-page student portfolio:

- `index.html`
- `about.html`
- `contact.html`

Every page must link to the other two pages. Add an email link and a section link on the homepage.

---

## 7. Images and file paths

Images are one of the most common elements in web applications.

```html
<img
    src="images/profile.jpg"
    alt="Portrait of a student"
    width="250"
>
```

Understand these attributes:

- `src`: image URL or file path.
- `alt`: text alternative for the image.
- `width`: requested display width in CSS pixels.

The browser preserves the image's aspect ratio automatically when only the width is specified.

### Organizing images

```text
project/
├── index.html
└── images/
    ├── profile.jpg
    └── campus.png
```

Use:

```html
<img src="images/profile.jpg" alt="Student profile">
<img src="images/campus.png" alt="University campus">
```

A broken image commonly means the path or filename is incorrect, the file is unavailable, or the server cannot access it.

### When should `alt` be empty?

For a meaningful image:

```html
<img src="lab.jpg" alt="Students working in a physics laboratory">
```

For a purely decorative image that adds no information:

```html
<img src="decoration.svg" alt="">
```

### Practice 5

Build a profile card containing:

- A profile picture.
- Your name.
- A short description.
- A link to your portfolio.
- A meaningful `alt` attribute.

---

## 8. Lists

HTML supports three common types of lists.

### Unordered list

Use when the order does not matter.

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

### Ordered list

Use when sequence matters.

```html
<ol>
    <li>Learn HTML</li>
    <li>Learn CSS</li>
    <li>Learn JavaScript</li>
</ol>
```

### Nested lists

```html
<ul>
    <li>Frontend
        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </li>
    <li>Backend</li>
</ul>
```

### Description list

```html
<dl>
    <dt>HTML</dt>
    <dd>Defines web content and structure.</dd>

    <dt>CSS</dt>
    <dd>Controls presentation and layout.</dd>
</dl>
```

### Practice 6

Create a course page with:

- An ordered list of learning steps.
- An unordered list of technologies.
- A nested list of frontend topics.
- A description list explaining HTML, CSS, and JavaScript.

---

## 9. Semantic HTML — extremely important for React

Semantic HTML means choosing elements based on **what the content means**, rather than simply how it looks.

For example, a navigation menu should use `<nav>`, not a generic `<div>` with no semantic meaning.

### Important semantic elements

- **`<header>`** — Logo, introductory content, top-level header.
- **`<nav>`** — Navigation links.
- **`<main>`** — The primary content of the page.
- **`<section>`** — Related content grouped together.
- **`<article>`** — Independent, self-contained content.
- **`<aside>`** — Related or supplementary content.
- **`<footer>`** — Copyright, contact details, footer links.

### Example: a complete semantic page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Blog</title>
</head>
<body>
    <header>
        <h1>Student Blog</h1>
        <p>Learning web development together.</p>
    </header>

    <nav aria-label="Main navigation">
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
        <a href="contact.html">Contact</a>
    </nav>

    <main>
        <section>
            <h2>Latest Posts</h2>

            <article>
                <h3>My First HTML Page</h3>
                <p>Today I learned about HTML elements.</p>
            </article>

            <article>
                <h3>Learning the DOM</h3>
                <p>Today I learned how JavaScript accesses a page.</p>
            </article>
        </section>

        <aside>
            <h2>Recommended</h2>
            <p>Practice writing HTML every day.</p>
        </aside>
    </main>

    <footer>
        <p>&copy; 2026 Student Blog</p>
    </footer>
</body>
</html>
```

### Why does semantic HTML matter for React?

React components often represent meaningful parts of a page:

```jsx
function Header() {
    return (
        <header>
            <h1>Student Blog</h1>
        </header>
    );
}
```

You do not need to use a `<div>` for everything. Semantic elements make applications more understandable, improve accessibility, and can help search engines interpret content.

### Practice 7

Build a blog page using semantic HTML only. Include a header, navigation, main content, at least two articles, a sidebar, and a footer.

---

## 10. `div` versus `span`

These two elements are extremely common in React applications.

### The `div` element

`<div>` is a generic container for grouping content.

```html
<div>
    <h2>Student Profile</h2>
    <p>Name: Ali</p>
    <p>Department: Physics</p>
</div>
```

By default, a `div` is a block-level element. It normally starts on a new line and occupies the available width.

### The `span` element

`<span>` is a generic inline container.

```html
<p>
    My favorite subject is
    <span>Quantum Mechanics</span>.
</p>
```

It is useful for grouping a small part of text without creating a separate block.

### Visual comparison

**DIV — block-level by default**

```html
<div>First block</div>
<div>Second block</div>
```

**SPAN — inline by default**

```html
<p>Learn <span>HTML</span> and <span>JavaScript</span> together.</p>
```

The distinction is about their default display behavior, not a permanent limitation. CSS can change either one's display mode.

### Practice 8

Create a student card using a `div`. Inside its description, use `span` to identify the student's department and status.

---

## 11. HTML tables

Tables represent structured data, not general page layouts.

```html
<table>
    <caption>Student Marks</caption>

    <thead>
        <tr>
            <th scope="col">Name</th>
            <th scope="col">Subject</th>
            <th scope="col">Marks</th>
        </tr>
    </thead>

    <tbody>
        <tr>
            <td>Ali</td>
            <td>Physics</td>
            <td>85</td>
        </tr>
        <tr>
            <td>Sara</td>
            <td>Mathematics</td>
            <td>92</td>
        </tr>
    </tbody>
</table>
```

| Element | Purpose |
|---|---|
| `<table>` | Creates the table |
| `<caption>` | Describes the table |
| `<thead>` | Groups header rows |
| `<tbody>` | Groups data rows |
| `<tr>` | Creates a row |
| `<th>` | Creates a header cell |
| `<td>` | Creates a data cell |
| `<tfoot>` | Groups footer rows, often totals |

HTML creates the structure; CSS controls borders, spacing, colors, and responsiveness.

### Practice 9

Create a marks table with five students and three subjects. Include a header row and a final row showing totals or averages.

---

## 12. Forms — essential for React

Forms are among the most important HTML concepts because React applications frequently collect user input.

Examples include:

- Login and registration.
- Search bars.
- Contact forms.
- Checkout forms.
- Student registration systems.
- Filters and settings.

### 12.1 The basic form

```html
<form>
    <label for="username">Username</label>
    <input
        type="text"
        id="username"
        name="username"
        placeholder="Enter your username"
    >

    <button type="submit">Register</button>
</form>
```

Understand the difference between these attributes:

- `id` identifies an element within the document.
- `name` identifies the field when form data is submitted.
- `placeholder` provides a hint inside an empty input.
- `for` connects a label to the input with the matching `id`.

**Important:** A placeholder is not a replacement for a proper label.

### 12.2 Common input types

- **Text:** Names, usernames, short text.
- **Email:** Email-format validation.
- **Password:** Masks the displayed characters.
- **Number:** Numeric input.
- **Date:** Date selection.
- **Checkbox:** Independent yes/no choices.

Other important types include `tel`, `url`, `search`, `radio`, `file`, `hidden`, `time`, and `range`.

The examples below demonstrate common input types:

```html
<input type="text" placeholder="Enter your name">
<input type="email" placeholder="you@example.com">
<input type="password" placeholder="Enter password">
<input type="number" placeholder="Enter age">
<input type="date">
<input type="checkbox">
```

### 12.3 Radio buttons versus checkboxes

Radio buttons allow one selection from a group when they share the same `name`.

```html
<p>Select your department:</p>

<label>
    <input type="radio" name="department" value="physics">
    Physics
</label>

<label>
    <input type="radio" name="department" value="computer-science">
    Computer Science
</label>
```

Checkboxes allow independent selections:

```html
<p>Select your interests:</p>

<label>
    <input type="checkbox" name="interest" value="coding">
    Coding
</label>

<label>
    <input type="checkbox" name="interest" value="research">
    Research
</label>
```

### 12.4 Dropdowns

```html
<label for="course">Choose a course:</label>

<select id="course" name="course">
    <option value="">Select a course</option>
    <option value="html">HTML</option>
    <option value="javascript">JavaScript</option>
    <option value="react">React</option>
</select>
```

### 12.5 Textareas

```html
<label for="message">Your message</label>

<textarea
    id="message"
    name="message"
    rows="5"
    placeholder="Write your message"
></textarea>
```

### 12.6 Buttons and their types

```html
<button type="button">Perform an action</button>

<button type="submit">Submit the form</button>

<button type="reset">Reset the form</button>
```

Inside a form, a `<button>` defaults to submit behavior if no other type is specified. Explicitly defining the type prevents accidental submissions.

### 12.7 HTML form validation

HTML offers built-in validation features:

```html
<form>
    <label for="email">Email</label>
    <input
        id="email"
        name="email"
        type="email"
        required
    >

    <label for="age">Age</label>
    <input
        id="age"
        name="age"
        type="number"
        min="18"
        max="100"
        required
    >

    <button type="submit">Submit</button>
</form>
```

Useful validation attributes include:

- `required`
- `min` and `max`
- `minlength` and `maxlength`
- `pattern`
- `step`

Client-side validation improves user experience but does not replace server-side validation.

### Practice 10 — Registration form

Create a form that collects:

1. Full name.
2. Email.
3. Password.
4. Age.
5. Department using radio buttons.
6. Skills using checkboxes.
7. Country using a dropdown.
8. A short biography.
9. Agreement to terms.
10. A submit button.

Use proper labels, appropriate input types, and validation attributes.

---

# Part 2 — The DOM (Document Object Model)

This is the bridge between HTML and React.

## 13. What exactly is the DOM?

DOM stands for **Document Object Model**.

When a browser parses HTML, it creates an object-based representation of the document. JavaScript can use this representation to find elements, read values, change content, modify attributes, and respond to user interactions.

Consider:

```html
<body>
    <h1>Hello</h1>
    <p>Welcome to my website.</p>
</body>
```

The browser creates a tree-like structure conceptually similar to this:

```text
document
└── html
    ├── head
    │   └── Metadata
    └── body
        ├── h1
        │   └── "Hello"
        └── p
            └── "Welcome to my website."
```

### Important DOM vocabulary

| Term | Meaning |
|---|---|
| Document | The complete document object |
| Node | A unit in the DOM tree |
| Element | A node representing an HTML element |
| Text node | A node representing text content |
| Parent | An element that contains another node |
| Child | A node directly inside another node |
| Sibling | Nodes sharing the same parent |
| Descendant | Any node nested inside an ancestor |

For example:

```html
<div id="card">
    <h2>Ali</h2>
    <p>Physics Student</p>
</div>
```

- The `div` is the parent of the `h2` and `p`.
- The `h2` and `p` are siblings.
- Both are descendants of the `div`.
- The text `Ali` is represented by a text node.

**Key lesson:** HTML is the markup source; the DOM is the browser's structured object model. JavaScript interacts with the DOM, not by editing the original HTML file directly.

---

## 14. Selecting DOM elements

Before JavaScript can change an element, it needs to find it.

Consider this HTML:

```html
<h1 id="title">Welcome</h1>

<p class="description">Learn JavaScript.</p>
<p class="description">Practice every day.</p>

<button id="changeButton">Change Title</button>
```

### 14.1 `getElementById()`

Selects an element by its ID.

```javascript
const title = document.getElementById("title");

console.log(title);
```

This returns the element with `id="title"`, or `null` if no matching element exists.

### 14.2 `querySelector()`

Selects the first element matching a CSS selector.

```javascript
const title = document.querySelector("#title");

const description = document.querySelector(".description");

const button = document.querySelector("button");
```

Selector meanings:

- `#title` selects an ID.
- `.description` selects a class.
- `button` selects a button element.

### 14.3 `querySelectorAll()`

Selects all matching elements and returns a static `NodeList`.

```javascript
const descriptions = document.querySelectorAll(".description");

console.log(descriptions.length);

descriptions.forEach(function (paragraph) {
    console.log(paragraph.textContent);
});
```

### 14.4 `getElementsByClassName()`

Returns a live `HTMLCollection`.

```javascript
const descriptions =
    document.getElementsByClassName("description");
```

A live collection can reflect DOM changes to the matching elements. By contrast, `querySelectorAll()` returns a static collection.

For most beginner projects, teach `querySelector()` and `querySelectorAll()` first because their CSS-selector syntax is versatile.

### Practice 11

Given a page with:

- One element with `id="heading"`.
- Four elements with `class="item"`.
- Three buttons.

Write JavaScript that selects the heading, the first item, all items, and all buttons. Print the results and the number of items.

---

## 15. Changing content with JavaScript

Once an element has been selected, JavaScript can change its content.

```html
<h1 id="title">Original Title</h1>
<p id="message">Waiting for an update...</p>

<script>
    const title = document.querySelector("#title");
    const message = document.querySelector("#message");

    title.textContent = "Updated Title";
    message.textContent = "The content has changed!";
</script>
```

### `textContent` versus `innerHTML`

Suppose we have:

```html
<div id="output"></div>
```

Using `textContent`:

```javascript
output.textContent = "<strong>Hello</strong>";
```

The browser displays the literal characters:

`<strong>Hello</strong>`

Using `innerHTML`:

```javascript
output.innerHTML = "<strong>Hello</strong>";
```

The browser parses the string as HTML, so `Hello` appears bold.

**Security warning:** Never insert untrusted user input into `innerHTML`. It can introduce cross-site scripting (XSS) vulnerabilities. Prefer `textContent` when you intend to display text.

### Reading content

```html
<h2 id="studentName">Ali</h2>

<script>
    const nameElement = document.querySelector("#studentName");

    console.log(nameElement.textContent);
</script>
```

### Practice 12

Create a page with a heading and paragraph. Use JavaScript to change both after the script executes. Then change the heading to display a name entered by the user without interpreting that name as HTML.

---

## 16. Attributes and properties

Students often use these terms interchangeably, but there is a difference.

Consider:

```html
<input id="username" value="Ali">
```

The HTML attribute `value="Ali"` provides the initial value. The DOM property `input.value` gives the current value of the input.

```javascript
const input = document.querySelector("#username");

console.log(input.getAttribute("value")); // "Ali"
console.log(input.value);                // "Ali"

input.value = "Sara";

console.log(input.value);                // "Sara"
console.log(input.getAttribute("value")); // Usually still "Ali"
```

This distinction is particularly important for form inputs.

### Common DOM properties

```javascript
element.textContent;
element.innerHTML;
element.value;
element.id;
element.className;
element.checked;
element.disabled;
```

Not every property is relevant to every element. For example, `checked` is useful for checkboxes and radio buttons.

### Practice 13

Create a checkbox and an input field. Write JavaScript to read the input's current value, check whether the checkbox is selected, and disable a button when the input is empty.

---

## 17. Changing styles and CSS classes

JavaScript can change an element's appearance directly.

```javascript
const title = document.querySelector("#title");

title.style.color = "blue";
title.style.fontSize = "32px";
```

However, modifying CSS classes is often a better approach for reusable styling.

```html
<style>
    .highlight {
        background-color: yellow;
        color: black;
    }

    .hidden {
        display: none;
    }
</style>

<p id="message">Important message</p>
```

```javascript
const message = document.querySelector("#message");

message.classList.add("highlight");
message.classList.remove("highlight");
message.classList.toggle("highlight");

console.log(message.classList.contains("highlight"));
```

| Method | Purpose |
|---|---|
| `classList.add()` | Adds a class |
| `classList.remove()` | Removes a class |
| `classList.toggle()` | Adds or removes a class |
| `classList.contains()` | Checks whether a class exists |

### Practice 14

Create a paragraph and a button. Each click should toggle a `highlight` class on the paragraph. Add another button that hides or shows the paragraph.

---

## 18. DOM events — the foundation of interactivity

An event is something that happens in the browser, such as:

- A button being clicked.
- A key being pressed.
- A form being submitted.
- An input value changing.
- A page finishing its initial load.

JavaScript can listen for these events and execute a function.

### 18.1 The click event

```html
<h1 id="title">Hello!</h1>
<button id="changeButton">Click Me</button>

<script>
    const title = document.querySelector("#title");
    const button = document.querySelector("#changeButton");

    button.addEventListener("click", function () {
        title.textContent = "You clicked the button!";
    });
</script>
```

`addEventListener()` attaches a listener for a specified event.

### 18.2 Why use `addEventListener()`?

You might encounter this:

```html
<button onclick="sayHello()">Click</button>
```

This is an inline event handler. It works, but `addEventListener()` generally separates HTML structure from JavaScript behavior more cleanly and allows multiple listeners.

### 18.3 The event object

```javascript
button.addEventListener("click", function (event) {
    console.log(event.type);
    console.log(event.target);
    console.log(event.currentTarget);
});
```

- `event`: information about the event.
- `event.target`: the element where the event originated.
- `event.currentTarget`: the element whose listener is currently executing.

These can be different when an event bubbles through nested elements.

### 18.4 Common events

| Event | Typical use |
|---|---|
| `click` | Buttons and clickable controls |
| `input` | Responding as text changes |
| `change` | Responding when a value is committed or changed, depending on the control |
| `submit` | Processing a form submission |
| `keydown` | Handling keyboard keys |
| `focus` | Input receives focus |
| `blur` | Input loses focus |
| `DOMContentLoaded` | HTML has been parsed and the DOM is ready |

### Practice 15

Create a counter with three buttons:

- Increase.
- Decrease.
- Reset.

Every click should update the number displayed on the page.

---

## 19. Handling form input using the DOM

This is one of the most valuable exercises before React.

```html
<form id="studentForm">
    <label for="name">Student name</label>
    <input id="name" name="name" required>

    <button type="submit">Add Student</button>
</form>

<p id="output"></p>

<script>
    const form = document.querySelector("#studentForm");
    const nameInput = document.querySelector("#name");
    const output = document.querySelector("#output");

    form.addEventListener("submit", function (event) {
        event.preventDefault();

        const studentName = nameInput.value.trim();

        if (studentName === "") {
            output.textContent = "Please enter a name.";
            return;
        }

        output.textContent = `Welcome, ${studentName}!`;
    });
</script>
```

### What is `preventDefault()`?

Normally, submitting a form may cause a browser navigation or page reload.

```javascript
event.preventDefault();
```

This prevents the event's default action. In this example, JavaScript handles the submission instead.

It does not automatically validate the data or send it to a server. Those tasks require additional logic.

### Why does `.trim()` matter?

```javascript
const name = nameInput.value.trim();
```

It removes whitespace from the beginning and end of the string. That way, a field containing only spaces is treated as empty.

### Practice 16

Build a form that accepts a student's name and marks. On submission:

1. Read both values.
2. Validate the inputs.
3. Calculate the percentage if the total marks are known.
4. Display the result.
5. Clear the form if submission succeeds.

---

## 20. Creating and removing elements

DOM manipulation includes creating new elements and adding them to the page.

```html
<ul id="taskList"></ul>
<button id="addTask">Add Task</button>

<script>
    const taskList = document.querySelector("#taskList");
    const addButton = document.querySelector("#addTask");

    addButton.addEventListener("click", function () {
        const item = document.createElement("li");

        item.textContent = "Complete HTML practice";

        taskList.appendChild(item);
    });
</script>
```

Important methods:

- `document.createElement()` creates an element.
- `appendChild()` adds a node as a child.
- `append()` adds nodes or text.
- `remove()` removes an element.
- `replaceChildren()` replaces an element's children.

### Removing an element

```javascript
const firstItem = document.querySelector("li");

if (firstItem) {
    firstItem.remove();
}
```

The check prevents an error if there is no matching list item.

### Practice 17

Create a task list where users can:

- Enter a task.
- Add the task to a list.
- Mark a task as complete.
- Delete a task.
- Display a message when no tasks remain.

---

## 21. Event bubbling and event delegation

This topic is especially useful when building dynamic interfaces.

Consider:

```html
<div id="parent">
    <button id="child">Click Me</button>
</div>
```

A click on the button can trigger the button's listener and then propagate to the parent. This upward propagation is called **event bubbling**.

```javascript
const parent = document.querySelector("#parent");
const child = document.querySelector("#child");

parent.addEventListener("click", function () {
    console.log("Parent clicked");
});

child.addEventListener("click", function () {
    console.log("Button clicked");
});
```

Clicking the button typically logs:

```text
Button clicked
Parent clicked
```

### `stopPropagation()`

```javascript
child.addEventListener("click", function (event) {
    event.stopPropagation();

    console.log("Button clicked only");
});
```

This stops the event from propagating further through the DOM. Use it when needed rather than by default.

### Event delegation

Instead of attaching a listener to every list item, attach one listener to their parent.

```html
<ul id="items">
    <li><button data-action="delete">Delete A</button></li>
    <li><button data-action="delete">Delete B</button></li>
    <li><button data-action="delete">Delete C</button></li>
</ul>
```

```javascript
const items = document.querySelector("#items");

items.addEventListener("click", function (event) {
    const button = event.target.closest("button[data-action='delete']");

    if (!button || !items.contains(button)) {
        return;
    }

    button.closest("li").remove();
});
```

Why is this useful? One listener can handle buttons added later, as long as their events reach the parent.

### Practice 18

Create a list of ten items. Use event delegation so that clicking any item's delete button removes the corresponding item. Newly added items must work without adding new event listeners.

---

## 22. Traversing the DOM

DOM traversal means moving from one element to its relatives.

```html
<div id="container">
    <h2>Student</h2>
    <p id="description">Physics student</p>
    <button>View Profile</button>
</div>
```

```javascript
const description = document.querySelector("#description");

console.log(description.parentElement);
console.log(description.previousElementSibling);
console.log(description.nextElementSibling);
console.log(description.children);
```

Useful properties and methods:

| Property or method | Meaning |
|---|---|
| `parentElement` | Parent element |
| `children` | Collection of child elements |
| `firstElementChild` | First child element |
| `lastElementChild` | Last child element |
| `previousElementSibling` | Previous sibling element |
| `nextElementSibling` | Next sibling element |
| `closest(selector)` | Nearest matching ancestor, including the element itself |

For UI work, element-specific properties such as `children` and `nextElementSibling` are often easier to use than `childNodes`, which also includes text nodes and comments.

### Practice 19

Create a card with a title, description, and button. When the button is clicked, use DOM traversal to change the description inside that same card. Do not select the description using a hardcoded global ID.

---

## 23. When should JavaScript run?

If a script tries to select an element before the browser has parsed it, the result may be `null`.

Problem:

```html
<script>
    const title = document.querySelector("#title");
    console.log(title);
</script>

<h1 id="title">Hello</h1>
```

The script executes before the heading is parsed.

### Solution 1: place the script after the content

```html
<h1 id="title">Hello</h1>

<script>
    const title = document.querySelector("#title");
    console.log(title);
</script>
```

### Solution 2: use `defer`

```html
<head>
    <script src="app.js" defer></script>
</head>
```

For a classic external script, `defer` allows HTML parsing to continue and runs the script after parsing is complete.

### Solution 3: listen for `DOMContentLoaded`

```javascript
document.addEventListener("DOMContentLoaded", function () {
    const title = document.querySelector("#title");

    console.log(title);
});
```

This event fires after the document has been parsed and deferred scripts have executed. It does not wait for every image or other external resource to finish loading.

### Practice 20

Create a separate `app.js` file. Load it from the HTML using `defer`, and make it update a heading and button. Verify that the JavaScript works without placing the script at the end of the body.

---

# Part 3 — Connecting HTML and the DOM to React

## 24. What is React, and why do we need it?

Imagine building a dashboard with:

- 20 interactive buttons.
- A list of 100 tasks.
- A search box.
- Filters.
- A form.
- Notifications.
- Several sections that update independently.

You could manually manipulate the DOM for each change. But as an application grows, coordinating those changes becomes difficult.

React lets you describe the UI using components and state.

### Vanilla JavaScript approach

```html
<h1 id="count">0</h1>
<button id="increase">Increase</button>
```

```javascript
let count = 0;

const heading = document.querySelector("#count");
const button = document.querySelector("#increase");

button.addEventListener("click", function () {
    count++;
    heading.textContent = count;
});
```

You must select the element, listen for the event, update the variable, and manually update the DOM.

### React approach

```jsx
import { useState } from "react";

function Counter() {
    const [count, setCount] = useState(0);

    return (
        <div>
            <h1>{count}</h1>

            <button onClick={() => setCount(count + 1)}>
                Increase
            </button>
        </div>
    );
}

export default Counter;
```

React connects the state to the rendered UI. When the state changes, React schedules an update and reconciles the rendered result.

The key idea is:

**In React, describe what the UI should look like for the current state, instead of manually changing every DOM element yourself.**

---

## 25. HTML versus JSX

JSX is a JavaScript syntax extension commonly used with React to describe UI elements.

It resembles HTML, but several rules are different.

### Difference 1: `class` versus `className`

HTML:

```html
<h1 class="title">Hello</h1>
```

JSX:

```jsx
<h1 className="title">Hello</h1>
```

In JSX, use `className` for CSS classes.

### Difference 2: `for` versus `htmlFor`

HTML:

```html
<label for="email">Email</label>
<input id="email" type="email">
```

JSX:

```jsx
<label htmlFor="email">Email</label>
<input id="email" type="email" />
```

### Difference 3: closing tags

HTML permits certain optional closing tags, and void elements do not have closing tags.

JSX requires elements to be properly closed.

```jsx
<img src="/profile.jpg" alt="Profile" />
<input type="text" />
<br />
```

### Difference 4: JavaScript expressions inside `{}`

HTML:

```html
<h1>Welcome</h1>
```

JSX:

```jsx
const name = "Ali";

<h1>Welcome, {name}</h1>
```

Curly braces allow JavaScript expressions inside JSX.

### Difference 5: event handlers

HTML:

```html
<button onclick="sayHello()">Click</button>
```

React JSX:

```jsx
<button onClick={sayHello}>Click</button>
```

React uses camelCase event names such as `onClick` and `onChange`. Here, `sayHello` is passed as a function rather than called immediately.

### Difference 6: inline styles

HTML:

```html
<h1 style="color: blue; font-size: 24px;">Hello</h1>
```

JSX:

```jsx
<h1 style={{ color: "blue", fontSize: "24px" }}>
    Hello
</h1>
```

In JSX, the `style` prop accepts an object. The outer braces enter JavaScript expression mode; the inner braces define the object.

### Difference 7: rendering lists

In HTML, students manually write repeated elements:

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

In React, they can generate the list from an array:

```jsx
const subjects = ["HTML", "CSS", "JavaScript"];

function SubjectList() {
    return (
        <ul>
            {subjects.map((subject) => (
                <li key={subject}>{subject}</li>
            ))}
        </ul>
    );
}
```

The `key` helps React identify items across updates. Use a stable, unique identifier when available; array indexes are not ideal keys for lists that can be reordered or modified.

---

## 26. HTML attributes versus React props

HTML attributes configure elements:

```html
<input type="text" placeholder="Enter name">
```

React props pass information into components or configure elements:

```jsx
function StudentCard({ name, department }) {
    return (
        <div>
            <h2>{name}</h2>
            <p>{department}</p>
        </div>
    );
}

function App() {
    return (
        <StudentCard
            name="Ali"
            department="Physics"
        />
    );
}
```

Here:

- `StudentCard` is a component.
- `name` and `department` are props.
- `"Ali"` and `"Physics"` are the supplied values.

This is one of the biggest differences between writing a static HTML page and building a reusable React application.

---

## 27. The DOM versus the virtual DOM

Students often hear that React uses a virtual DOM. They should understand the idea without believing that the virtual DOM is a second browser DOM.

- **DOM:** The browser's object representation of the document.
- **React element:** A description of what React should render.
- **Virtual DOM:** An informal term commonly used for React's in-memory element tree and related representations.
- **Reconciliation:** React's process of comparing rendered descriptions and determining the updates needed.
- **DOM update:** Changes applied to the actual browser DOM.

A simplified example:

1. A counter displays `0`.
2. The user clicks Increase.
3. React state becomes `1`.
4. React renders the component again.
5. React reconciles the new result and updates the relevant DOM output.

React does not necessarily rebuild the entire real DOM on every render. Also, React is not always faster than manual DOM manipulation in every situation; its main benefit is a declarative, component-based model for managing UI.

---

## 28. Controlled inputs — a critical React concept

In plain HTML and JavaScript, an input can manage its own current value in the DOM.

In React, a controlled input has its value driven by React state.

```jsx
import { useState } from "react";

function NameForm() {
    const [name, setName] = useState("");

    return (
        <div>
            <label htmlFor="name">Your name</label>

            <input
                id="name"
                value={name}
                onChange={(event) => setName(event.target.value)}
            />

            <p>Hello, {name || "student"}!</p>
        </div>
    );
}

export default NameForm;
```

Walk through the flow:

1. `useState("")` creates state with an empty string.
2. `value={name}` makes the input display the current state value.
3. Typing triggers `onChange`.
4. `event.target.value` provides the new input value.
5. `setName()` updates state.
6. React renders the updated value in the paragraph and input.

This is why students need to understand DOM input values, events, and event objects before learning React forms.

---

# Part 4 — Hands-on practice workbook

The following exercises are designed to turn the concepts into practical skills.

## Student practice tracker

Use this checklist to track completion:

- [ ] **1. HTML document** — Create a valid HTML document with a title, heading, paragraph, and metadata. *(Beginner)*
- [ ] **2. Personal portfolio** — Build a three-page website using links, images, headings, and lists. *(Beginner)*
- [ ] **3. Semantic blog** — Build a blog using header, nav, main, section, article, aside, and footer. *(Beginner)*
- [ ] **4. Student marks table** — Display five students, subject marks, headings, and a totals row. *(Beginner)*
- [ ] **5. Registration form** — Collect user details with labels, multiple input types, and validation. *(Beginner)*
- [ ] **6. Interactive counter** — Implement increase, decrease, and reset using DOM events. *(Intermediate)*
- [ ] **7. Live character counter** — Show how many characters remain while a user types in a textarea. *(Intermediate)*
- [ ] **8. Searchable list** — Filter a list of students as the user types into a search field. *(Intermediate)*
- [ ] **9. Task manager** — Add, complete, delete, and count tasks using DOM manipulation. *(Intermediate)*
- [ ] **10. Event delegation** — Build a dynamic list with delete buttons handled by one parent listener. *(Intermediate)*
- [ ] **11. Student result calculator** — Validate marks, calculate percentages, and display a result. *(Intermediate)*
- [ ] **12. React conversion** — Convert the task manager or counter into a React component using state. *(React-ready)*

---

## 29. Final project — Student Management Dashboard

This project combines HTML, DOM manipulation, events, forms, arrays, and objects. It also provides a natural starting point for a React application.

### Project requirements

Students must build a dashboard that lets a user:

- Add a student with a name, department, and marks.
- Display all students in a table or list.
- Search students by name.
- Delete a student.
- Calculate the class average.
- Validate the form.
- Show helpful messages when the list is empty or input is invalid.

### Suggested interface

**Student Dashboard**

| Metric | Example |
|---|---:|
| Total students | 3 |
| Class average | 81.7% |

**Add student**

- Student name
- Department
- Marks out of 100
- Add Student button

*Illustrative mockup. The controls above are for demonstrating the interface, not a complete persistent student database.*

### Recommended file structure

```text
student-dashboard/
├── index.html
├── styles.css
└── app.js
```

### Recommended implementation order

1. Build the static HTML structure.
2. Style the page with basic CSS.
3. Select the form, input fields, search box, and output container.
4. Create an array of student objects.
5. Add a student when the form is submitted.
6. Render the array into the DOM.
7. Implement search and delete operations.
8. Calculate the average.
9. Test empty inputs, invalid marks, and an empty list.
10. Convert the project into React using components and state.

The project initially stores data in memory. Refreshing the page will clear it unless students add a persistence mechanism such as `localStorage` or a backend.

---

# Part 5 — Quick revision and assessment

## 30. Essential concepts students must know before React

### HTML foundations

- [ ] Explain tags, elements, and attributes.
- [ ] Write a complete HTML document.
- [ ] Use headings, paragraphs, links, images, and lists.
- [ ] Explain relative paths and image alt text.
- [ ] Choose semantic elements appropriately.
- [ ] Create tables and accessible forms.

### DOM foundations

- [ ] Explain the DOM tree and parent/child relationships.
- [ ] Select elements with querySelector and querySelectorAll.
- [ ] Read and update textContent and input.value.
- [ ] Explain attributes versus DOM properties.
- [ ] Use classList to update styles.
- [ ] Create and remove elements.

### Events and interaction

- [ ] Use addEventListener.
- [ ] Explain event.target and event.currentTarget.
- [ ] Handle form submissions using preventDefault.
- [ ] Explain event bubbling and delegation.
- [ ] Read and validate form values.
- [ ] Explain why script loading order matters.

### React readiness

- [ ] Explain HTML versus JSX.
- [ ] Use className and htmlFor in JSX.
- [ ] Pass JavaScript expressions using braces.
- [ ] Explain props and reusable components.
- [ ] Explain state-driven rendering and controlled inputs.
- [ ] Explain why lists need stable keys.

## 31. Common mistakes to watch for

| Mistake | Correct approach |
|---|---|
| Using `<div>` for everything | Use semantic elements where appropriate. |
| Using placeholder instead of a label | Associate a real `<label>` with the input. |
| Using `innerHTML` with user input | Prefer `textContent` for plain text. |
| Selecting an element before it exists | Use `defer` or appropriate script placement. |
| Forgetting `preventDefault()` | Prevent native form submission when handling it manually. |
| Using `onclick` everywhere | Learn `addEventListener()` for vanilla JavaScript. |
| Confusing HTML `value` with current input value | Read the DOM property `input.value`. |
| Using `class` in JSX | Use `className`. |
| Using `for` in JSX labels | Use `htmlFor`. |
| Manually manipulating the DOM throughout a React component | Normally let React manage rendered UI through state and props. |
| Using array indexes for every React key | Prefer stable, unique item identifiers. |




**Final advice for students:** Don't try to memorize every tag. Learn the common elements, practise creating forms and pages, understand how JavaScript accesses the DOM, and build small projects without copying complete solutions. Once students can independently create a page, manipulate its content, handle events, and validate forms, they will have a strong foundation for learning React.
