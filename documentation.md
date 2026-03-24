# Business Website Guide with HTML, CSS, and JavaScript

This is a reusable handbook for building business websites with plain HTML, CSS, and JavaScript.

Use it as:

- a learning guide
- a copy-paste reference
- a checklist when building client sites

## 1. Core idea

Websites usually use three layers:

- HTML: structure and content
- CSS: styling and layout
- JavaScript: interactivity and behavior

Basic example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Describe the business here.">
  <title>Business Name</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Welcome to My Business</h1>
  <script src="script.js"></script>
</body>
</html>
```

## 2. Common project structure

```text
project/
  index.html
  about.html
  products.html
  contact.html
  style.css
  script.js
  images/
```

## 3. HTML tags you will use constantly

### Headings

```html
<h1>Main page heading</h1>
<h2>Section heading</h2>
<h3>Subsection heading</h3>
```

Use one main `h1` per page when possible.

### Paragraphs

```html
<p>This is a paragraph.</p>
```

### Links

```html
<a href="contact.html">Contact</a>
<a href="mailto:info@business.com">Email Us</a>
<a href="tel:5551234567">Call Us</a>
```

### Images

```html
<img src="images/logo.png" alt="Business logo">
```

Always use `alt`.

### Buttons

```html
<button type="button">Click Me</button>
<button type="submit">Submit</button>
```

### Lists

```html
<ul>
  <li>Free estimates</li>
  <li>Fast service</li>
  <li>Reliable support</li>
</ul>
```

### Containers

```html
<div class="card">Card content</div>
<span class="highlight">Highlighted text</span>
```

## 4. Semantic HTML you should prefer

These tags help with structure, accessibility, and SEO:

```html
<header></header>
<nav></nav>
<main></main>
<section></section>
<article></article>
<aside></aside>
<footer></footer>
```

Example:

```html
<body>
  <header>
    <nav>...</nav>
  </header>

  <main>
    <section>Hero</section>
    <section>Services</section>
    <section>Testimonials</section>
  </main>

  <footer>...</footer>
</body>
```

## 5. Business website sections you will build often

### Navbar

```html
<header class="site-header">
  <nav class="navbar">
    <a href="index.html" class="logo">Business Name</a>
    <div class="nav-links">
      <a href="index.html">Home</a>
      <a href="about.html">About</a>
      <a href="services.html">Services</a>
      <a href="contact.html">Contact</a>
    </div>
  </nav>
</header>
```

### Hero

```html
<section class="hero">
  <div class="hero-content">
    <h1>Professional Services for Local Businesses</h1>
    <p>Short message explaining the main value.</p>
    <a href="contact.html" class="btn">Get a Quote</a>
  </div>
</section>
```

### Services or product cards

```html
<section class="services">
  <h2>Our Services</h2>
  <div class="grid">
    <article class="card">
      <h3>Service One</h3>
      <p>Description here.</p>
    </article>
    <article class="card">
      <h3>Service Two</h3>
      <p>Description here.</p>
    </article>
  </div>
</section>
```

### Contact form

```html
<form class="contact-form">
  <label for="name">Name</label>
  <input type="text" id="name" name="name" required>

  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>

  <label for="message">Message</label>
  <textarea id="message" name="message" rows="5" required></textarea>

  <button type="submit">Send</button>
</form>
```

### Footer

```html
<footer class="footer">
  <p>&copy; 2026 Business Name</p>
  <p><a href="mailto:info@business.com">info@business.com</a></p>
</footer>
```

## 6. HTML attributes to know

```html
<div class="card"></div>
<section id="services"></section>
<img src="images/photo.jpg" alt="Office photo">
<input type="email" placeholder="Email" required>
```

Most common:

- `class`: reusable styling hook
- `id`: unique target for links or JavaScript
- `src`: file location for images or scripts
- `href`: destination for links
- `alt`: image description
- `type`: tells inputs and buttons how to behave
- `required`: makes fields mandatory

## 7. CSS syntax

```css
selector {
  property: value;
}
```

Example:

```css
h1 {
  color: blue;
  font-size: 40px;
}
```

## 8. CSS selectors

```css
p {
  color: black;
}

.card {
  background: #f4f4f4;
}

#hero {
  min-height: 500px;
}

.navbar a {
  color: white;
}
```

- `p` targets all paragraphs
- `.card` targets a class
- `#hero` targets a unique id
- `.navbar a` targets links inside `.navbar`

## 9. Colors

### Text color

```css
p {
  color: #333333;
}
```

### Background color

```css
body {
  background-color: white;
}
```

### Common formats

```css
color: red;
color: #1c96e8;
color: rgb(28, 150, 232);
color: rgba(28, 150, 232, 0.7);
```

## 10. Text styling

```css
body {
  font-family: Arial, sans-serif;
}

h1 {
  font-size: 48px;
  font-weight: 700;
  letter-spacing: 1px;
}

p {
  line-height: 1.6;
  text-align: left;
}

a {
  text-decoration: none;
}
```

Useful properties:

- `font-family`
- `font-size`
- `font-weight`
- `line-height`
- `letter-spacing`
- `text-align`
- `text-transform`
- `text-decoration`

## 11. Spacing and sizing

```css
.box {
  width: 300px;
  height: 200px;
  padding: 20px;
  margin: 20px;
  border: 1px solid #ccc;
  border-radius: 12px;
}
```

Meaning:

- `width` and `height`: size
- `padding`: space inside
- `margin`: space outside
- `border`: outline
- `border-radius`: rounded corners

## 12. Display and layout

### Common display values

```css
display: block;
display: inline;
display: inline-block;
display: none;
display: flex;
display: grid;
```

## 13. Flexbox

Flexbox is one of the most useful CSS tools for business sites.

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 20px;
}
```

Key properties:

- `justify-content`: horizontal distribution
- `align-items`: vertical alignment
- `gap`: spacing between items
- `flex-direction`: row or column

Common values:

```css
justify-content: flex-start;
justify-content: center;
justify-content: flex-end;
justify-content: space-between;
```

## 14. Grid

Great for cards and product layouts.

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
```

Responsive version:

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}
```

## 15. Positioning

```css
position: static;
position: relative;
position: absolute;
position: fixed;
position: sticky;
```

Examples:

```css
.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
}

.badge {
  position: absolute;
  top: 10px;
  right: 10px;
}
```

## 16. Centering

### Center text

```css
text-align: center;
```

### Center a layout container

```css
.container {
  width: min(1100px, 90%);
  margin: 0 auto;
}
```

### Center with flexbox

```css
.hero {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## 17. Backgrounds and images

```css
.hero {
  background: linear-gradient(to right, #1c96e8, #0f4c81);
}

.banner {
  background-image: url("images/hero.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}
```

## 18. Buttons

```css
.btn {
  display: inline-block;
  padding: 12px 24px;
  background: #1c96e8;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
}

.btn:hover {
  background: #1477b8;
}
```

## 19. Forms in CSS

```css
label {
  display: block;
  margin-bottom: 8px;
  font-weight: 600;
}

input,
textarea,
select {
  width: 100%;
  padding: 12px;
  margin-bottom: 16px;
  border: 1px solid #ccc;
  border-radius: 8px;
}
```

## 20. Responsive design

Always include:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Use media queries:

```css
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    align-items: flex-start;
  }

  .grid {
    grid-template-columns: 1fr;
  }
}
```

Typical mobile changes:

- stack columns
- reduce padding
- reduce font sizes slightly
- make buttons easier to tap

## 21. Strong CSS starter base

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  line-height: 1.6;
  color: #222;
  background: #fff;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}

a {
  color: inherit;
  text-decoration: none;
}

.container {
  width: min(1100px, 90%);
  margin: 0 auto;
}
```

## 22. JavaScript basics

JavaScript adds behavior.

Examples:

- opening a mobile menu
- validating forms
- updating page content
- showing popups

### Add the file

```html
<script src="script.js"></script>
```

### Variables

```js
let businessName = "Goofbox";
const button = document.querySelector(".btn");
```

### Selecting elements

```js
const heading = document.querySelector("h1");
const cards = document.querySelectorAll(".card");
```

### Changing text

```js
heading.textContent = "Welcome to Goofbox";
```

### Click events

```js
button.addEventListener("click", function () {
  alert("Button clicked");
});
```

### Toggle a class

```js
const menuButton = document.querySelector(".menu-button");
const navLinks = document.querySelector(".nav-links");

menuButton.addEventListener("click", function () {
  navLinks.classList.toggle("open");
});
```

## 23. Useful JavaScript for business websites

### Auto year in footer

HTML:

```html
<p>&copy; <span id="year"></span> Business Name</p>
```

JavaScript:

```js
document.querySelector("#year").textContent = new Date().getFullYear();
```

### Basic form validation

```js
const form = document.querySelector(".contact-form");

form.addEventListener("submit", function (event) {
  const email = document.querySelector("#email").value;

  if (email === "") {
    event.preventDefault();
    alert("Please enter your email.");
  }
});
```

## 24. Accessibility basics

Important habits:

- use real heading order
- use `alt` text
- connect labels to inputs
- keep text readable
- do not rely only on color

Good:

```html
<label for="email">Email</label>
<input type="email" id="email" name="email">
```

## 25. SEO basics

Important basics for each page:

- unique `<title>`
- meta description
- one clear `h1`
- useful page text
- good image `alt` text
- mobile-friendly layout

Example:

```html
<title>Goofbox | Custom Gift Boxes</title>
<meta name="description" content="Shop custom gift boxes for birthdays, holidays, and special events.">
```

## 26. Common mistakes to avoid

- forgetting `body { margin: 0; }`
- missing the viewport meta tag
- not testing on mobile
- stretching images
- using too many colors
- using too many fonts
- putting everything inside plain `div`s
- forgetting hover states
- using fixed widths that break small screens

## 27. Starter business website example

### HTML

```html
<body>
  <header>
    <nav class="navbar container">
      <a href="index.html" class="logo">Business Name</a>
      <div class="nav-links">
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div class="container">
        <h1>Main Business Headline</h1>
        <p>Short explanation of what the company offers.</p>
        <a href="#contact" class="btn">Get Started</a>
      </div>
    </section>

    <section id="services" class="section">
      <div class="container">
        <h2>Services</h2>
        <div class="grid">
          <article class="card">
            <h3>Service One</h3>
            <p>Description</p>
          </article>
          <article class="card">
            <h3>Service Two</h3>
            <p>Description</p>
          </article>
        </div>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container">
      <p>&copy; <span id="year"></span> Business Name</p>
    </div>
  </footer>
</body>
```

### CSS

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  color: #222;
}

.container {
  width: min(1100px, 90%);
  margin: 0 auto;
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.nav-links {
  display: flex;
  gap: 20px;
}

.hero {
  padding: 100px 0;
  background: #f5f9fc;
}

.section {
  padding: 80px 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
}

.card {
  padding: 24px;
  border-radius: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
}

.btn {
  display: inline-block;
  padding: 12px 24px;
  background: #1c96e8;
  color: white;
  border-radius: 8px;
}
```

### JavaScript

```js
document.querySelector("#year").textContent = new Date().getFullYear();
```

## 28. Ecommerce and Shopify note

If you want customers to buy directly from the site, Shopify is a good option for:

- products
- carts
- checkout
- payments
- inventory

A practical path is:

- build the marketing pages in HTML/CSS/JS
- use Shopify for the store and checkout

## 29. Best workflow for client websites

1. Plan the pages and sections.
2. Build the HTML structure first.
3. Style the layout and spacing with CSS.
4. Add colors, typography, and buttons.
5. Make it mobile responsive.
6. Add JavaScript only where needed.
7. Test links, forms, and layout on multiple screen sizes.

## 30. What to learn next

After this guide, the best next topics are:

- advanced flexbox and grid
- mobile nav menus
- form submission services
- SEO structure
- Shopify integration
- accessibility testing

Use this file as your starting handbook whenever you build a new business site.
