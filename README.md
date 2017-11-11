# Katamino Polymer

Katamino is a superb puzzle and a challenging game.

[Check out the DEMO](https://katamino-polymer.firebaseapp.com/)

## How the game works

The game consists of 12 different pieces constructed of right angled blocks so each piece is made of 5 "squares". (Think Tetris pieces, but 5 squares instead of 4.)

The gameboard is constructed with a movable divider so one can take sets of 4 up to the whole set of 12 pieces and form them into a 5 block by X rectangle. (Where X = the number of wood blocks in your set.)

The two or three player strategy game is accomplished on a square board divided into 64 smaller squares. Players take turns to place a piece on the gameboard. The first player who cannot place a piece anymore loses. (Similar to Blokus)

The two player puzzle game mode is accomplished by dividing the board into two sections, each player chooses five blocks and are also given 4 small "filler" blocks of 1 and 2 squares. The first one to fit all their blocks perfectly into their half of the rectangle board, wins.


## Setup

##### Prerequisites

First, install [Polymer CLI](https://github.com/Polymer/polymer-cli) using
[npm](https://www.npmjs.com) (we assume you have pre-installed [node.js](https://nodejs.org)).

    npm install -g polymer-cli
    
Second, install [Bower](https://bower.io/) using [npm](https://www.npmjs.com)

    npm install -g bower
    
##### Initialize project from git

Clone this repo

    git clone https://github.com/axax/katamino-polymer.git

Run bower install 

    bower install

### Start the development server

This command serves the app at `http://127.0.0.1:8081` and provides basic URL
routing for the app:

    polymer serve

### Build

The `polymer build` command builds your Polymer application for production, using build configuration options provided by the command line or in your project's `polymer.json` file.  

You can configure your `polymer.json` file to create multiple builds. This is necessary if you will be serving different builds optimized for different browsers. You can define your own named builds, or use presets. See the documentation on [building your project for production](https://www.polymer-project.org/2.0/toolbox/build-for-production) for more information.

Katamino Polymer is configured to create three builds using [the three supported presets](https://www.polymer-project.org/2.0/toolbox/build-for-production#build-presets):

```
"builds": [
  {
    "preset": "es5-bundled"
  },
  {
    "preset": "es6-bundled"
  },
  {
    "preset": "es6-unbundled"
  }
]
```

Builds will be output to a subdirectory under the `build/` directory as follows:

```
build/
  es5-bundled/
  es6-bundled/
  es6-unbundled/
```

* `es5-bundled` is a bundled, minified build with a service worker. ES6 code is compiled to ES5 for compatibility with older browsers.
* `es6-bundled` is a bundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that can handle ES6 code - see [building your project for production](https://www.polymer-project.org/2.0/toolbox/build-for-production#compiling) for a list.
* `es6-unbundled` is an unbundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that support HTTP/2 push.

Run `polymer help build` for the full list of available options and optimizations. Also, see the documentation on the [polymer.json specification](https://www.polymer-project.org/2.0/docs/tools/polymer-json) and [building your Polymer application for production](https://www.polymer-project.org/2.0/toolbox/build-for-production).

### Preview the build

This command serves your app. Replace `build-folder-name` with the folder name of the build you want to serve.

    polymer serve build/build-folder-name/

### Run tests

This command will run [Web Component Tester](https://github.com/Polymer/web-component-tester)
against the browsers currently installed on your machine:

    polymer test

If running Windows you will need to set the following environment variables:

- LAUNCHPAD_BROWSERS
- LAUNCHPAD_CHROME

Read More here [daffl/launchpad](https://github.com/daffl/launchpad#environment-variables-impacting-local-browsers-detection)
