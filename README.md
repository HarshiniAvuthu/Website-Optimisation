## Website Performance Optimization Portfolio Project

I optimized the index.html,pizza.html,main.js to achieve at least a PageSpeed score of 90.

# Part 1: Optimize PageSpeed Insights score for index.html
* Add a print media query to print.css in
* Transfer contents of views folder to the root folder
* Create a small version of pizzera.jpg for use in index.html
* Use Web Font Loader to load the Google webfont asynchornously
* Inline css/style.css
* Use Grunt to Minify CSS, Uglify JS, Minify HTML, Optimize images

# Part 2: Optimize Frames per Second in pizza.html
* Move the document.body.scrollTop out of the loop in updatePositions
* Set the number of pizzas to 36 in document.addEventListener('DOMContentLoaded', function()
* Move the phase value calculation outside the loop and push the 5 unique phase values for each scroll to an array
* Change CSS for .mover: Add backface-visibility: hidden; transform: translateZ(0);
* Declare the var phase outside the loop to prevent it from being created each iteration.
* Move items var to avoid redefining it in updatePositions function
* Declare movingPizzas1 variable outside the loop to avoid accessing the DOM every iteration

# Part 3: Optimize Time to Resize Pizzas in pizza.html
* In the changePizzaSizes function, the randomPizzas variable was created so the querySelectorAll method only runs once outside the loop.
* Refactor the code inside the for loop in changePizzaSizes funciton to use a percentage value instead of converting it to pixels.
* Declare pizzasDiv outside the loop so it makes one DOM call only.
* Replace querySelector with the faster getElementById