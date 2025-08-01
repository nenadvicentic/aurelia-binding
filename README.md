# aurelia-binding

[![npm Version](https://img.shields.io/npm/v/aurelia-binding.svg)](https://www.npmjs.com/package/aurelia-binding)
[![ZenHub](https://raw.githubusercontent.com/ZenHubIO/support/master/zenhub-badge.png)](https://zenhub.io)
[![Join the chat at https://gitter.im/aurelia/discuss](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/aurelia/discuss?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![CircleCI](https://circleci.com/gh/aurelia/binding.svg?style=shield)](https://circleci.com/gh/aurelia/binding)

This library is part of the [Aurelia](http://www.aurelia.io/) platform and implements a modern databinding library for JavaScript and HTML.

> To keep up to date on [Aurelia](http://www.aurelia.io/), please visit and subscribe to [the official blog](http://blog.aurelia.io/) and [our email list](http://eepurl.com/ces50j). We also invite you to [follow us on twitter](https://twitter.com/aureliaeffect). If you have questions look around our [Discourse forums](https://discourse.aurelia.io/), chat in our [community on Gitter](https://gitter.im/aurelia/discuss) or use [stack overflow](http://stackoverflow.com/search?q=aurelia). Documentation can be found [in our developer hub](http://aurelia.io/docs). If you would like to have deeper insight into our development process, please install the [ZenHub](https://zenhub.io) Chrome or Firefox Extension and visit any of our repository's boards.

## Platform Support

This library can be used in the **browser** only.

## Building The Code

To build the code, follow these steps.

1. Ensure that [NodeJS](http://nodejs.org/) is installed. This provides the platform on which the build tooling runs.
2. From the project folder, execute the following command:

    ```shell
    npm install
    ```
3. Execute build command:
    ```shell
    npm run build
    ```
    `npm run build` uses `gulp build` command under the hood.

4. You will find the compiled code in the `dist` folder, available in three module formats: AMD, CommonJS and ES6.

5. See `gulpfile.js` for other tasks related to generating the docs and linting. The tasks are located in `/build` folder.

## Running The Tests

To run the unit tests, first ensure that you have followed the steps above in order to install all dependencies and successfully build the library. Once you have done that, proceed with these additional steps:

1. From the project folder, execute the following command:

    ```shell
    npm install
    ```

4. You can now run the tests with this command:

    ```shell
    npm run test
    ```

    `npm run test` command uses `karma start --single-run` command under the hood.
  
  To test in Internet Explorer use this command:
  ```shell
  karma start --browsers IE
  ```

  ### How tests are configured

[Karma](http://karma-runner.github.io/) runner (version 1) is used to run tests in browser, while [Webpack](https://v4.webpack.js.org/) (version 4) is used as the loader for `src` and `test` files.

#### Older version of NPM packages
The reason to use version 4 of Webpack, version 7 of [babel-loader](https://webpack.js.org/loaders/babel-loader/) and version 6 [Babel](https://babeljs.io/) is that [babel-preset-es2015](https://babeljs.io/docs/babel-preset-es2015) and it's bundled plugins `babel-plugin-transform-es2015-*` have been depracted in favour of new [babel-preset-env](https://babeljs.io/docs/babel-preset-env).

Differences are decribed in the article [babel-preset-es2015 -> babel-preset-env](https://babeljs.io/docs/env/).
