# npmdoc-grpc

#### api documentation for  [grpc (v1.2.4)](http://www.grpc.io/)  [![npm package](https://img.shields.io/npm/v/npmdoc-grpc.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-grpc) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grpc.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grpc)

#### gRPC Library for Node

[![NPM](https://nodei.co/npm/grpc.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/grpc)

- [https://npmdoc.github.io/node-npmdoc-grpc/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-grpc/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grpc/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grpc/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-grpc/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-grpc/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Google Inc."
    },
    "binary": {
        "module_name": "grpc_node",
        "module_path": "src/node/extension_binary",
        "host": "https://storage.googleapis.com/",
        "remote_path": "grpc-precompiled-binaries/node/{name}/v{version}",
        "package_name": "{node_abi}-{platform}-{arch}.tar.gz"
    },
    "bugs": {
        "url": "https://github.com/grpc/grpc/issues"
    },
    "bundleDependencies": [
        "node-pre-gyp"
    ],
    "contributors": [
        {
            "name": "Michael Lumish"
        }
    ],
    "dependencies": {
        "arguejs": "^0.2.3",
        "lodash": "^4.15.0",
        "nan": "^2.0.0",
        "node-pre-gyp": "^0.6.0",
        "protobufjs": "^5.0.0"
    },
    "description": "gRPC Library for Node",
    "devDependencies": {
        "async": "^2.0.1",
        "body-parser": "^1.15.2",
        "electron-mocha": "^3.1.1",
        "express": "^4.14.0",
        "google-auth-library": "^0.9.2",
        "google-protobuf": "^3.0.0",
        "istanbul": "^0.4.4",
        "jsdoc": "^3.3.2",
        "jshint": "^2.5.0",
        "minimist": "^1.1.0",
        "mocha": "^3.0.2",
        "mocha-jenkins-reporter": "^0.2.3",
        "poisson-process": "^0.2.1"
    },
    "directories": {
        "lib": "src/node/src"
    },
    "dist": {
        "shasum": "ef0c8c708245d8fc797e39aa330dce409b3dd03c",
        "tarball": "https://registry.npmjs.org/grpc/-/grpc-1.2.4.tgz"
    },
    "engines": {
        "node": ">=4"
    },
    "files": [
        "LICENSE",
        "src/node/README.md",
        "src/proto",
        "etc",
        "src/node/index.js",
        "src/node/src",
        "src/node/ext",
        "include/grpc",
        "src/core",
        "src/boringssl",
        "src/zlib",
        "third_party/nanopb",
        "third_party/zlib",
        "third_party/boringssl",
        "binding.gyp"
    ],
    "homepage": "http://www.grpc.io/",
    "jshintConfig": {
        "bitwise": true,
        "curly": true,
        "eqeqeq": true,
        "esnext": true,
        "freeze": true,
        "immed": true,
        "indent": 2,
        "latedef": "nofunc",
        "maxlen": 80,
        "mocha": true,
        "newcap": true,
        "node": true,
        "noarg": true,
        "quotmark": "single",
        "strict": true,
        "trailing": true,
        "undef": true,
        "unused": "vars"
    },
    "license": "BSD-3-Clause",
    "main": "src/node/index.js",
    "maintainers": [
        {
            "name": "grpc-packages"
        },
        {
            "name": "murgatroid99"
        }
    ],
    "name": "grpc",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/grpc/grpc.git"
    },
    "scripts": {
        "coverage": "istanbul cover ./node_modules/.bin/_mocha src/node/test",
        "electron-build": "node-pre-gyp configure build --runtime=electron --disturl=https://atom.io/download/atom-shell",
        "gen_docs": "jsdoc -c src/node/jsdoc_conf.json",
        "install": "node-pre-gyp install --fallback-to-build",
        "lint": "node ./node_modules/jshint/bin/jshint src/node/src src/node/test src/node/interop src/node/index.js --exclude-path=src/node/.jshintignore",
        "test": "mocha src/node/test && npm run-script lint"
    },
    "version": "1.2.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
