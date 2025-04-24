---
layout: essay
type: essay
title: "Reuse, Reduce, Recycle"
# All dates must be YYYY-MM-DD format!
date: 2025-04-23
published: true
labels:
  - Design Patterns
  - Organization
  - Optimization
---

<img width="300px" style="float: right; margin-left: 10px; margin-bottom: 10px;" class="rounded" src="https://compote.slate.com/images/8a5bf959-9321-4a83-b960-dad1120144ac.jpeg?width=780&height=520&rect=1560x1040&offset=0x0">

## Modern problems require modern solutions...

As we developers build more complex applications, naturally, certain challenges tend to pop up again and again. I suppose we _could_ just do things the hard way, repeatedly writing tedious code from scratch and squashing the same recurring bugs over and over—essentially reinventing the wheel every single time—but why deny what makes life a hundred times easier?

That's where design patterns come in. Design patterns are reusable solutions to common problems in software design. Some examples of design patterns include:
* <b>Factory:</b> creates objects without revealing the underlying logic, like the specific class of the object being created.
* <b>Singleton:</b> acts like a global variable by providing one shared object (like a manager) that the whole program can use.
* <b>Observer:</b> defines a one-to-many dependency relationship where a change in one object (the subject) triggers updates in all dependent objects (observers)
* <b>Model-View-Controller (MVC):</b> separates an application into three parts: model (data), view (user interface), and controller (user input)

<br>
<hr>

<img width="300px" style="float: right; margin-left: 10px; margin-bottom: 10px;" class="rounded" src="https://yt3.googleusercontent.com/612AwBlYgjEci6ejL6u9rt-khLxfLcNyZuB55sTs_4SCKxHhjfVrdl9yCF5PnjZVf1hob6tv=s900-c-k-c0x00ffffff-no-rj">

##  Patterns here, there, and everywhere!

Personally, I've already been using design patterns in my code without even realizing it at first. They are especially prevalent in bigger projects like [Cooking Compass](https://github.com/Cooking-Compass), which combines Next.js with React Bootstrap for structure and styling. This is a good example of MVC, where the model is the database, the view is what the user sees via the React and Bootstrap components, and the controller is everything that handles what happens when the user clicks a button (and other user interactions).

Cooking Compass also uses the Observer pattern. When the user submits a recipe, the app needs to update what the recipe list displays. The Observer pattern allows the recipe list (the observer) to automatically update whenever the data (the subject) changes, ensuring that the user sees the most up-to-date list without needing to refresh the page manually.

Ultimately, I've found that using design patterns like MVC and Observer in the development of Cooking Compass keeps the app organized and easy to maintain. It enhances the overall user experience, making sure everything runs smoothly as the project grows.
