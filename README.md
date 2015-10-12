## Website Performance Optimization portfolio project

The challenge was to optimize this online portfolio for speed. In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To see the final result, visit [Optimized website](https://rawgit.com/javipascual/frontend-nanodegree-mobile-portfolio/master/index.html)

### Optimizations applied

* **index.html**

  * add attribute `media=print` to stylesheet print.css
  * add async to embedded script and to google analytics script
  * move style.css and fonts to the end

* **views/js/main.js**

  * function `updatePositions` optimized:
    - move document.body.scrollTop out of the loop
  * function changeSize optimized:
    - document query `document.querySelectorAll(".randomPizzaContainer")` factored out of the loop
    - function `determineDx` removed
  * number of sliding pizzas based on the size of the window

* **views/pizza.html**

  * css files moved to the bottom of the html
