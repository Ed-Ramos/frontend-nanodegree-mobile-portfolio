##Front End Web Developer- Website Performance Optimization Project

This project is comprised of two parts. Part 1 is to optimize a given website by shorten the critical rendering path and achieving a pagespeed score of at least 90 for Mobile and Desktop. Part 2 of this project, is to optimize JS code used by pizza site such that we achieve 60fps while scrolling and be able to resize pizza in less than 5ms when using pizza size slider.

####Part 1: Optimize PageSpeed Insights score for index.html
To accomplish this part of project, I performed the following: Minified print and style CSS files, Minified perfmatters JS file, Inlined style.css, added media = “print” to print.css link, added “async” to google analytics.com script, resized and compressed pizzeria.jpg, and compressed profilePic.jpeg
To verify PageSpeed score, I hosted page on github. The page address is (http://ed-ramos.github.io/frontend-nanodegree-mobile-portfolio). . To see results, add this address to Google’s PageSpeed Insights page located at (https://developers.google.com/speed/pagespeed/insights/)
For simplicity, I placed all source files that were edited in the src folder. I added “Orig” to files name

####Part 2: Optimize Frames per Second in pizza.html
To accomplish this part of project, I first used Chrome’s Dev Tools to record measurements as I scrolled through page and used the pizza size slider.
On the ChangePizzaSizes function, replaced querySelectorAll method with the more efficient getElementsbyClassName method.  calculate the dx and newwidth variables outside of the for loop as its values does not change as i changes.  Also, create variables outside of for loop so that document is referred to once and not multiple times inside loop.
On the UpdatePositions function,  calculate the five unique phase values outside of main for loop and place them in an array. Replaced querySelectorAll method with the more efficient getElementsbyClassName method. Create variable outside of loop so that document is accessed once and not multiple times.
Finally, changed code so that instead of 200 sliding pizza being generated when page loads, only 40 are generated. This should cover the number of pizzas that are visible on screen.
