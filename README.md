# npmdoc-redux-saga

#### api documentation for  [redux-saga (v0.14.7)](https://github.com/redux-saga/redux-saga#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-redux-saga.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-redux-saga) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-redux-saga.svg)](https://travis-ci.org/npmdoc/node-npmdoc-redux-saga)

#### Saga middleware for Redux to handle Side Effects

[![NPM](https://nodei.co/npm/redux-saga.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-saga)

- [https://npmdoc.github.io/node-npmdoc-redux-saga/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-saga/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-saga/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-saga/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-redux-saga/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-redux-saga/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "redux-saga",
    "version": "0.14.7",
    "description": "Saga middleware for Redux to handle Side Effects",
    "main": "lib/index.js",
    "module": "es/index.js",
    "jsnext:main": "es/index.js",
    "scripts": {
        "lint": "eslint src",
        "test": "cross-env BABEL_ENV=cjs babel-node test/index.js | tap-spec",
        "check": "npm run lint && npm run test",
        "compile": "rimraf lib && cross-env BABEL_ENV=cjs babel -d lib/ src/",
        "build:umd:dev": "cross-env BABEL_ENV=cjs webpack src/index.js dist/redux-saga.js --config webpack.config.dev.js",
        "build:umd:prod": "cross-env BABEL_ENV=cjs webpack src/index.js dist/redux-saga.min.js --config webpack.config.prod.js",
        "build:es": "cross-env BABEL_ENV=es babel src --out-dir es",
        "build": "rimraf dist es && npm run build:umd:dev && npm run build:umd:prod && npm run build:es",
        "prepublish": "npm run check && npm run compile && npm run build",
        "counter": "cross-env BABEL_ENV=cjs node examples/counter/server.js",
        "cancellable-counter": "cross-env BABEL_ENV=cjs node examples/cancellable-counter/server.js",
        "test-counter": "cross-env BABEL_ENV=cjs babel-node examples/counter/test/sagas.js | tap-spec",
        "shop": "cross-env BABEL_ENV=cjs node examples/shopping-cart/server.js",
        "test-shop": "cross-env BABEL_ENV=cjs babel-node examples/shopping-cart/test/sagas.js | tap-spec",
        "async": "cross-env BABEL_ENV=cjs node examples/async/server.js",
        "test-async": "cross-env BABEL_ENV=cjs babel-node examples/async/test/sagas.js | tap-spec",
        "real-world": "npm --prefix examples/real-world install examples/real-world && cross-env BABEL_ENV=cjs node --require babel-register examples/real-world/server.js",
        "docs:clean": "rimraf _book",
        "docs:prepare": "gitbook install",
        "docs:build": "npm run docs:prepare && gitbook build -g redux-saga/redux-saga",
        "docs:watch": "npm run docs:prepare && gitbook serve",
        "docs:publish": "npm run docs:clean && npm run docs:build && cd _book && git init && git commit --allow-empty -m 'update book' && git checkout -b gh-pages && touch .nojekyll && git add . && git commit -am 'update book' && git push git@github.com:redux-saga/redux-saga gh-pages --force"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/redux-saga/redux-saga.git"
    },
    "keywords": [
        "javascript",
        "redux",
        "middleware",
        "saga",
        "effects",
        "side effects"
    ],
    "author": "Yassine ELOUAFI <yelouafi@gmail.com>",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/redux-saga/redux-saga/issues"
    },
    "homepage": "https://github.com/redux-saga/redux-saga#readme",
    "dependencies": {},
    "devDependencies": {
        "babel-cli": "^6.1.18",
        "babel-core": "^6.14.0",
        "babel-eslint": "^6.0.3",
        "babel-loader": "^6.2.5",
        "babel-polyfill": "^6.7.4",
        "babel-preset-es2015": "^6.14.0",
        "babel-preset-react": "^6.11.1",
        "babel-preset-stage-2": "^6.13.0",
        "cross-env": "^1.0.8",
        "eslint": "^2.8.0",
        "express": "^4.13.3",
        "gitbook-cli": "1.0.1",
        "isomorphic-fetch": "^2.2.0",
        "lolex": "^1.5.2",
        "react": "^15.0.0",
        "react-dom": "^15.0.0",
        "react-redux": "^4.4.5",
        "redux": "^3.5.1",
        "redux-logger": "^2.6.1",
        "rimraf": "^2.4.3",
        "tap-spec": "^4.1.1",
        "tape": "^4.2.2",
        "typescript": "^1.8.10",
        "typescript-definition-tester": "0.0.4",
        "webpack": "1.13.0",
        "webpack-dev-middleware": "^1.4.0",
        "webpack-hot-middleware": "^2.6.0"
    },
    "typings": "./index.d.ts",
    "npmName": "redux-saga",
    "npmFileMap": [
        {
            "basePath": "/dist/",
            "files": [
                "*.js"
            ]
        }
    ]
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
