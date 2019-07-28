---
title: Understanding Flexbox with Cats: Part 1 Basics
published: false
tags: flexbox, css, cats, tutorial
description: The first part of "Flexbox with Cats" series of tutorials covering how to work with containers and positioning. This tutorial series will use a metaphor of cats and boxes to teach Flexbox.
cover_image: https://github.com/kefimochi/Flexbox-with-cats/blob/master/karina-vorozheeva-rW-I87aPY5Y-unsplash.jpg?raw=true
---

Everyone loves cats, right? They are adorable fluffy little beings that enjoy smashing things and not obeying anyone. Well, in this series we'll make an assumption that suddenly they will listen to all commands given the magical phrase, `display: flex;`. "Understanding Flexbox with Cats" will use the analogy of `cats and boxes` to teach concepts like the CSS box model, flexbox positioning, and provide some valuable tips on the use of containers. Please keep in mind that this series assumes that a reader already has some basic understanding of HTML and CSS.

In part one, we will mainly focus on a reader's thorough understanding of how flexbox positioning works with multiple containers. This part is for two types of people: those who never truly understood flexbox and those who love reading how someone can creatively use an analogy when connecting two seemingly unrelated things.

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

Keeping that in mind, lets set up our HTML. Right now it is important to notice that `cats`(3 images) were already placed in a `box`(div with a class of `cat-box`). You might wonder why are they all gathered in one place, well, it's time to introduce some kitten logic!

{% codepen https://codepen.io/KateEfimova/pen/NQxNVp default-tab=result %}

You see— as their default behavior, cats _love_ to cuddle. Especially considering that those kittens are in an unfamiliar environment where they were just placed seconds ago after ruining an entire apartment. They're not sure how to act, so they would just always stay close next to each other in the top left corner, warming each other up and feeling safe.

![All cat images are inside of a div container and are aligned in the top left corner](https://thepracticaldev.s3.amazonaws.com/i/gpa56eyvjawy3zy42y1o.png)

<figcaption>All cat images are inside of a div container and are aligned in the top left corner</figcaption>

## Introducing Flexbox

Cats generally consider themselves to be of high esteem, so in order for them to obey, we'll have to give a command of `display: flex;` to the box kittens are in. Someone might wonder, "why not give it to every single cat individually instead?" Well, this is because the box holds higher authority over cats due to restricting the space they can move in! And cats — being proud aristocrats — _only_ listen to higher authority. Nothing will happen if you'll try to add `display: flex;` to any of the cat images; they're very stubborn (More on the `why` later, it is related to `thinking outside of the box`! _pun intended_)

What display flex will do is tell cat images to position themselves in a row and start listening to other commands. As you just thought, they were originally positioned in a row, so the only difference that will be noticed is a lack of space between pictures.

![On the left there's a small space between pictures of cats vs on the right there's no space between cat pictures](https://thepracticaldev.s3.amazonaws.com/i/g1ovqqyv19e7vxvwemda.png)

<figcaption>On the left there's a small space between pictures of cats vs on the right there's no space between cat pictures due to added `display: flex;`</figcaption>

Now, let's pretend that a perfectionist friend comes over to your apartment, and wants to align all kittens and the box according to the center of that room. There are two directions we'll have to align them in: horizontal and vertical. Here's a well-done visual representation of the axis:

![Cross(x) vs main(y) Axis when it comes to web development](https://mdn.mozillademos.org/files/15631/align5.png)

<figcaption>Cross(x) vs main(y) Axis when it comes to web development</figcaption>

First, let's align them according to y-axis by attaching `align-items: center;` to the `.cat-box`. Then, let's also position them correctly on x-axis by adding `justify-content: center;`

![Cats that are aligned centrally on the y-axis](https://thepracticaldev.s3.amazonaws.com/i/1fe1y0tiu2ir8c56latc.png)

<figcaption>Cats that are aligned centrally on the y-axis</figcaption>
![Cats that are aligned centrally on both y-axis and x-axis](https://thepracticaldev.s3.amazonaws.com/i/rpw3nrm0gu7o6cl08iks.png)
<figcaption>Cats that are aligned centrally on both y-axis and x-axis</figcaption>

At this point, these CSS properties were added to `.cat-box`:

<pre>
  display: flex;
  align-items: center;
  justify-content: center;
</pre>

As you have probably noticed, even though cats are now aligned centrally, the box holding them is still not where it needs to be. The perfectionist friend gets upset and, not trusting you with such an "_important_" responsibility anymore, starts to mess with cat positioning himself.

Here's what he gets by trying to align all containers on the `body` of CSS by attaching the same properties we just attached to `.cat-box`

![Despite using same properties on the `body`, the box only gets aligned centrally according to x-axis](https://thepracticaldev.s3.amazonaws.com/i/n2kvatihe14xrwyv9rw8.png)

<figcaption>Despite using same properties on the `body`, the box only gets aligned centrally according to x-axis</figcaption>

What he doesn't yet realize is that all furniture and other items like Nintendo Switch and MacBook Pro were suddenly centered in the apartment too, which is definitely an unwanted behavior! It is generally considered a bad practice to attach flexbox properties to the body.

![A MacBook on the left of kittens and Nintendo Switch on the right of the kittens get aligned centrally on y-axis](https://thepracticaldev.s3.amazonaws.com/i/luue5r1h4yn4tc5o0k90.png)

<figcaption>A MacBook on the left of kittens and Nintendo Switch on the right of the kittens get aligned centrally on y-axis</figcaption>

So in order to align both kittens _and_ the box to the center of our screens, we'll have to create another `<div>` with a class of `.outer-container` and wrap it around the existing content. Why do we need that? There's no other way to manipulate the container where cat images are currently in without it, let's dive deeper into why by looking at an example!

Take a look at this dev.to component that can be found on their main page. On the right side is a demonstration of how many containers(boxes) are currently used to make it work, notice how they're nested — meaning inside each other. Light color that looks similar to a highlighter is there to portray inner padding of each container.

![Dev.to components with navigation links is broken down to several colored boxes](https://thepracticaldev.s3.amazonaws.com/i/0yn25gekow9k33tjrxnl.png)

<figcaption>Dev.to components with navigation links is broken down into several colored boxes</figcaption>

The reason why all links in a dark blue container are positioned in a column and not in a row — unlike the container that holds all icons — is because they were given a flexbox property of `flex-direction: column;`. If this property would be given to the purple container that holds all elements, than all icons

Outer box can dictate the behavior of it's children. Or, in other words, any of the elements inside of the `.outer-container` will be aligned according to the properties given. In our case the only element inside of it is an inner box with a class of `.cat-box`.

Do keep in mind that manipulations are **always** one level deep! If you haven't noticed the pattern yet: we wanted to align kittens => gave a command to their closest box, desired to manipulate that same box => created a container outside of it that wraps the whole content. You would not be able to control cats from the `.outer-container`.

<img src="https://thepracticaldev.s3.amazonaws.com/i/bzr47frhmg7w17i22gw9.png"  alt="A black text divider" height="50%" width="50%">

## Conclusion

Hopefully an analogy of using `cats and boxes` helped you to grasp concepts of flexbox better. All terminology was on purpose simplified to focus solely on the important stuff: building and understanding. Please feel free to continue researching flexbox on your own time, if you got interested in the subject. In addition, I'd love to hear your thoughts on Part 1: what did go well as well as what could have been done better? Do keep in mind that it is my first ever article written!

<center>~ Thank you for reading! ~</center>
