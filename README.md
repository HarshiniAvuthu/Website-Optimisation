### Website Performance Optimization portfolio project

## Goal 
- To optimize a provided website with a number of optimization- and performance-related issues so that it achieves a PageSpeed score of 90 and runs at 60 frames per second.

## Installation
First of all, install the dependencies to run this website.
- NodeJS
- GulpJS

## Getting started
- Clone the repo to your local machine: $ git clone https://github.com/HarshiniAvuthu/Website-Optimisation.git
- Launch a local http server to test: $ python -m SimpleHTTPServer
- In the same directory, run the commend: ./ngrok http 8080 to access a secure public URL to the site.
- Copy the public URL given by nrok from the terminal window and paste it into your browser to view the site.
- Use Google PageSpeed Insights to check the Google PageSeed score of the homepage
- Capture a timeline session while scrolling down the page of pizza.html to check the framerate of this page.

## Optimizations Performed

I optimized the index.html,pizza.html,main.js to achieve at least a PageSpeed score of 90.

# Part 1: Optimize PageSpeed Insights score for index.html
* Added a print media query to print.css.
* Transfered contents of views folder to the root folder.
* Created a small version of pizzera.jpg for use in index.html
* Used Web Font Loader to load the Google webfont asynchornously.
* Inline css/style.css.
* Use Grunt to Minify CSS, Uglify JS, Minify HTML, compress images files.

# Part 2: Optimize Frames per Second in pizza.html
* Modified querySelector() and querySelectorAll
* Moved the document.body.scrollTop out of the loop in updatePositions.
* Set the number of pizzas to 36 in document.addEventListener('DOMContentLoaded', function())
* Changed CSS for .mover: Add backface-visibility: hidden; transform: translateZ(0);
* Declare the var phase outside the loop to prevent it from being created each iteration.
* Moved items var to avoid redefining it in updatePositions function
* Declared movingPizzas1 variable outside the loop to avoid accessing the DOM every iteration

# Part 3: Optimize Time to Resize Pizzas in pizza.html
* In the changePizzaSizes function, the randomPizzas variable was created so the querySelectorAll method only runs once outside the loop.
* Refactor the code inside the for loop in changePizzaSizes funciton to use a percentage value instead of converting it to pixels.
* Declared pizzasDiv outside the loop so it makes one DOM call only.
* Replaced querySelector with the faster getElementById.