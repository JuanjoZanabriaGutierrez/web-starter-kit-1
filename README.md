[![Web Starter Kit](https://user-images.githubusercontent.com/25930200/63020667-68e27c00-bea7-11e9-8047-a9d595ad9c1a.jpg)](https://github.com/justcoded/web-starter-kit/releases)

>  A modern Web starter kit for projects

![node](http://img.shields.io/badge/node-8.0.x-blue.svg) ![npm](https://img.shields.io/badge/npm-5.0.x-blue.svg)  [![release](https://img.shields.io/github/release/justcoded/web-starter-kit.svg)](/releases) ![SCSS](http://img.shields.io/badge/SCSS-3.x.x-c6538c.svg) [![travis](https://img.shields.io/travis/justcoded/web-starter-kit.svg)](https://travis-ci.org) [![license](http://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) [![license](http://img.shields.io/badge/autoprefixer-included-blue.svg)](https://www.npmjs.com/package/autoprefixer) [![readme](http://img.shields.io/badge/readme-md-blue.svg)](/README.md) [![requests](http://img.shields.io/badge/PRs-welcome-green.svg)](/pulls)


## Overview

Web Starter Kit (WSK) - is an opinionated boilerplate for web development. Tools for building a great experience across many devices. A solid starting point for both professionals and newcomers to the industry.

## Table of Contents
1. [Browser Support](#browser-support)
2. [Features](#features)
3. [Install](#install)
4. [Quickstart](#quickstart)
5. [Getting the code](#getting-the-code)
6. [Prerequisites](#prerequisites)
7. [Commands](#commands)
8. [Structure](#structure)
9. [Templating](#templating)
10. [Styles](#styles)
11. [JavaScript](#javascript)
12. [Tasks](#tasks)
13. [Troubleshooting](#troubleshooting)
14. [Contributing](#contributing)
15. [License](#license)


## Browser Support

At present, we officially aim to support the last two versions of the following browsers:

* Chrome
* Edge
* Firefox
* Safari
* iOS
* Android 5+

This is not to say that WSK cannot be used in browsers older than those reflected, but merely that our focus will be on ensuring our layouts work great in the above.


## Features

| Feature | Summary |
| --- | --- |
| Easy start | We don't use responsive boilerplate. You are free to make your own decision in what way to make responsive for the site. Just start with `index.html` from `src/html`. |
| HTML templating | Used [gulp-file-include](https://github.com/haoxins/gulp-file-include) for templating html files. |
| Sass support | Compile [Sass](http://sass-lang.com/) into CSS with ease, bringing support for variables, mixins and more (run `gulp` for project compiling). In our WSK we use [Dart-Sass](https://sass-lang.com/dart-sass) version compiler and follow [Sass guidelines](https://sass-guidelin.es/#architecture). |
| PostCSS support | PostCSS connecting most usable plugins library for CSS optimisation. In our WSK we use [autoprefixer](https://github.com/postcss/autoprefixer), [cssnano](https://github.com/cssnano/cssnano), [sort-css-media-queries](https://github.com/solversgroup/postcss-sort-media-queries), etc. |
| JavaScript ES6+ Support | Optional JavaScript ES6+ support .You can use all kind of ES6+ features here. ES6+ source code will be automatically transpiled to ES5 for wide browser support. For bundling and transpiling used [Browserify](http://browserify.org/) and [Babel](https://babeljs.io/). |
| Code Linting | JavaScript code linting is done using [esLint](https://www.npmjs.com/package/gulp-eslint) - a linter tool for identifying and reporting on patterns in JavaScript (used [airbnb-base rules](https://www.npmjs.com/package/eslint-config-airbnb-base)). HTML code linting is done using [HTMLHint](https://github.com/htmlhint/HTMLHint). |
| Performance optimization | Minify and concatenate JavaScript, CSS, HTML and images to help keep your pages lean (run `gulp` to create an optimised version of your project to `assets`). |
| Built-in HTTP Server | A built-in server for previewing your site locally while you develop and iterate. |
| Live Browser Reloading | Reload the browser in real-time anytime an edit is made without the need for an extension (run `gulp` and edit your files). |
| Cross-device Synchronization | Synchronize clicks, scrolls, forms and live-reload across multiple devices as you edit your project. Powered by [BrowserSync](http://browsersync.io) (run `gulp` and open up the IP provided on other devices on your network). |


## Install

Init your project using [jcn](https://github.com/justcoded/npm-jcn) or directly [download WSK](https://github.com/justcoded/web-starter-kit/releases/latest) and run `$ npm install --global gulp && npm install` in that directory to get started.


To take advantage of WSK you need to:

1. Download the code.
2. Install all necessary dependencies if you don't already have them.
3. Modify the application as you wish.
4. Make the production of your code.

This starter wasn't tested on Linux. If you want to use it on Ubuntu 17 type these commands in a command terminal:
```sh
$ sudo snap install node --classic --channel 6/stable
```
```sh
$ npm install gulpjs/gulp-cli -g
```

## Quickstart

Init your project using [jcn](https://github.com/justcoded/npm-jcn) or  [download](https://github.com/justcoded/web-starter-kit/releases/latest) the kit from this repository and build on what is included in the `assets` directory.

You can start from `src/html` - the default starting point, with template text.

Be sure to look over the [installation](#install) to verify your environment is prepared to run Web Starter Kit.
Once you have verified that your system can run WSK, check out the [commands](#commands) available to get started.


## Getting the code

[Download](https://github.com/justcoded/web-starter-kit/releases/latest) and extract WSK to the place where you want to work.

## Prerequisites

### [Node.js](https://nodejs.org)

Bring up a terminal and type `node --version`.
Node should respond with a version at or above 8.0.x.
If you need to install Node, go to [nodejs.org](https://nodejs.org) and click on the big green Install button.

### [Gulp](http://gulpjs.com)

Bring up a terminal and type `gulp --version`.
If Gulp is installed it should return a version number at or above 4.0.x.
If you need to install/upgrade Gulp, open up a terminal and type in the following:

```sh
$ npm install --global gulp
```

*This will install Gulp globally. Depending on your user account, you may need to [configure your system](https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md) to install packages globally without administrative privileges.*


### Local dependencies

Next, install the local dependencies WSK requires:

```sh
$ npm install
```

That's it! You should now have everything needed to use the WSK.  
You may also want to get used to some of the [commands](#commands) available.


## Commands

There are few commands available to help you build and test sites:

### Watch For Changes & Automatically Refresh Across Devices

```sh
$ gulp
```

`gulp` task creates the `assets` folder in the root of the project.
This includes linting as well as image, script, stylesheet and HTML optimization.
Also, a [browsersync](https://browsersync.io/) script will be automatically generated, which will take care of precaching your sites resources.


### Serve the Fully Built & Optimized Site

```sh
$ gulp build
```

`gulp build` task creates the `production` folder in the root of the project with **minifying** files from `assets`. It will help you to create clear instances of code for the **production** or **further implementation**.


### Lint only

```sh
$ gulp lint-js
```

`gulp lint-js` task run the separate lint for JS files.

## Structure

If you want to use our WSK, you need to know something about the structure.  
Your folder structure for WSK:

```
├── assets              #Folder with files after compiling
├── src                 #Folder with sources
├── sys_icon            #Folder with system icons for notification
├── tasks               #Folder with tasks for gulpfile
├── .browserslistrc     #Config for autoprefixer
├── .editorconfig       #Config for IDE
├── .eslintignore       #Eslint ignore list
├── .eslintrc           #Config for eslint
├── .gitattributes      #Git config for defining attributes per path
├── .gitignore          #Git ignore list
├── .htaccess           #Config file of Apache web service
├── .travis.yml         #Config file of service for building and testing projects hosted at GitHub
├── CONTRIBUTING.md
├── gulp-config.js      #Config for gulp
├── gulpfile.js         #File with gulp tasks
├── LICENSE
├── package.json        #File with dependencies
└── README.md
```
 
In `package.json` you can find all the dependencies. Folder `tasks` - for gulpfile tasks. In `src` folder you can find all sources for the project (images, html, sass, javascript files).

### `src` folder structure

```
├── html
   ├── partials                #Folder for html components, that we can include into the templates
   ├── templates               #Folder for source html templates of pages
├── images                     #Folder for storing images
├── js                         #Folder for storing js files
   ├── modules                 #Folder for storing js modules
   ├── app.js                  #Main js file
├── scss
   ├── abstracts               #Folder for storing scss files
      ├── functions.scss       #Sass functions
      ├── helpers.scss         #Style helpers
      ├── main.scss            #Main file to import abstracts styles (used for importing another files)
      ├── mixins.scss          #Sass mixins
      ├── variables.scss       #Sass variables & CSS custom properties that we can use in project
   ├── base                    #Folder for storing base styles
      ├── forms.scss           #Styles for forms
      ├── main.scss            #Main file to import base styles (used for importing another files)
      ├── reset.scss           #Styles reset
      ├── typography.scss      #Styles for text
   ├── components              #Global Reusable Presentational Components
   ├── layout                  #Global layout
   ├── pages                   #Global styles for pages
   ├── styles.scss             #Main file to import project styles (used for importing another files)
├── vendor_entries             #Folder for vendor entries (plugins)
   ├── vendor.js               #File for plugins js
   ├── vendor.scss             #File for plugins styles
```

Use `images` folder to add your graphic files, `modules` to add your javascript modules (don't forget to include it in app.js), `scss` folder to add your styles for the project. You can create, delete files and folders in `scss`, but don't forget to include them in `scss/styles.scss` file .

Use `vendor_entries` to include plugins into your project.

## Templating

In our WSK you can use [gulp-file-include](https://github.com/haoxins/gulp-file-include) for **templating html** files. It's simple, just see [example](https://github.com/haoxins/gulp-file-include#examples) or demo example in our WSK folder `src/html`.

## Styles

In our WSK you can use [Sass](http://sass-lang.com/) ([Dart-Sass](https://sass-lang.com/dart-sass) version compiler). Sass is the most mature, stable, and powerful professional grade CSS extension language in the world.

Sass is a CSS preprocessor — a layer between the stylesheets you author and the .css files you serve to the browser. Sass (short for Syntactically Awesome Style Sheets) plugs the holes in CSS as a language, allowing you to write DRY code that’ll be faster, more efficient, and easier to maintain. In our WSK we follow [Sass guidelines](https://sass-guidelin.es/#architecture).

So while normal CSS doesn’t yet allow things like variables, mixins (reusable blocks of styles), and other goodies, Sass provides a syntax that does all of that and more—enabling “super functionality” in addition to your normal CSS.

* All custom **sass** files locate in `src/scss/` folder;
* Entry point is `src/scss/styles.scss` you can **import** all your `.scss` files from here;
* All **extensions** must be installed by the [npm](https://docs.npmjs.com/cli/install);
* After installing the extension you must **include** its **css** or **sass** files in `src/vendor_entries/vendor.scss` using `@import`.

You are able to add your own **custom sass files** and optionally **disable/enable** [postcss-sort-css-media-queries](https://github.com/solversgroup/postcss-sort-media-queries).
You can see this property `getPathesForStylesCustom` in the `gulp-config.js` file:

![image](https://user-images.githubusercontent.com/38295556/72220657-88b3c400-355b-11ea-90d7-4cbb5edb0f43.png)

Please don't forget to link all your **styles custom files** in **html** file:

![image](https://user-images.githubusercontent.com/38295556/72220723-4b036b00-355c-11ea-841a-ce218c304aed.png)

Also, you might want to add files to the ignore list (check `getPathesToCopyForProduction` and `getPathesToCopy` properties in the `gulp-config.js` file). By default they will be copied to the `assets` and `production` folders.

In our WSK you can use [PostCSS](https://postcss.org/). PostCSS is a tool for transforming CSS with JavaScript. Currently, PostCSS has more than 200 plugins. You can find all of the plugins in the [plugins list](https://github.com/postcss/postcss/blob/master/docs/plugins.md).

* You **don't need** to write **prefixes** for different browsers like `-webkit` it will be done by the [autoprefixer](https://github.com/postcss/autoprefixer).

In **production** mode we use:

* **Group and sort CSS media queries** by [sort-css-media-queries](https://github.com/solversgroup/postcss-sort-media-queries). By **default** we use `desktop-first` sorting type, but you can change it in `gulp-config.js` to `mobile-first`.
* **Minifying** `.css` files by [cssnano](https://github.com/cssnano/cssnano).

## JavaScript

 In our WSK you can use ES6+. ES6+ isn't introducing anything other than improvements to the JavaScript language and a few new features.

 It is not an alternative syntax or language like CoffeeScript or TypeScript. It's good ol' fashioned JavaScript. The reason so many people are excited is that this version introduces a lot of much-needed improvements to the language.

 For bundling and transpiling `.js` files in our WSK we used [Browserify](http://browserify.org/) and [Babel](https://babeljs.io/).

* All custom **javascript** files are located in `js` folder;
* Entry point for javascript is `src/js/app.js` you can **import** all your **javascript** files from here using [ES6 import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import) feature;
* All **javascript** is **babelified** so yes! You can use all kind of [ES6 features](https://babeljs.io/docs/learn-es2015/) here.
* All **extensions** must be installed by the [npm](https://docs.npmjs.com/cli/install);
* After installing the extension you must **include** its **javascript** files in `src/vendor_entries/vendor.js` by adding new elements to the **array**.

In **production** mode we use:

* **Uglifying** `.js` files by [uglifyJS](https://github.com/mishoo/UglifyJS2).

## Tasks

| Task | Description |
| --- | --- |
| browser-sync-server | Browsersync can watch your files as you work. Changes you make will either be injected into the page (CSS & images) or will cause all browsers to do a full-page refresh. |
| build-html | Compiles all html templates into html files. |
| build-js | Compiles all js from `src/js` to `assets/js` folder. |
| build-js-vendors | Compiles all vendor js from `src/vendor_entries` to `assets/js` folder. |
| build-styles | Compiles all scss from `src/scss` to `assets/css`   folder. |
| build-styles-custom | Compiles all custom scss files listed in the `gulp-config.js` to `assets/css` folder |
| build-styles-vendors | Compiles all vendor styles from `src/vendor_entries` to `assets/css`   folder. |
| clean-build | Cleaning `assets` folder. |
| clean-production | Cleaning `production` folder. |
| copy-folders-production | Copy all folders & files from `assets` to `production`. |
| copy-folders | Copy all not compiling files & folders from `src` to `assets`. |
| lint-html | Need to lint html files. |
| lint-js | Need to lint js files. |
| image-min | We use this to minify images. |
| watch | Task for watching all the changes. |

## Troubleshooting

If you find yourself running into issues during installation or running the tools, please check our [Troubleshooting](https://github.com/justcoded/web-starter-kit/wiki/Troubleshooting) guide and then open an [issue](https://github.com/justcoded/web-starter-kit/issues). We would be happy to discuss how they can be solved.


## Contributing

Contributions, questions and comments are all welcome and encouraged. For code contributions to Web Starter Kit, please see our [Contribution guide](CONTRIBUTING.md) before submitting a pull request. [Website](https://github.com/justcoded/web-starter-kit) related issues should be filed on the [Web Fundamentals](https://github.com/justcoded/web-starter-kit/issues) issue tracker.

## License

The MIT License (MIT).

Copyright (c) 2020 JustCoded the IP provided on other devices on your network.
