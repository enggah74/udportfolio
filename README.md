## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

### Sample Portfolios

Feeling uninspired by the portfolio? Here's a list of cool portfolios I found after a few minutes of Googling.

* <a href="http://www.reddit.com/r/webdev/comments/280qkr/would_anybody_like_to_post_their_portfolio_site/">A great discussion about portfolios on reddit</a>
* <a href="http://ianlunn.co.uk/">http://ianlunn.co.uk/</a>
* <a href="http://www.adhamdannaway.com/portfolio">http://www.adhamdannaway.com/portfolio</a>
* <a href="http://www.timboelaars.nl/">http://www.timboelaars.nl/</a>
* <a href="http://futoryan.prosite.com/">http://futoryan.prosite.com/</a>
* <a href="http://playonpixels.prosite.com/21591/projects">http://playonpixels.prosite.com/21591/projects</a>
* <a href="http://colintrenter.prosite.com/">http://colintrenter.prosite.com/</a>
* <a href="http://calebmorris.prosite.com/">http://calebmorris.prosite.com/</a>
* <a href="http://www.cullywright.com/">http://www.cullywright.com/</a>
* <a href="http://yourjustlucky.com/">http://yourjustlucky.com/</a>
* <a href="http://nicoledominguez.com/portfolio/">http://nicoledominguez.com/portfolio/</a>
* <a href="http://www.roxannecook.com/">http://www.roxannecook.com/</a>
* <a href="http://www.84colors.com/portfolio.html">http://www.84colors.com/portfolio.html</a>

### Rosario Safreno's changes for P4 Web Performance Optimization
04/12/2015/04/18/2015: How I accomplished the First Stage Optimization of making sure it's 60fps:
  1. Attain a score of at least 90% in PageSpeed Insights as follows:
    * First I spent almost 3 weeks of just going through the Web Performance Optimization lessons, Google Web Performance Optimization articles, Google Web Fundamentals and Chrome Devtools tutorials.
    * I created an account with Google Analytics, obtained a token id to substitute in script tags where it is required and replaced the script with the snippet code for my token id in Google Analytics.
    * I obtained Chrome Canary and the PageSpeed Insights Chrome extension. I was able to follow the instructions to use my Android HTC One M8 where I would change my URL in Chrome Canary and it would reflect on my Android.
    * I installed and executed ngrok and python SimpleHTTP server using port 8080 per instructions from Cameron Pittman's README.md.
  1. I ran ngrok and python server and followed the suggestions from the Google Web Performance Optimization articles to submit the final project for Web Perf Optimization in order to achieve at least 90% in PageSpeed Insights:
    * I read and asked some questions from the Web Perf Optimization forum about ngrok and python.
    * I installed gulp and npm modules and created package.json and gulpfile.js to minify js, css and png/jpg files. Corrected all the errors generated by gulp for main.js.
    * I used inline CSS instead of style href to physical CSS files and substituted regular css file to use minified CSS version.
    * I used Adobe Photoshop to reduce the pixel image size and save the jpg/png files with a lesser image quality.
    * I copied the css @font-face equivalent of the googleapi web fonts and added to each of the inline css.
    * I added async to the google analytics.js.
    * I copied the javascript code from perfmatters.js and copied it inline in index.html.
  1. For the P4 project, I did the following:
    * I read the notes from the 1st launch of P4.
    * I read the questions from the forum on P4 (getting started on P4, questions on Part1 and Part2), fonts optimization, FPS metrics, Project 4-Part 2 Getting Started, etc (for the Jan '15 cohort).
    * I ran all 5 html files using the PageSpeed Insights native using ngrok and python and followed most of the suggestions that mattered most and made sure it reached a score of at least 90% such as add meta viewport,
    * Most of the minification were completed in previous step and just ran gulp in the background to watch files that changed.
    * I re-compressed png/jpg images using Adobe Photoshop by using "Save for Web". It further reduced these files to lesser kilobytes.

  1. First Stage Optimization:
    * Original main.js w/o any changes (Most of the frames were in the 30fps). I cannot paste screenshots here.
    * Updated event for addEventListener with the following:
    -Since 256 / 8 is always constant, I created a new variable, factor, and used it to compute the style.top. This way, it is not computed all the time inside the loop with factor as the variable for the Math.floor function.
    -Provided a new variable, movingPizza, to define the element movingPizzas1 outside the loop.
    -Reduced the # of iterations to generate moving pizzas from 200 to 50.
    * Updated function updatePositions() as follows:
    -Added a new variable, scrollVar, to replace the result of getting the # of pixels / 1250 when scrolling vertically. There is no need to divide it by 1250 in the loop all the time.
    -Replaced the document.body.scrollTop / 1250 with the variable scrollVar.
    -Created a new array variable, items, which contains all elements with class = ".mover" and replaced all references with items using getElementsByClassName instead of querySelectorAll. to replace with the following. I added a new variable, scrollVar, to replace the result of getting the # of pixels when vertical scroll moves.
    * Moved definition of pizzasDiv outside of the loop in the main logic.

  1. Second Stage Optimization:
    * Uupdated the function change PizzaSlices as follows:
    -Defined a new array pizzaList for all elements with class=randomPizzaContainer and replaced all its references.
    -Moved variables dx and newwidth outside of the loop since both are constant based on the size since there is only value of the size passed. After moving these values out of the loop, the time to resize pizzas measured from 200-300ms to 1.44ms.
    -Replaced all document.querySelectorAll with document.getElementsByClassName.
    -Added { backface-visibility: hidden; } under the .mover class in style.css.

### Comments
```
I wish all the documents coming from the Office Launch for P4, Ilya's instructions for the Final Project for Web Optimization Performance and the notes from the P4 Effective Optimization for 60fps would all be combined. There are so many instructions floating around that you don't know which one to follow including the README.md from Cameron Pittman portfolio repo that was forked.
```



