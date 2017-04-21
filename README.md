# npmdoc-mitt

#### api documentation for  [mitt (v1.1.2)](https://github.com/developit/mitt)  [![npm package](https://img.shields.io/npm/v/npmdoc-mitt.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mitt) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mitt.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mitt)

#### Tiny 200b functional Event Emitter / pubsub.

[![NPM](https://nodei.co/npm/mitt.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/mitt)

- [https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mitt/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mitt/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mitt/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mitt/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "mitt",
    "version": "1.1.2",
    "description": "Tiny 200b functional Event Emitter / pubsub.",
    "jsnext:main": "dist/mitt.es.js",
    "module": "dist/mitt.es.js",
    "main": "dist/mitt.js",
    "umd:main": "dist/mitt.umd.js",
    "scripts": {
        "bump": "standard-version",
        "testonly": "mocha --compilers js:babel-register test/**/*.js",
        "lint": "eslint src test",
        "test": "flow && npm run lint && npm run testonly",
        "build": "npm-run-all --silent clean -p rollup -p minify:* -s docs size",
        "clean": "rimraf dist",
        "rollup": "rollup -c",
        "minify:cjs": "uglifyjs $npm_package_main -cm toplevel -o $npm_package_main -p relative --in-source-map ${npm_package_main}.map --source-map ${npm_package_main}.map",
        "minify:umd": "uglifyjs $npm_package_umd_main -cm -o $npm_package_umd_main -p relative --in-source-map ${npm_package_umd_main}.map --source-map ${npm_package_umd_main}.map",
        "docs": "documentation readme src/index.js --section API -q",
        "size": "echo \"Gzipped Size: $(strip-json-comments --no-whitespace $npm_package_main | gzip-size | pretty-bytes)\"",
        "release": "npm run build -s && npm run bump && git push --follow-tags origin master && npm publish"
    },
    "repository": "developit/mitt",
    "keywords": [
        "events",
        "eventemitter",
        "pubsub"
    ],
    "homepage": "https://github.com/developit/mitt",
    "authors": [
        "Jason Miller <jason@developit.ca>"
    ],
    "license": "MIT",
    "files": [
        "src",
        "dist",
        "mitt.d.ts"
    ],
    "eslintConfig": {
        "parser": "babel-eslint",
        "extends": "eslint:recommended",
        "env": {
            "browser": true,
            "mocha": true,
            "es6": true
        },
        "globals": {
            "expect": true
        },
        "rules": {
            "semi": [
                2,
                "always"
            ]
        }
    },
    "typings": "./mitt.d.ts",
    "devDependencies": {
        "babel-core": "^6.9.1",
        "babel-eslint": "^7.1.1",
        "babel-plugin-transform-flow-strip-types": "^6.21.0",
        "babel-preset-es2015": "^6.9.0",
        "babel-preset-stage-0": "^6.5.0",
        "babel-register": "^6.9.0",
        "chai": "^3.5.0",
        "documentation": "^4.0.0-beta4",
        "eslint": "^3.13.1",
        "flow-bin": "^0.38.0",
        "gzip-size-cli": "^1.0.0",
        "mocha": "^3.2.0",
        "npm-run-all": "^2.1.1",
        "pretty-bytes-cli": "^2.0.0",
        "rimraf": "^2.5.2",
        "rollup": "^0.41.4",
        "rollup-plugin-buble": "^0.15.0",
        "rollup-plugin-flow": "^1.1.1",
        "sinon": "^1.17.4",
        "sinon-chai": "^2.8.0",
        "standard-version": "^4.0.0",
        "strip-json-comments-cli": "^1.0.1",
        "uglify-js": "^2.6.2"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
