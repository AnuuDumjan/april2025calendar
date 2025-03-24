# More HTML & Forms

## Session 1: Introduction to Semantic HTML

### What is Semantic HTML?

Semantic HTML refers to using HTML elements that convey meaning about their content, making the structure of web pages more understandable to both developers and browsers.

### Importance of Semantic HTML

- **Accessibility:** Improves navigation for assistive technologies.
- **SEO:** Enhances search engine understanding and indexing.
- **Code Readability:** Makes the HTML structure clearer for developers.

### Non-Semantic vs. Semantic Elements

- **Non-Semantic Elements:** `<div>`, `<span>` – Generic containers without specific meaning.
- **Semantic Elements:** `<article>`, `<section>`, `<header>`, `<footer>`, `<nav>`, `<aside>`, `<main>` – Clearly define the purpose of the content they enclose.

### Key Semantic Elements

- `<header>`: Defines introductory content or navigational links.
- `<nav>`: Contains navigation links.
- `<main>`: Specifies the main content of a document.
- `<section>`: Represents a thematic grouping of content.
- `<article>`: Denotes independent, self-contained content.
- `<aside>`: Contains content tangentially related to the main content.
- `<footer>`: Defines a footer for a document or section.

### Practical Example: Refactoring Non-Semantic to Semantic HTML

**Non-Semantic HTML:**

```html
<div>
  <div>
    <h1>Website Title</h1>
    <p>Welcome to our website!</p>
  </div>
  <div>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#contact">Contact</a>
  </div>
  <div>
    <h2>About Us</h2>
    <p>We are a company dedicated to providing excellent services.</p>
  </div>
  <div>
    <p>&copy; 2025 Company Name. All rights reserved.</p>
  </div>
</div>
Semantic HTML:

<header>
  <h1>Website Title</h1>
  <p>Welcome to our website!</p>
</header>
<nav>
  <a href="#home">Home</a>
  <a href="#about">About</a>
  <a href="#services">Services</a>
  <a href="#contact">Contact</a>
</nav>
<main>
  <section>
    <h2>About Us</h2>
    <p>We are a company dedicated to providing excellent services.</p>
  </section>
</main>
<footer>
  <p>&copy; 2025 Company Name. All rights reserved.</p>
</footer>
```

## Session 2: Building Forms with Semantic HTML

### Purpose of HTML Forms

Forms collect user input for processing, such as registrations, feedback, or orders.

### The `<form>` Element

- **Definition:** A container for form controls.
- **Attributes:**
    - `action`: Specifies where to send the form data upon submission.
    - `method`: Defines the HTTP method (`GET` or `POST`) to use when submitting the form.

### Common Form Controls

- **Text Fields:** `<input type="text">` – For single-line text input.
- **Radio Buttons:** `<input type="radio">` – Allow selection of one option from a set.
- **Checkboxes:** `<input type="checkbox">` – Enable multiple selections.
- **Submit Buttons:** `<input type="submit">` – Trigger form submission.

### The `<label>` Element

- **Purpose:** Associates text with form controls, enhancing accessibility.
- **Usage:** Clicking the label focuses the corresponding input.

### Grouping Controls with `<fieldset>` and `<legend>`

- **`<fieldset>`:** Groups related form controls.
- **`<legend>`:** Provides a caption for the `<fieldset>`, describing its purpose.

### Form Accessibility Best Practices

- Use labels for all form controls.
- Ensure keyboard navigation is supported.
- Provide clear instructions and error messages.

### Hands-on Example: Creating a Contact Form

```html
html
CopyEdit
<form action="/submit-contact" method="post">
  <fieldset>
    <legend>Contact Us</legend>

    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <label for="message">Message:</label>
    <textarea id="message" name="message" required></textarea>

    <button type="submit">Send Message</button>
  </fieldset>
</form>

```

## Session 3: Creating Tables in HTML

### Purpose of HTML Tables

Tables organize data into rows and columns, facilitating comparison and analysis.

### Basic Table Structure

- `<table>`: The container element for a table.
- `<tr>`: Defines a row in the table.
- `<th>`: Defines a header cell in a table.
- `<td>`: Defines a standard data cell in a table.

### Adding a Table Caption

- `<caption>`: Provides a title or description for the table, improving accessibility.

### Grouping Table Sections

- `<thead>`: Groups the header content.
- `<tbody>`: Groups the body content.
- `<tfoot>`: Groups the footer content.

### Spanning Rows and Columns

- `colspan`: Attribute that allows a cell to span multiple columns.
- `rowspan`: Attribute that allows a cell to span multiple rows.

### Table Accessibility Best Practices

- Use `<caption>` to describe the table's purpose.
- Use `<th>` for header cells and associate them with data cells using the `scope` attribute.
- Ensure tables are readable and navigable with assistive technologies.

### Hands-on Example: Creating a Product Inventory Table

```html
html
CopyEdit
<table>
  <caption>Product Inventory</caption>
  <thead>
    <tr>
      <th scope="col">Product Name</th>
      <th scope="col">Description</th>
      <th scope="col">Price</th>
      <th scope="col">Availability</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Product A</td>
      <td>High-quality product A.</td>
      <td>$10.00</td>
      <td>In Stock</td>
    </tr>
    <tr>
      <td>Product B</td>
      <td>Durable and reliable product B.</td>
      <td>$15.00</td>
      <td>Out of Stock</td>
    </tr>
    <tr>
      <td>Product C</td>
      <td>Eco-friendly product C.</td>
      <td>$20.00</td>
      <td>In Stock</td>
    </tr>
  </tbody>
</table>

```
