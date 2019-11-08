# Parcel-dynamic-import
Repo showing problem with [Parcel bundler](https://parceljs.org/) and [dynamic imports](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import).

Parcel-bundler 1.12.4
Typescript 3.7.2
Chrome 77.0.3865.120
Ubuntu 18.04.3 LTS

## Setup
Install project dependencies and start the Parcel development server.
```sh
npm install
npm run start
```

## Problem 1 
Point browser to http://localhost:1234/index.html and open the javascript console.

#### Expected
```
hello bars!
hello world!
hello foos!
```
#### Actual
```
hello bars!
hello world!
```

## Problem 2
Point browser to http://localhost:1234/index2.html and open the javascript console.

Expected:
```
hello bars!
hello world!
hello foos!
```
Actual:
```
hello bars!
hello world!
> Uncaught ReferenceError: parcelRequire is not defined
    at bundle-loader.js:80
    at bundle-loader.js:80
```

