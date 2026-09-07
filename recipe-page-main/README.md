# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)


**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- Your challenge is to build out this recipe page and get it looking as close to the design as possible.

### Screenshot

![](./assets/images/recipe%20page.%20png.png)


### Links

- Solution URL: [GitHub repository](https://github.com/iggysav/FrontMentor/tree/master/recipe-page-main)
- Live Site URL: [Live site](https://iggysav.github.io/FrontMentor/recipe-page-main)


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox


### What I learned

Understood that heading hierarchy (```h1```–```h6```) reflects document outline, not visual size. For example, all major sections use ```<h2>```, and visual differences are controlled via CSS.
Used ```<strong>``` for meaningful emphasis (not just bold styling), separating content from presentation.

Fought with card width and learned that block elements stretch to their parent width.
Solutions:
```display: inline-block``` + ```width: min-content``` (but text may break out).
```display: table``` (more predictable).
Final choice: fixed widths with fluid ```clamp()``` for full control.
Used ```box-sizing: border-box``` to include padding in width calculations.

Custom list markers:
Styled markers with ```::marker``` (color, size, font-weight).
Discovered that ```transform``` on ```::marker``` has limited support, so I used custom ```::before``` with absolute positioning as a fallback (though in the end ```::marker``` worked for my use case).

Great!!! Yehhh!!! Fluid responsive design with ```clamp()```:
Replaced fixed breakpoints with linear interpolation using ```clamp()```.
Learned to compose formulas:
```clamp(Vmin, calc(Vmin + (100vw - Wmin) * (Vmax - Vmin) / (Wmax - Wmin)), Vmax)```
Created an image overflow effect on mobile using a CSS variable:
```--image-overflow``` expands the image beyond card edges with smooth transition.


### Continued development

- Practice more advanced responsive techniques (container queries, subgrid).

 - Improve accessibility (focus indicators, ARIA attributes).

- Explore CSS animations and transitions for micro-interactions.

- Learn to use CSS clamp() in combination with custom properties for more complex fluid systems.


### AI Collaboration

I used ChatGPT as a learning assistant, as suggested in AGENTS.md. Throughout this project, an AI assistant acted as a coding mentor, helping me:

- Solve layout problems — such as centering the card and preventing it from stretching.

- Build a fluid responsive design — using clamp() with linear interpolation for smooth scaling.

- Refactor repetitive code — extracting common styles and using CSS variables.

The assistant encouraged me to think independently, asked guiding questions, and provided hints rather than giving complete solutions — which helped me learn more deeply.

## Author

- Frontend Mentor - [@iggysav](https://www.frontendmentor.io/profile/iggysav)
- Linkedin - [Linkedin](https://www.linkedin.com/in/savastsiuk-igor-527a1089/)

