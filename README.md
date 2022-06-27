# Frontend Mentor - Interactive rating component solution

This is a solution to the [Interactive rating component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-rating-component-koxpeBUmI). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Select and submit a number rating
- See the "Thank you" card state after submitting a rating

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- [React](https://reactjs.org/) - JS library
- [Styled Components](https://styled-components.com/) - For styles


### What I learned

I've learnt how to:
1. Effectively use grid and flexboxes to align the components
2. Create a transition of card flipping that can be used for future projects
```css
.flip-card {
    position: relative;
    width: 100%;
    height: 100%;
    transform-style: preserve-3d;
    transition: var(--transition);
}

.flip-card-container .flip-card {
    transform: rotateX(180deg);
}

.flip-card-front,
.flip-card-back {

    border-radius: 2rem;
    width: 90%;
    height: 90%;
    padding: 2rem;
    display: flex;
    gap: 1.5rem;
    flex-direction: column;
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    /* Safari */
    backface-visibility: hidden;
    background: var(--primary-background-grey);
}
.flip-card-back{
    align-items: center;
    text-align: center;
}

.flip-card-back {
    transform: rotateX(180deg);
}
```
3. UseState
```js
const [active, setActive] = useState();
const handleOnClick = (index) => {
    setActive(index);
  }
 <button type='button' onClick={() => handleOnClick(index)} className={active === index ? 'active btn-rating-item' : 'inactive btn-rating-item'} key={index}>{button}</button>
```
4. Mapping to create buttons
```js
 {buttons.map((button, index) => {
              return (
               //code here
              )
            })}
```


## Author

- Website - [John Ling](https://uygnis.github.io/uygnis/)
- Frontend Mentor - [@Uygnis](https://www.frontendmentor.io/profile/Uygnis)
