# React App Guide
Get started into Frontend Web Development with React!

## Table of Contents
1. [Introduction](#introduction)
1. [Environment Setup](#environment-setup)
2. [Creating](#creating)
3. [Coding](#coding)
4. [General Tips](#general-tips)

## Introduction<a name="introduction"></a>
In this guide I will cover everything needed to design and deploy a web app using React. React is a free and open-source JavaScript library, makes it easy to use HTML and JavaScript with what is called JSX, and it is the most popular Web framework according to Stack Overflow Developer Survey 2021. 

## Environment Setup<a name="environment-setup"></a>
Install <a href="https://git-scm.com/">git</a>, <a href="https://nodejs.org/en/">Node.js</a>, and <a href="https://classic.yarnpkg.com/en/docs/install/#windows-stable">Yarn</a>. Git is used for version control, Node.js is a JavaScript runtime environment that runs JavaScript outside of the web browser, and Yarn is a dependency manager and will be used over npm.

## Creating<a name="creating"></a>
Open a terminal, if using VSCode as the IDE here is a shortcut: ```Ctrl```+```~```

Then run
```shell
yarn create react-app <NAME_OF_APP>
cd <NAME_OF_APP>
yarn start
```
with replacing <NAME_OF_APP> with whatever you want the folder to be called. This will open up a tab in your browser at ```localhost:3000```. Now you can clean up the boiler plate code, or just start coding. Now would be a good point to add this folder to a GitHub repository.

Clean up boiler plate code
https://www.youtube.com/watch?v=hT3j87FMR6M&t=435s https://www.youtube.com/watch?v=hT3j87FMR6M&t=1290s

Configure deployment: https://create-react-app.dev/docs/deployment/ keep 
```"deploy": "gh-pages -d build",```

(RECOMMENDED) Change favicon i.e. the icon that you see on the tab of your website: https://stackoverflow.com/questions/18301745/how-to-set-up-a-favicon

## Coding<a name="coding"></a>

Before coding, one should view all of the files present. Understanding index.html, index.js, package.json are important; however, you will only work with package.json most likely (for dependencies).

#### JavaScript
This is the only true coding part, and will not be too complex considering this is a guide purely for front-end.

You can use React class components, but it can be hard to understand e.g. that ```setState()``` will cause a re-render, and it is more code. I, and others, recommend and use Functional Components in React. Learn arrow functions, ```var```,```let```,```const``` (good to use const and Conditional (ternary) operator instead of returns nested in if blocks), hooks, how to export functions. Brackets and parantheses may be annoying, but you can do nice stuff with curly braces (interpolation). Some more links:

https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0

https://reactjs.org/docs/hooks-state.html
#### JSX(HTML)
Coding this part is usually not too difficult, but will involve some research on best practices e.g. alt text for images and not using button for navigation links (credit to @EddyVinckk) and reading through documentation. To make things look nice, use Material UI. You will have to run ```yarn add @material-ui/core``` followed by ```yarn``` in the base folder of the app(with package.json) which will be the same process for adding dependencies. Running ```yarn add -D @types/<DEPENDENCY_NAME>``` may be needed to help VSCode recognize the types in the dependency. Here is an example of Material UI.
```javascript 
<AppBar position="static" color="primary">
  <Typography variant="h6" noWrap>
    Material-UI
  </Typography>
</AppBar>
``` 
If you want to change the background color, modify public/index.html (also where you change favicon).
#### CSS
Keep things simple at first and use ```className```!! Using something like
```javascript
<div style={{backgroundColor:"#F0DB4F", width:"100%"}}> 
```
can be done but it is very annoying—lacks auto suggestion and makes the JSX crowded. If you are wrestling with styling, be aware of !important, overriding, and try using Inspect Element to see if any styling is crossed out.
## General Tips<a name="general-tips"></a>
It is best to go in with a plan of what you’re going to make and try to foresee issues and develop ways to ensure that you Do not Repeat Yourself (DRY). Sometimes though, it takes less time (and brainpower) to use any fancy feature, specifically for code readability or trying to keep things short.

Use custom CSS last, those are small details usually and you probably will not need to do much for formatting with CSS. HTML is where the formatting is and will be the majority of your code. 

Let Material UI or other UI framworks like Bootstrap do the heavy lifting. And if you want to implement some complex features, look for good libraries first. If you want to implement anything with transforming, transitions, it probably is CSS but you can also do a lot with JS. When you’re stackoverflow-ing you probably will search for a JS solution first.

Use Font Awesome React https://fontawesome.com/v5.15/how-to-use/on-the-web/using-with/react for icons.

“Good artists copy, great artists steal”—so take other people’s CSS >:)

Check https://search.google.com/test/mobile-friendly to quickly verify if your website is mobile-friendly

Use https://medium.com/swlh/demystifying-the-folder-structure-of-a-react-app-c60b29d90836 as a guide for naming conventions in folders, but this is not necessary until there is substantial complexity.
