---
title: Understanding Flexbox with Cats: Part 1 Basics
published: false
tags: flexbox, css, cats, tutorial
description: The first part of "Flexbox with Cats" series of tutorials covering how to work with containers and positioning. This tutorial series will use a metaphor of cats and boxes to teach Flexbox.
cover_image: https://github.com/kefimochi/Flexbox-with-cats/blob/master/karina-vorozheeva-rW-I87aPY5Y-unsplash.jpg?raw=true
---

Everyone loves cats, right? They are adorable fluffy little beings that enjoy smashing things and not obeying anyone. Well, in this series we'll make an assumption that suddenly they will listen to all commands given the magical phrase, `display: flex;`. "Understanding Flexbox with Cats" will use the analogy of `cats and boxes` to teach concepts like the CSS box model, flexbox positioning, and some valuable tips on the use of containers(aka "boxes", aka "divs"). Please keep in mind that this series assumes that a reader already has some basic understanding of HTML and CSS functionality.

In part one, we will mainly focus on a reader's thorough understanding of how flexbox positioning works with multiple containers. Covering margins, borders, paddings, relative width & height, as well as flex properties like `flex-direction`, `align-self`, and `justify-content`.

<center>~ Please enjoy this article full of kitten logic! ~</center>
<img src="https://github.com/kefimochi/Flexbox-with-cats/blob/master/MyCat.png?raw=true" height="200" width="200" alt="An illustration of a black cat staring at you">

### "Flexbox with Cats" Contests

- [Part 1: Flexbox basics](https://dev.to/kefimochi/understanding-flexbox-with-cats-part-1-1nah-temp-slug-8615884?preview=c73c442aaa9309c1cde8720742d43900fd95cf84461ad1cd51e51aac752140bc22e5682dcae9b0d080323f28eaf4c926a9752cdbfcbce5ad141b3b94)
  - Beginner-friendly introduction to CSS's box model, positioning of divs, and covering concepts such as `margin vs padding vs border`.
- Part 2: Think in "boxes"
  - An article describing how to recognize containers("divs") when working with a provided design and how to implement the desired positioning.
- Part 3: Advanced Flexbox and CSS
  - Covering everything from using flexbox in order to make a website responsive all the way to how to create your own designs. We'll also get to look at real-world implementations of everything learned throughout this series.

<img src="https://thepracticaldev.s3.amazonaws.com/i/bzr47frhmg7w17i22gw9.png"  alt="A black text divider" height="50%" width="50%">

## Introduction to "Cats and Boxes"

![Cat's face looking deeply into your soul from inside of a box](https://thepracticaldev.s3.amazonaws.com/i/04tkt4ec6pmgu5zxv731.jpg)

<figcaption>Cat's face looking deeply into your soul from inside of a box</figcaption>

Let's imagine a situation where suddenly you found yourself being responsible for three little kittens. As you see your apartment slowly turning into a disordered mess due to those tiny energized cats walking all over the place—and scratching on surfaces they shouldn't be scratching—you slowly begin to panic. What's a possible solution to all this chaos? 🤔

If you thought about trying to limit cats' space, you were correct! Just like in real life, we first have to set up a `box`(also known as a `<div>` element) before putting any `cats`(representation for any content, like images, text, lists, etc) into it. It would not make sense to first put kittens on the ground and then add a box on top of them, so try to avoid doing that when using flexbox too!

## Setting up a Default Box

Keeping that in mind, lets set up our HTML. Right now it is important to notice that `cats`(3 images) were already placed in a `box`(div with a class of `cat-box`). Notice an added class of a `cat-box` on the `div` container, it is there so we could manipulate it later with CSS. You might wonder why are they all gathered in one place, well, it's time to introduce some kitten logic!

{% codepen https://codepen.io/KateEfimova/pen/NQxNVp default-tab=result %}

You see— as their default behavior, cats _love_ to cuddle. Especially considering that those kittens are in an unfamiliar environment where they were just placed seconds ago after ruining an entire apartment. They're not sure how to act, so they would just always stay close next to each other in the top left corner, warming each other up and giving an occasional bite from time to time.

![All cat images are inside of a div container and are aligned in the top left corner](https://thepracticaldev.s3.amazonaws.com/i/gpa56eyvjawy3zy42y1o.png)

<figcaption>All cat images are inside of a div container and are aligned in the top left corner</figcaption>

## Introducing Flexbox

Now that all three kittens are preset in the box, it's time to have some fun and begin manipulations! Cats generally consider themselves to be of a high esteem, so in order for them to obey, we'll have to give a command of `display: flex;` to the box. Someone might ask: why not give it to every single cat individually instead? Well, that is because the box has even a higher ranking than cats since from the beginning it was restricting them! And cats — being proud aristocrats — _only_ listen to higher authority. Nothing will happen if you'll try to add `display: flex;` to any of the kittens.

Let's pretend that a perfectionist friend comes over to your apartment, and wants to align all kittens and the box according to the center of that room. There are two directions we'll have to align them in: horizontal and vertical. Here's a well-done visual representation of the axis:

![Cross(x) vs main(y) Axis when it comes to web development](https://mdn.mozillademos.org/files/15631/align5.png)

<figcaption>Cross(x) vs main(y) Axis when it comes to web development</figcaption>

### Aligning by Y-axis

![Cross(x) vs main(y) Axis when it comes to web development](https://thepracticaldev.s3.amazonaws.com/i/1fe1y0tiu2ir8c56latc.png)

<figcaption>Cross(x) vs main(y) Axis when it comes to web development</figcaption>

At this point, our `cat-box` class has these CSS properties:

<img src="https://thepracticaldev.s3.amazonaws.com/i/bzr47frhmg7w17i22gw9.png"  alt="A black text divider" height="50%" width="50%">

## Conclusion

Hopefully an analogy of using `cats and boxes` helped you to better grasp concepts of flexbox. All terminology was on purpose simplified to focus solely on the important stuff: building and understanding. Please feel free to continue researching flexbox on your own time if you got interested in the subject. In addition, I'd love to hear your thoughts on Part 1: what did I do well as well as what could have been done better?

<center>~ Thank you for reading! ~</center>
