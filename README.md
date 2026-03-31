# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/fontend_mentor_order_summary_component/blob/main/project_screenshot.png)

### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/fontend_mentor_order_summary_component.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/fontend_mentor_order_summary_component/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** Flexbox for centering the card and managing the internal alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

Check the code snippets attached below:

```html
<main>
  <article class="order_summary">
    <img class="hero-image" src="./images/illustration-hero.svg" alt="Hero Image">
    <section class="order_content">
      <h1 class="title">Order Summary</h1>
      <p class="description">You can now listen to millions of songs, audiobooks, and podcasts on any device anywhere you like!</p>
      <div class="plan">
        <img class="icon" src="./images/icon-music.svg" alt="Music Icon">
        <div class="plan_details">
          <h2>Annual Plan</h2>
          <p class="price">$59.99/year</p>
        </div>
        <a class="change-link" href="#" rel="noopener noreferrer">Change</a>
      </div>
      <button type="button" class="proceed_btn">Proceed to Payment</button>
      <button type="button" class="cancel_btn">Cancel Order</button>
    </section>
  </article>
</main>
```
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --fw-base: 500;
  --fw-bold: 900;
  --fw-semibold: 700;
  --font-size-base: 1rem;
  --blue-50: 225, 100%, 98%;
  --gray-600: 224, 23%, 55%;
  --blue-950: 223, 47%, 23%;
  --blue-700: 245, 75%, 52%;
  --blue-100: 225, 100%, 94%;
  --font-family: 'Red Hat Display', sans-serif;
}
body {
  display: flex;
  height: 100vh;
  line-height: 1.5;
  align-items: center;
  justify-content: center;
  color: hsl(var(--gray-600));
  font-weight: var(--fw-base);
  font-family: var(--font-family);
  font-size: var(--font-size-base);
  background: hsl(var(--blue-100)) url(./images/pattern-background-mobile.svg) no-repeat center top / 100%;
}
img {
  height: auto;
  max-width: 100%;
}
.hero-image {
  display: block;
}
.order_summary {
  margin: 0 auto;
  overflow: hidden;
  border-radius: 1.25rem;
  width: min(450px, 90%);
  background-color: hsl(var(--blue-50));
  box-shadow: 0rem 1.5rem 3rem -1.5rem hsla(var(--blue-700), 0.2);
}
.order_content {
  gap: 1.5rem;
  display: flex;
  padding: 2rem;
  text-align: center;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}
.order_content .title {
  color: hsl(var(--blue-950));
  font-weight: var(--fw-bold);
  font-size: clamp(var(--font-size-base), 1vw + 1.125rem, 1.75rem);
}
.order_content .plan {
  gap: 1rem;
  width: 100%;
  display: flex;
  padding: 1rem;
  text-align: left;
  align-items: center;
  border-radius: 1rem;
  background-color: hsla(var(--blue-100), 0.25);
}
.order_content .plan h2 {
  font-weight: var(--fw-bold);
  color: hsl(var(--blue-950));
  font-size: clamp(var(--font-size-base), 1vw + 0.5rem, 1.125rem);
}
.order_content .plan a {
  margin-left: auto;
  color: hsl(var(--blue-700));
  font-weight: var(--fw-bold);
  font-size: calc(var(--font-size-base) / 1.125);
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
.order_content .plan a:hover, .order_content .plan a:focus, .order_content .plan a:active {
  opacity: 0.7;
  text-decoration: none;
}
.order_content .proceed_btn, .order_content .cancel_btn {
  width: 100%;
  border: none;
  padding: 1rem;
  cursor: pointer;
  border-radius: 0.75rem;
  color: hsl(var(--blue-50));
  font-weight: var(--fw-semibold);
  font-family: var(--font-family);
  font-size: var(--font-size-base);
  background-color: hsl(var(--blue-700));
  box-shadow: 0 1rem 1rem 0 hsla(var(--blue-700), 0.2);
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
.order_content .proceed_btn:hover, .order_content .proceed_btn:focus, .order_content .proceed_btn:active {
  opacity: 0.7;
}
.order_content .cancel_btn {
  padding: 0;
  width: auto;
  box-shadow: none;
  font-weight: var(--fw-bold);
  color: hsl(var(--gray-600));
  background-color: transparent;
}
.order_content .cancel_btn:hover, .order_content .cancel_btn:focus, .order_content .cancel_btn:active {
  color: hsl(var(--blue-950));
}
.attribution { font-size: 11px; text-align: center; position: absolute; bottom: 1rem; }
.attribution a { color: hsl(var(--blue-700)); }

@media (min-width: 992px) {
  body {
    background-image: url(./images/pattern-background-desktop.svg);
  }
  .order_content {
    padding: 2.5rem 3rem;
  }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)