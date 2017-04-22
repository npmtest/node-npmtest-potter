# npmtest-potter

#### basic test coverage for  [potter (v4.0.3)](https://github.com/uber/potter)  [![npm package](https://img.shields.io/npm/v/npmtest-potter.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-potter) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-potter.svg)](https://travis-ci.org/npmtest/node-npmtest-potter)

#### A command line for developer workflows, and generating applications and services

[![NPM](https://nodei.co/npm/potter.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/potter)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-potter/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-potter/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-potter/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-potter/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-potter/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-potter/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-potter/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-potter/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-potter/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-potter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-potter/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-potter/build/test-report.html](https://npmtest.github.io/node-npmtest-potter/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-potter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-potter/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-potter/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-potter/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-potter/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-potter/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-potter/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-potter/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "potter",
    "version": "4.0.3",
    "description": "A command line for developer workflows, and generating applications and services",
    "keywords": [
        "web",
        "framework",
        "scaffold",
        "guide",
        "production"
    ],
    "author": "Jake Verbaten <jakev@uber.com>",
    "repository": "git://github.com/uber/potter.git",
    "main": "index",
    "homepage": "https://github.com/uber/potter",
    "bugs": {
        "url": "https://github.com/uber/potter/issues"
    },
    "contributors": [
        "Tom Croucher <tomc@uber.com>"
    ],
    "bin": {
        "potter": "./cli/cli.js",
        "playdoh": "./cli/cli-deprecated.js"
    },
    "dependencies": {
        "array-find": "^0.1.1",
        "chalk": "^0.5.1",
        "debuglog": "^1.0.1",
        "error": "^3.0.0",
        "minimist": "^1.1.0",
        "mkdirp": "^0.5.0",
        "msee": "^0.1.1",
        "parents": "^1.0.0",
        "process": "^0.7.0",
        "read-json": "0.0.0",
        "rimraf": "^2.2.8",
        "run-parallel": "^1.0.0",
        "run-series": "^1.0.2",
        "safe-json-parse": "^2.0.0",
        "semver": "^3.0.1",
        "stackup": "0.0.5",
        "wizzard": "1.0.0",
        "xtend": "^4.0.0",
        "uuid": "^1.4.1",
        "url": "^0.10.1"
    },
    "licenses": [
        {
            "type": "MIT",
            "url": "http://github.com/uber/potter/raw/master/LICENSE"
        }
    ],
    "devDependencies": {
        "fixtures-fs": "^1.0.2",
        "istanbul": "~0.1.46",
        "jshint": "^2.5.1",
        "opn": "^0.1.2",
        "pre-commit": "0.0.8",
        "request": "^2.36.0",
        "tap-spec": "^0.1.9",
        "tape": "^2.12.3"
    },
    "scripts": {
        "test": "npm run check-package -s && npm run jshint -s && node test/index.js | tap-spec",
        "fast-test": "npm run check-package -s && npm run jshint -s && node test/unit.js | tap-spec",
        "check-package": "npm ls 1>/dev/null --loglevel=warn",
        "jshint-pre-commit": "jshint --verbose $(git diff --cached --name-only --diff-filter=ACMRTUXB | grep '\\.js$')",
        "jscs-pre-commit": "jscs $(git diff --cached --name-only | grep '\\.js$')",
        "jshint": "jshint --verbose .",
        "fast-cover": "istanbul cover --report none --print detail test/unit.js",
        "cover": "istanbul cover --report none --print detail test/index.js",
        "view-cover": "istanbul report html && opn ./coverage/index.html"
    },
    "pre-commit": [
        "jshint-pre-commit",
        "fast-test"
    ],
    "engine": {
        "node": ">= 0.10.x"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
