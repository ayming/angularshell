# AngularShell

AngularShell is a AngularJS [FireShell](https://github.com/toddmotto/fireshell) build.

## Jump start

Get started with AngularShell:

1. Read the [installation guide](https://github.com/toddmotto/fireshell/blob/master/docs/DOCS.md#project-setup-and-grunt-installation)
2. Clone the git repo — `git clone https://github.com/ayming/angularshell.git`

## Documentation

 * FireShell - https://github.com/toddmotto/fireshell/blob/master/docs/DOCS.md
 * Grunt - http://gruntjs.com/getting-started
 * HTML5 Boilerplate - https://github.com/h5bp/html5-boilerplate/blob/v4.3.0/doc/TOC.md
 * JSHint - https://github.com/gruntjs/grunt-contrib-jshint
 * Uglify - https://github.com/gruntjs/grunt-contrib-uglify
 * Liveload - https://github.com/gruntjs/grunt-contrib-connect
 * Concat - https://github.com/gruntjs/grunt-contrib-concat
 * ngmin - https://github.com/btford/grunt-ngmin
 * Sass - https://github.com/gruntjs/grunt-contrib-sass
 * grunt-open - https://github.com/jsoverson/grunt-open

## Scaffolding

````
├── app
│   ├── assets
│   │   ├── css
│   │   ├── fonts
│   │   ├── img
│   │   ├── js
│   │   └── partials
│   ├── vendor
│   ├── favicon.ico
│   └── index.html
├── src
│   ├── js
│   │   ├── controllers
│   │   ├── directives
│   │   ├── filters
│   │   ├── services
│   │   └── app.js
│   └── scss
│       ├── mixins
│       ├── modules
│       ├── partials
│       ├── vendor
│       └── style.scss
├── grunt-build.command
├── grunt-build.bat
├── grunt-dev.command
├── grunt-dev.bat
├── package.json
├── README.md
├── .editorconfig
├── .gitignore
├── .jshintrc
└── .travis.yml
````

## About ngmin

[ngmin](https://github.com/btford/ngmin) is an AngularJS application pre-minifier but it does not currently attempt to be fully generalized, and might not work. There are some points you must be careful.

#### Something should be work

```javascript
someModule.controller('myCtrl', function ($scope) {});
someModule.service('myService', function ($scope) {});
someModule.factory('myFactory', function (a) {});
```

#### Something is temporarily not working

```javascript
// incorrect
someModule.config(function (a) {});
// correct
someModule.config(['a', function (a) {}]);

// incorrect
someModule.run(function (a) {});
// correct
someModule.run(['a', function (a) {}]);

// incorrect
function SomeCtrl($scope) {}
// correct
function SomeCtrl($scope) {}
SomeCtrl.$inject = ['$scope'];
```

To know more about angular minification, please take a look at the [document](http://docs.angularjs.org/tutorial/step_05).

## License

#### The MIT License (MIT)

Copyright (c) AngularShell

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Release History

 * 2013-10-17   v0.0.1   Work in progress.