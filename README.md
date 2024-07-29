# Frontend Mentor - Faq Accordion

<div align="left">
  <a href="https://github.com/MinhQuan2121?tab=repositories" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Demo&label=&color=6A0DAD&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="demo badge"/>
  </a>
  <a href="https://www.frontendmentor.io/profile/MinhQuan2121" target="_blank">
    <img src="https://img.shields.io/static/v1?message=Frontend%20Mentor&label=&color=ff1538&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="FrontendMentor badge"/>
  </a>
</div>

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### Screenshot

![](./screenshots/FireShot%20Capture%20004%20-%20Frontend%20Mentor%20-%20FAQ%20accordion%20-%20127.0.0.1.png)

![](./screenshots/chrome-capture-2024-7-26.gif)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- BEM

### What I learned

Basic accordion css style like other beginner
```css
.faq__accordion-content {
    margin: 12px 0;
    line-height: 1.4;
    overflow: hidden;
    max-height: 0;
    transition: max-height 1s ease-in-out;
    color: var(--grayish-purple);
}

.faq__accordion-content.active {
    max-height: 500px;
}
```

Learn more about JS with chatGPT. Things i learned:
1. forEach
2. addEventListener
3. nextElementSibling
4. classList.contains (I used to use classList only)
```js
const labels = document.querySelectorAll('.faq__accordion-label');
  const accordion = document.querySelectorAll('.faq__accordion-content');
  // Function to handle the click event
  
  labels.forEach(label => {
      label.addEventListener('click', () => {
          const icon = label.querySelector('img');
          const accordionContent = label.nextElementSibling;
          accordionContent.classList.toggle('active');

          if (accordionContent.classList.contains('active')) {
              icon.src = './assets/images/icon-minus.svg'; 
          } else {
              icon.src = './assets/images/icon-plus.svg';
          }
      });
  });
```

### Continued development

<!-- Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect. -->

### Useful resources

- [Fonts Google](https://fonts.google.com/) - This helped me for free fonts. It is good for beginner and faster for a simple project.

## Author

- Website - [Minhquan721](none)
- Frontend Mentor - [@Minhquan721](https://www.frontendmentor.io/profile/MinhQuan2121)

## Acknowledgments

<p>For future development, I plan to focus on enhancing my skills in BEM and Semantic to create faster website and better performance.</p>
