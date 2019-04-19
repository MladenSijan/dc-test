# Task guide
> This is a guide which describes how to initialize, configure and start boilerplate code that you will use in order to complete the task that is given to you.

> Codebase is set up and managed using [Webpack4](https://webpack.js.org/)

When it comes to app functionalities, you have to enable a feature where when you click on menu icon, __sidebar should appear aside the content__ (You are given the image as a mail attachment where you can see how it should look like).

Required design for website is located in __design prototype__ folder where desktop and mobile version are provided along with style guide (font sizes and color palette).

All other requirements and information for task are provided to you via email.

**The part that you will be working on is located in *src* folder where the structure is already set up with appropriate assets and *index.html* is located in *dist* folder where it's content should be added.**

You can write all your styles in css/style.scss file and __writing it as SASS code will be considered as a plus__.

After you complete the task, you have to ZIP whole folder __EXCLUDING node_modules FOLDER__ and send it to us via email (or providing link to google drive)

## Setup

### Requirements

Node `">=5.0.0"` you can install it from [here](http://nodejs.org/)


### Clone the repository

Put this command in your terminal based on OS you are using:

*OSX & Linux*

```bash
git clone --depth 1 git@github.com:digital-cube/html-test.git && 
cd html-test && rm -rf .git && git init
```

*Windows*

```bash
git clone --depth 1 git@github.com:digital-cube/html-test.git &&
cd html-test && rd /s /q .git && git init
```

### Dependencies

To get an app working, you have to install all of it's dependencies with following command:

```bash
npm install
```

## Configuration

### Adding third party libraries (optional)


__Note that jQuery is already included in this boilerplate code by default, but you can append additional libraries if necessary__


If you want to use third party libraries, you should first install them via **npm install library_name --save**

You can provide them as plugins by registering them in __webpack.dev.config.js__ file.

In this example jQuery and momentjs are appended in PLUGINS array where you define it's alias names that will be used when you import that library in your code.


```
const PLUGINS = [
    new webpack.ProvidePlugin({
        $: 'jquery',
        jQuery: 'jquery',
        moment: 'moment',
    })
];
```


Since you have registered third party libraries in your project, you **don't have to import** them explicitly in __js/scripts.js__ file.


Now you will be able to use them with caution on ordering imports if some of them are dependent on each other.


## Running

Following command starts an app on given port, recompiles it on detected changes in code and reloads browser
```bash
npm run start
```

