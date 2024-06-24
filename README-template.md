# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

-It is a template with three columns, its information is based on data about cars.

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./images/desktop.png)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

-My process was dynamic, I learned to solve the distribution of columns, and create transparency in the buttons. also color separation.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library
- [Next.js](https://nextjs.org/) - React framework
- [Styled Components](https://styled-components.com/) - For styles

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->

  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
  
  <link rel="stylesheet" href="./style.css">
    
  <title>Frontend Mentor | 3-column preview card component</title>
</head>
<body>
  
<main>
  <div class="container">
    <section class="wrapper">
      <div class="content sedans">
          <img src="./images/icon-sedans.svg" alt="icon-sedans">
          <h1> Sedans</h1>
          <p>Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city 
            or on your next road trip.</p>
          <button class="btn btn-sedans">Learn more</button>
      </div>

      <div class="content suvs">
        <img src="./images/icon-suvs.svg" alt="icon-suvs">
        <h1>SUVs</h1>
        <p>Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation 
          and off-road adventures.</p>
          <button class="btn btn-suvs">Learn more</button>
    </div>

    <div class="content luxury">
      <img src="./images/icon-luxury.svg" alt="icon-luxury">
      <h1>luxury</h1>
      <p>Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury 
        rental and arrive in style.</p>
        <button class="btn btn-luxury">Learn more</button>
     </div>
    </section>
  </div>

  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="#">ElianaRestrepo99</a>.
  </div>
</main>

</body>
</html>
```
```css
@import url('https://fonts.googleapis.com/css2?family=Lexend+Deca:wght@100..900&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@100.. 900&display=swap');


*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body{
    font-family: 'Lexend Deca',serif;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    height: 100vh;
    background-color: hsl(0, 0%, 95%) ;
    padding: 1rem;
}

.btn{
    color: hsl(179, 100%, 13%);
    border-radius: 50px;
    padding: .8rem 1.5rem;
    font-family: 'Big Shoulders Display',sans-serif;
    border: 2px solid hsl(0, 0%, 95%);
}


.container{
    max-width: 900px;
    background-color: hsl(0, 0%, 95%);
    padding: 1rem;
    margin: auto;
}

.wrapper{
    background-color:hsl(31, 77%, 52%);
    display: flex;
    border-radius: 1rem;
    overflow: hidden;
}

.wrapper .content{
    padding: 3rem 2.5rem;
}

.wrapper .sedans{
    background-color: hsl(31, 77%, 52%)s ;
}

.wrapper .suvs{
    background-color: hsl(184, 100%, 22%);
}

.wrapper .luxury{
    background-color: hsl(179, 100%, 13%);
}

.wrapper .content h1{
    color: #ffff;
    text-transform: uppercase;
    font-size: 2.5rem;
    font-weight: 700;
    font-family: Big Shoulders Display, serif;
    margin: 1.5rem 0;
}

.wrapper .content p{
    color: hsla(0, 0%, 100%, 0.75);
    font-size: 1rem;
    margin-bottom: 3rem;
    line-height: 1.5;
}

.wrapper .btn.btn-sedans{
    color: hsl(31, 77%, 52%);
}

.wrapper .btn.btn-suvs{
    color: hsl(184, 100%, 22%);
}

.wrapper .btn.btn-luxury{
    color: hsl(179, 100%, 13%);
}

.wrapper .btn.btn-sedans:hover,
.wrapper .btn.btn-suvs:hover,
.wrapper .btn.btn-luxury:hover{
    background-color: transparent;
    color: hsl(0, 0%, 95%);
}

@media screen and (max-width: 780px) {
    
    .body{
        height: calc(100vh -1%);
    }

    .container{
        min-width: 500px;
        margin: auto;
    }

    .wrapper{
        flex-direction: column;
    }

    .btn{
        margin: 0;
    }

    .wrapper .content p{
        margin: 2rem 0;
    }
}



.attribution { 
    font-size: 11px; 
    text-align: center;
 }

.attribution a { 
    color: hsl(179, 100%, 13%);
}
```
```js
const proudOfThisFunc = () => {
  console.log('🎉')
}
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
