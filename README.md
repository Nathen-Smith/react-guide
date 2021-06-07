# React App Guide

## Creating
https://reactjs.org/docs/create-a-new-react-app.html

Configure deployment: https://create-react-app.dev/docs/deployment/

(RECOMMENDED) Change favicon, aka the icon that you see on the tab of your website: https://stackoverflow.com/questions/18301745/how-to-set-up-a-favicon

Support mobile viewing (one liner!)
https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag

Support smooth scrolling
https://gomakethings.com/smooth-scrolling-links-with-only-css/

## Coding
#### JavaScript
You can use class components, but it can be hard to understand e.g. that ```setState()``` will cause a re-render, and it is more code. I, and others, recommend and use functional JS (include "ES6" when looking for documentation). Learn arrow functions, ```var```,```let```,```const``` (good to use const and Conditional (ternary) operator instead of returns nested in if blocks), hooks, how to export functions. Brackets and parantheses may be annoying, but you can do nice stuff with curly braces (interpolation). Some more links:

https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0

https://reactjs.org/docs/hooks-state.html
#### HTML
Should be pretty intuitive and won't require much work here, main difference here is you often do not need to worry about classes if you want to, just use Bootstrap https://react-bootstrap.github.io/getting-started/introduction to take care of things e.g. 
```javascript 
<Navbar bg="light" expand="lg">
``` 
vs 
```javascript
<nav class="navbar navbar-expand-lg navbar-light bg-light">
```
Plus, Bootstrap comes with nice pre-made styles. Also remember to use Inspect Elements to help debug! If you want to change the background color, modify public/index.html (also where you change favicon and other things.
#### CSS
Don’t go down a rabbit hole. Just keep things simple at first and use ```className```!!! Using something like
```javascript
<div style={{backgroundColor:"#F0DB4F", width:"100%"}}> 
```
can be done but it is very annoying—lacks auto suggestion and things like rgba (there is a workaround but it is ugly). In short, only use inline if absolutely necessary. Here is an example: https://github.com/Nathen-Smith/personal-site/blob/main/src/components/Links.js#L61-L73. If you are wrestling with styling, be aware of !important, overriding, and try using Inspect Element to see if any styling is crossed out.
## General Tips
It is best to go in with a plan of what you’re going to make and try to foresee issues and develop ways to ensure that you Do not Repeat Yourself (DRY). Sometimes though, it takes less time (and brainpower) to use any fancy feature, specifically for code readability or trying to keep things short. Remember to not optimize last, if you even need to. 

Use virtual environment.

Use custom CSS last, those are small details usually and you probably will not need to do much for formatting with CSS (just like art save details for last). HTML is where the formatting is and will be the majority of your code. 

Let Bootstrap do the heavy lifting. And if you want to implement some complex features, look for good libraries first, or make your own hook e.g. https://github.com/Nathen-Smith/personal-site/blob/main/src/shared-hooks/useScreenType.js (credit to benawad). If you want to implement anything with transforming, transitions, it probably is CSS but you can also do a lot with JS. When you’re stackoverflow-ing you probably will search for a JS solution first.

Use Font Awesome React https://fontawesome.com/v5.15/how-to-use/on-the-web/using-with/react for icons.

“Good artists copy, great artists steal”—so take other people’s CSS >:)
