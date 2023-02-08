# Frontend Mentor - Profile card component solution

This is a solution to the [Profile card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- Build out the project to the designs provided

### Screenshot

![](./images/Screenshot%202022-05-01%20at%2001-26-33%20Frontend%20Mentor%20Profile%20card%20component.png)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/profile-card-component-using-bem-and-flexbox-Bkj8iVjSc)
- [Live Site URL](https://mariushor.github.io/Profile-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM

### What I learned

I am very pleased to have learned how to insert and position decorative images to my background but also for figuring out a way on my own on how to precisely position the avatar image where I wanted:

```css
.wrapper {
  background: var(--clr-dark-cyan);
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100vh;
  position: relative;
  z-index: -1;
  overflow: hidden;
}

.wrapper::before {
  content: '';
  background: url(../images/bg-pattern-top.svg);
  background-position: bottom right;
  background-repeat: no-repeat;
  transform: translate(-50%, -50%);
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: -1;
}

.wrapper::after {
  content: '';
  background: url(../images/bg-pattern-bottom.svg);
  background-position: top left;
  background-repeat: no-repeat;
  transform: translate(-50%, -50%);
  top: 100%;
  left: 100%;
  width: 100%;
  height: 100%;
  position: absolute;
  z-index: -1;
}
```
```css
.card__top {
  background: url(../images/bg-pattern-card.svg);
  height: 14rem;
  display: flex;
  justify-content: center;
}

.card__avatar {
  border: solid 0.5rem white;
  border-radius: 50%;
  width: 9.6rem;
  height: 9.6rem;
  align-self: flex-end;
  transform: translateY(50%);
  overflow: hidden;
}
```

## Author

- Frontend Mentor - [@mariusHor](https://www.frontendmentor.io/profile/MariusHor)
