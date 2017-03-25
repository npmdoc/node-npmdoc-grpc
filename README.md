# api documentation for  [grpc (v1.2.0)](http://www.grpc.io/)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grpc.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grpc)
#### gRPC Library for Node

[![NPM](https://nodei.co/npm/grpc.png?downloads=true)](https://www.npmjs.com/package/grpc)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grpc/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-grpc_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grpc/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-grpc/build/screen-capture.npmPackageListing.svg)



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
            "name": "Michael Lumish",
            "email": "mlumish@google.com"
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
        "shasum": "9b99516a885475fdd25f28766cab8e6460153f52",
        "tarball": "https://registry.npmjs.org/grpc/-/grpc-1.2.0.tgz"
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
            "name": "murgatroid99",
            "email": "mlumish@google.com"
        },
        {
            "name": "tbetbetbe",
            "email": "temiola@google.com"
        },
        {
            "name": "grpc-packages",
            "email": "grpc-packages@google.com"
        }
    ],
    "name": "grpc",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "1.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module grpc](#apidoc.module.grpc)
1.  [function <span class="apidocSignatureSpan">grpc.</span>Metadata ()](#apidoc.element.grpc.Metadata)
1.  [function <span class="apidocSignatureSpan">grpc.</span>Server (options)](#apidoc.element.grpc.Server)
1.  [function <span class="apidocSignatureSpan">grpc.</span>ServerCredentials ()](#apidoc.element.grpc.ServerCredentials)
1.  [function <span class="apidocSignatureSpan">grpc.</span>closeClient (client_obj)](#apidoc.element.grpc.closeClient)
1.  [function <span class="apidocSignatureSpan">grpc.</span>getClientChannel (client)](#apidoc.element.grpc.getClientChannel)
1.  [function <span class="apidocSignatureSpan">grpc.</span>load (filename, format, options)](#apidoc.element.grpc.load)
1.  [function <span class="apidocSignatureSpan">grpc.</span>loadObject (value, options)](#apidoc.element.grpc.loadObject)
1.  [function <span class="apidocSignatureSpan">grpc.</span>makeGenericClientConstructor (methods, serviceName, class_options)](#apidoc.element.grpc.makeGenericClientConstructor)
1.  [function <span class="apidocSignatureSpan">grpc.</span>setLogVerbosity (verbosity)](#apidoc.element.grpc.setLogVerbosity)
1.  [function <span class="apidocSignatureSpan">grpc.</span>setLogger (logger)](#apidoc.element.grpc.setLogger)
1.  [function <span class="apidocSignatureSpan">grpc.</span>waitForClientReady (client, deadline, callback)](#apidoc.element.grpc.waitForClientReady)
1.  object <span class="apidocSignatureSpan">grpc.</span>Metadata.prototype
1.  object <span class="apidocSignatureSpan">grpc.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">grpc.</span>callError
1.  object <span class="apidocSignatureSpan">grpc.</span>credentials
1.  object <span class="apidocSignatureSpan">grpc.</span>logVerbosity
1.  object <span class="apidocSignatureSpan">grpc.</span>propagate
1.  object <span class="apidocSignatureSpan">grpc.</span>status
1.  object <span class="apidocSignatureSpan">grpc.</span>writeFlags

#### [module grpc.Metadata](#apidoc.module.grpc.Metadata)
1.  [function <span class="apidocSignatureSpan">grpc.</span>Metadata ()](#apidoc.element.grpc.Metadata.Metadata)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.</span>_fromCoreRepresentation (metadata)](#apidoc.element.grpc.Metadata._fromCoreRepresentation)

#### [module grpc.Metadata.prototype](#apidoc.module.grpc.Metadata.prototype)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>_getCoreRepresentation ()](#apidoc.element.grpc.Metadata.prototype._getCoreRepresentation)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>add (key, value)](#apidoc.element.grpc.Metadata.prototype.add)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>clone ()](#apidoc.element.grpc.Metadata.prototype.clone)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>get (key)](#apidoc.element.grpc.Metadata.prototype.get)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>getMap ()](#apidoc.element.grpc.Metadata.prototype.getMap)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>remove (key)](#apidoc.element.grpc.Metadata.prototype.remove)
1.  [function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>set (key, value)](#apidoc.element.grpc.Metadata.prototype.set)

#### [module grpc.Server](#apidoc.module.grpc.Server)
1.  [function <span class="apidocSignatureSpan">grpc.</span>Server (options)](#apidoc.element.grpc.Server.Server)

#### [module grpc.Server.prototype](#apidoc.module.grpc.Server.prototype)
1.  [function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>addProtoService (service, implementation)](#apidoc.element.grpc.Server.prototype.addProtoService)
1.  [function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>addService (service, implementation)](#apidoc.element.grpc.Server.prototype.addService)
1.  [function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>bind (port, creds)](#apidoc.element.grpc.Server.prototype.bind)
1.  [function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>register (name, handler, serialize, deserialize, type)](#apidoc.element.grpc.Server.prototype.register)

#### [module grpc.ServerCredentials](#apidoc.module.grpc.ServerCredentials)
1.  [function <span class="apidocSignatureSpan">grpc.</span>ServerCredentials ()](#apidoc.element.grpc.ServerCredentials.ServerCredentials)
1.  [function <span class="apidocSignatureSpan">grpc.ServerCredentials.</span>createInsecure ()](#apidoc.element.grpc.ServerCredentials.createInsecure)
1.  [function <span class="apidocSignatureSpan">grpc.ServerCredentials.</span>createSsl ()](#apidoc.element.grpc.ServerCredentials.createSsl)

#### [module grpc.credentials](#apidoc.module.grpc.credentials)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>combineCallCredentials ()](#apidoc.element.grpc.credentials.combineCallCredentials)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>combineChannelCredentials (channel_credential)](#apidoc.element.grpc.credentials.combineChannelCredentials)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>createFromGoogleCredential (google_credential)](#apidoc.element.grpc.credentials.createFromGoogleCredential)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>createFromMetadataGenerator (metadata_generator)](#apidoc.element.grpc.credentials.createFromMetadataGenerator)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>createInsecure ()](#apidoc.element.grpc.credentials.createInsecure)
1.  [function <span class="apidocSignatureSpan">grpc.credentials.</span>createSsl ()](#apidoc.element.grpc.credentials.createSsl)



# <a name="apidoc.module.grpc"></a>[module grpc](#apidoc.module.grpc)

#### <a name="apidoc.element.grpc.Metadata"></a>[function <span class="apidocSignatureSpan">grpc.</span>Metadata ()](#apidoc.element.grpc.Metadata)
- description and source-code
```javascript
function Metadata() {
  this._internal_repr = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Server"></a>[function <span class="apidocSignatureSpan">grpc.</span>Server (options)](#apidoc.element.grpc.Server)
- description and source-code
```javascript
function Server(options) {
  this.handlers = {};
  var handlers = this.handlers;
  var server = new grpc.Server(options);
  this._server = server;
  this.started = false;
<span class="apidocCodeCommentSpan">  /**
   * Start the server and begin handling requests
   * @this Server
   */
</span>  this.start = function() {
    if (this.started) {
      throw new Error('Server is already running');
    }
    this.started = true;
    server.start();
    /**
     * Handles the SERVER_RPC_NEW event. If there is a handler associated with
     * the requested method, use that handler to respond to the request. Then
     * wait for the next request
     * @param {grpc.Event} event The event to handle with tag SERVER_RPC_NEW
     */
    function handleNewCall(err, event) {
      if (err) {
        return;
      }
      var details = event.new_call;
      var call = details.call;
      var method = details.method;
      var metadata = Metadata._fromCoreRepresentation(details.metadata);
      if (method === null) {
        return;
      }
      server.requestCall(handleNewCall);
      var handler;
      if (handlers.hasOwnProperty(method)) {
        handler = handlers[method];
      } else {
        var batch = {};
        batch[grpc.opType.SEND_INITIAL_METADATA] =
            (new Metadata())._getCoreRepresentation();
        batch[grpc.opType.SEND_STATUS_FROM_SERVER] = {
          code: grpc.status.UNIMPLEMENTED,
          details: '',
          metadata: {}
        };
        batch[grpc.opType.RECV_CLOSE_ON_SERVER] = true;
        call.startBatch(batch, function() {});
        return;
      }
      streamHandlers[handler.type](call, handler, metadata);
    }
    server.requestCall(handleNewCall);
  };

  /**
   * Gracefully shuts down the server. The server will stop receiving new calls,
   * and any pending calls will complete. The callback will be called when all
   * pending calls have completed and the server is fully shut down. This method
   * is idempotent with itself and forceShutdown.
   * @param {function()} callback The shutdown complete callback
   */
  this.tryShutdown = function(callback) {
    server.tryShutdown(callback);
  };

  /**
   * Forcibly shuts down the server. The server will stop receiving new calls
   * and cancel all pending calls. When it returns, the server has shut down.
   * This method is idempotent with itself and tryShutdown, and it will trigger
   * any outstanding tryShutdown callbacks.
   */
  this.forceShutdown = function() {
    server.forceShutdown();
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.ServerCredentials"></a>[function <span class="apidocSignatureSpan">grpc.</span>ServerCredentials ()](#apidoc.element.grpc.ServerCredentials)
- description and source-code
```javascript
function ServerCredentials() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.closeClient"></a>[function <span class="apidocSignatureSpan">grpc.</span>closeClient (client_obj)](#apidoc.element.grpc.closeClient)
- description and source-code
```javascript
function closeClient(client_obj) {
  client.getClientChannel(client_obj).close();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.getClientChannel"></a>[function <span class="apidocSignatureSpan">grpc.</span>getClientChannel (client)](#apidoc.element.grpc.getClientChannel)
- description and source-code
```javascript
getClientChannel = function (client) {
  return client.$channel;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.load"></a>[function <span class="apidocSignatureSpan">grpc.</span>load (filename, format, options)](#apidoc.element.grpc.load)
- description and source-code
```javascript
function load(filename, format, options) {
  if (!format) {
    format = 'proto';
  }
  var convertFieldsToCamelCaseOriginal = ProtoBuf.convertFieldsToCamelCase;
  if(options && options.hasOwnProperty('convertFieldsToCamelCase')) {
    ProtoBuf.convertFieldsToCamelCase = options.convertFieldsToCamelCase;
  }
  var builder;
  try {
    switch(format) {
      case 'proto':
      builder = ProtoBuf.loadProtoFile(filename);
      break;
      case 'json':
      builder = ProtoBuf.loadJsonFile(filename);
      break;
      default:
      throw new Error('Unrecognized format "' + format + '"');
    }
  } finally {
    ProtoBuf.convertFieldsToCamelCase = convertFieldsToCamelCaseOriginal;
  }
  return loadObject(builder.ns, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.loadObject"></a>[function <span class="apidocSignatureSpan">grpc.</span>loadObject (value, options)](#apidoc.element.grpc.loadObject)
- description and source-code
```javascript
function loadObject(value, options) {
  var result = {};
  if (value.className === 'Namespace') {
    _.each(value.children, function(child) {
      result[child.name] = loadObject(child, options);
    });
    return result;
  } else if (value.className === 'Service') {
    return client.makeProtobufClientConstructor(value, options);
  } else if (value.className === 'Message' || value.className === 'Enum') {
    return value.build();
  } else {
    return value;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.makeGenericClientConstructor"></a>[function <span class="apidocSignatureSpan">grpc.</span>makeGenericClientConstructor (methods, serviceName, class_options)](#apidoc.element.grpc.makeGenericClientConstructor)
- description and source-code
```javascript
makeGenericClientConstructor = function (methods, serviceName, class_options) {
  if (!class_options) {
    class_options = {};
  }
<span class="apidocCodeCommentSpan">  /**
   * Create a client with the given methods
   * @constructor
   * @param {string} address The address of the server to connect to
   * @param {grpc.Credentials} credentials Credentials to use to connect
   *     to the server
   * @param {Object} options Options to pass to the underlying channel
   */
</span>  function Client(address, credentials, options) {
    if (!options) {
      options = {};
    }
    /* Append the grpc-node user agent string after the application user agent
     * string, and put the combination at the beginning of the user agent string
     */
    if (options['grpc.primary_user_agent']) {
      options['grpc.primary_user_agent'] += ' ';
    } else {
      options['grpc.primary_user_agent'] = '';
    }
    options['grpc.primary_user_agent'] += 'grpc-node/' + version;
    /* Private fields use $ as a prefix instead of _ because it is an invalid
     * prefix of a method name */
    this.$channel = new grpc.Channel(address, credentials, options);
  }

  _.each(methods, function(attrs, name) {
    var method_type;
    if (_.startsWith(name, '$')) {
      throw new Error('Method names cannot start with $');
    }
    if (attrs.requestStream) {
      if (attrs.responseStream) {
        method_type = 'bidi';
      } else {
        method_type = 'client_stream';
      }
    } else {
      if (attrs.responseStream) {
        method_type = 'server_stream';
      } else {
        method_type = 'unary';
      }
    }
    var serialize = attrs.requestSerialize;
    var deserialize = attrs.responseDeserialize;
    var method_func = requester_makers[method_type](
        attrs.path, serialize, deserialize);
    if (class_options.deprecatedArgumentOrder) {
      Client.prototype[name] = deprecated_request_wrap(method_func);
    } else {
      Client.prototype[name] = method_func;
    }
    // Associate all provided attributes with the method
    _.assign(Client.prototype[name], attrs);
  });

  return Client;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.setLogVerbosity"></a>[function <span class="apidocSignatureSpan">grpc.</span>setLogVerbosity (verbosity)](#apidoc.element.grpc.setLogVerbosity)
- description and source-code
```javascript
function setLogVerbosity(verbosity) {
  common.logVerbosity = verbosity;
  grpc.setLogVerbosity(verbosity);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.setLogger"></a>[function <span class="apidocSignatureSpan">grpc.</span>setLogger (logger)](#apidoc.element.grpc.setLogger)
- description and source-code
```javascript
function setLogger(logger) {
  common.logger = logger;
  grpc.setDefaultLoggerCallback(function(file, line, severity,
                                         message, timestamp) {
    logger.error(log_template({
      file: path.basename(file),
      line: line,
      severity: severity,
      message: message,
      timestamp: timestamp.toISOString()
    }));
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.waitForClientReady"></a>[function <span class="apidocSignatureSpan">grpc.</span>waitForClientReady (client, deadline, callback)](#apidoc.element.grpc.waitForClientReady)
- description and source-code
```javascript
waitForClientReady = function (client, deadline, callback) {
  var checkState = function(err) {
    if (err) {
      callback(new Error('Failed to connect before the deadline'));
      return;
    }
    var new_state = client.$channel.getConnectivityState(true);
    if (new_state === grpc.connectivityState.READY) {
      callback();
    } else if (new_state === grpc.connectivityState.FATAL_FAILURE) {
      callback(new Error('Failed to connect to server'));
    } else {
      client.$channel.watchConnectivityState(new_state, deadline, checkState);
    }
  };
  checkState();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.Metadata"></a>[module grpc.Metadata](#apidoc.module.grpc.Metadata)

#### <a name="apidoc.element.grpc.Metadata.Metadata"></a>[function <span class="apidocSignatureSpan">grpc.</span>Metadata ()](#apidoc.element.grpc.Metadata.Metadata)
- description and source-code
```javascript
function Metadata() {
  this._internal_repr = {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata._fromCoreRepresentation"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.</span>_fromCoreRepresentation (metadata)](#apidoc.element.grpc.Metadata._fromCoreRepresentation)
- description and source-code
```javascript
_fromCoreRepresentation = function (metadata) {
  var newMetadata = new Metadata();
  if (metadata) {
    _.forOwn(metadata, function(value, key) {
      newMetadata._internal_repr[key] = _.clone(value);
    });
  }
  return newMetadata;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.Metadata.prototype"></a>[module grpc.Metadata.prototype](#apidoc.module.grpc.Metadata.prototype)

#### <a name="apidoc.element.grpc.Metadata.prototype._getCoreRepresentation"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>_getCoreRepresentation ()](#apidoc.element.grpc.Metadata.prototype._getCoreRepresentation)
- description and source-code
```javascript
_getCoreRepresentation = function () {
  return this._internal_repr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.add"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>add (key, value)](#apidoc.element.grpc.Metadata.prototype.add)
- description and source-code
```javascript
add = function (key, value) {
  key = normalizeKey(key);
  validate(key, value);
  if (!this._internal_repr[key]) {
    this._internal_repr[key] = [];
  }
  this._internal_repr[key].push(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.clone"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>clone ()](#apidoc.element.grpc.Metadata.prototype.clone)
- description and source-code
```javascript
clone = function () {
  var copy = new Metadata();
  _.forOwn(this._internal_repr, function(value, key) {
    copy._internal_repr[key] = _.clone(value);
  });
  return copy;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.get"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>get (key)](#apidoc.element.grpc.Metadata.prototype.get)
- description and source-code
```javascript
get = function (key) {
  key = normalizeKey(key);
  if (Object.prototype.hasOwnProperty.call(this._internal_repr, key)) {
    return this._internal_repr[key];
  } else {
    return [];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.getMap"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>getMap ()](#apidoc.element.grpc.Metadata.prototype.getMap)
- description and source-code
```javascript
getMap = function () {
  var result = {};
  _.forOwn(this._internal_repr, function(values, key) {
    if(values.length > 0) {
      result[key] = values[0];
    }
  });
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.remove"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>remove (key)](#apidoc.element.grpc.Metadata.prototype.remove)
- description and source-code
```javascript
remove = function (key) {
  key = normalizeKey(key);
  if (Object.prototype.hasOwnProperty.call(this._internal_repr, key)) {
    delete this._internal_repr[key];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Metadata.prototype.set"></a>[function <span class="apidocSignatureSpan">grpc.Metadata.prototype.</span>set (key, value)](#apidoc.element.grpc.Metadata.prototype.set)
- description and source-code
```javascript
set = function (key, value) {
  key = normalizeKey(key);
  validate(key, value);
  this._internal_repr[key] = [value];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.Server"></a>[module grpc.Server](#apidoc.module.grpc.Server)

#### <a name="apidoc.element.grpc.Server.Server"></a>[function <span class="apidocSignatureSpan">grpc.</span>Server (options)](#apidoc.element.grpc.Server.Server)
- description and source-code
```javascript
function Server(options) {
  this.handlers = {};
  var handlers = this.handlers;
  var server = new grpc.Server(options);
  this._server = server;
  this.started = false;
<span class="apidocCodeCommentSpan">  /**
   * Start the server and begin handling requests
   * @this Server
   */
</span>  this.start = function() {
    if (this.started) {
      throw new Error('Server is already running');
    }
    this.started = true;
    server.start();
    /**
     * Handles the SERVER_RPC_NEW event. If there is a handler associated with
     * the requested method, use that handler to respond to the request. Then
     * wait for the next request
     * @param {grpc.Event} event The event to handle with tag SERVER_RPC_NEW
     */
    function handleNewCall(err, event) {
      if (err) {
        return;
      }
      var details = event.new_call;
      var call = details.call;
      var method = details.method;
      var metadata = Metadata._fromCoreRepresentation(details.metadata);
      if (method === null) {
        return;
      }
      server.requestCall(handleNewCall);
      var handler;
      if (handlers.hasOwnProperty(method)) {
        handler = handlers[method];
      } else {
        var batch = {};
        batch[grpc.opType.SEND_INITIAL_METADATA] =
            (new Metadata())._getCoreRepresentation();
        batch[grpc.opType.SEND_STATUS_FROM_SERVER] = {
          code: grpc.status.UNIMPLEMENTED,
          details: '',
          metadata: {}
        };
        batch[grpc.opType.RECV_CLOSE_ON_SERVER] = true;
        call.startBatch(batch, function() {});
        return;
      }
      streamHandlers[handler.type](call, handler, metadata);
    }
    server.requestCall(handleNewCall);
  };

  /**
   * Gracefully shuts down the server. The server will stop receiving new calls,
   * and any pending calls will complete. The callback will be called when all
   * pending calls have completed and the server is fully shut down. This method
   * is idempotent with itself and forceShutdown.
   * @param {function()} callback The shutdown complete callback
   */
  this.tryShutdown = function(callback) {
    server.tryShutdown(callback);
  };

  /**
   * Forcibly shuts down the server. The server will stop receiving new calls
   * and cancel all pending calls. When it returns, the server has shut down.
   * This method is idempotent with itself and tryShutdown, and it will trigger
   * any outstanding tryShutdown callbacks.
   */
  this.forceShutdown = function() {
    server.forceShutdown();
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.Server.prototype"></a>[module grpc.Server.prototype](#apidoc.module.grpc.Server.prototype)

#### <a name="apidoc.element.grpc.Server.prototype.addProtoService"></a>[function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>addProtoService (service, implementation)](#apidoc.element.grpc.Server.prototype.addProtoService)
- description and source-code
```javascript
addProtoService = function (service, implementation) {
  var options;
  if (service.grpc_options) {
    options = service.grpc_options;
  }
  this.addService(common.getProtobufServiceAttrs(service, options),
                  implementation);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Server.prototype.addService"></a>[function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>addService (service, implementation)](#apidoc.element.grpc.Server.prototype.addService)
- description and source-code
```javascript
addService = function (service, implementation) {
  if (!_.isObject(service) || !_.isObject(implementation)) {
    throw new Error('addService requires two objects as arguments');
  }
  if (_.keys(service).length === 0) {
    throw new Error('Cannot add an empty service to a server');
  }
  if (this.started) {
    throw new Error('Can\'t add a service to a started server.');
  }
  var self = this;
  _.forOwn(service, function(attrs, name) {
    var method_type;
    if (attrs.requestStream) {
      if (attrs.responseStream) {
        method_type = 'bidi';
      } else {
        method_type = 'client_stream';
      }
    } else {
      if (attrs.responseStream) {
        method_type = 'server_stream';
      } else {
        method_type = 'unary';
      }
    }
    var impl;
    if (implementation[name] === undefined) {
<span class="apidocCodeCommentSpan">      /* Handle the case where the method is passed with the name exactly as
         written in the proto file, instead of using JavaScript function
         naming style */
</span>      if (implementation[attrs.originalName] === undefined) {
        common.log(grpc.logVerbosity.ERROR, 'Method handler ' + name + ' for ' +
            attrs.path + ' expected but not provided');
        impl = defaultHandler[method_type];
      } else {
        impl = _.bind(implementation[attrs.originalName], implementation);
      }
    } else {
      impl = _.bind(implementation[name], implementation);
    }
    var serialize = attrs.responseSerialize;
    var deserialize = attrs.requestDeserialize;
    var register_success = self.register(attrs.path, impl, serialize,
                                         deserialize, method_type);
    if (!register_success) {
      throw new Error('Method handler for ' + attrs.path +
          ' already provided.');
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Server.prototype.bind"></a>[function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>bind (port, creds)](#apidoc.element.grpc.Server.prototype.bind)
- description and source-code
```javascript
bind = function (port, creds) {
  if (this.started) {
    throw new Error('Can\'t bind an already running server to an address');
  }
  return this._server.addHttp2Port(port, creds);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.Server.prototype.register"></a>[function <span class="apidocSignatureSpan">grpc.Server.prototype.</span>register (name, handler, serialize, deserialize, type)](#apidoc.element.grpc.Server.prototype.register)
- description and source-code
```javascript
register = function (name, handler, serialize, deserialize, type) {
  if (this.handlers.hasOwnProperty(name)) {
    return false;
  }
  this.handlers[name] = {
    func: handler,
    serialize: serialize,
    deserialize: deserialize,
    type: type
  };
  return true;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.ServerCredentials"></a>[module grpc.ServerCredentials](#apidoc.module.grpc.ServerCredentials)

#### <a name="apidoc.element.grpc.ServerCredentials.ServerCredentials"></a>[function <span class="apidocSignatureSpan">grpc.</span>ServerCredentials ()](#apidoc.element.grpc.ServerCredentials.ServerCredentials)
- description and source-code
```javascript
function ServerCredentials() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.ServerCredentials.createInsecure"></a>[function <span class="apidocSignatureSpan">grpc.ServerCredentials.</span>createInsecure ()](#apidoc.element.grpc.ServerCredentials.createInsecure)
- description and source-code
```javascript
createInsecure = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.ServerCredentials.createSsl"></a>[function <span class="apidocSignatureSpan">grpc.ServerCredentials.</span>createSsl ()](#apidoc.element.grpc.ServerCredentials.createSsl)
- description and source-code
```javascript
createSsl = function () { [native code] }
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.grpc.credentials"></a>[module grpc.credentials](#apidoc.module.grpc.credentials)

#### <a name="apidoc.element.grpc.credentials.combineCallCredentials"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>combineCallCredentials ()](#apidoc.element.grpc.credentials.combineCallCredentials)
- description and source-code
```javascript
combineCallCredentials = function () {
  var current = arguments[0];
  for (var i = 1; i < arguments.length; i++) {
    current = current.compose(arguments[i]);
  }
  return current;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.credentials.combineChannelCredentials"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>combineChannelCredentials (channel_credential)](#apidoc.element.grpc.credentials.combineChannelCredentials)
- description and source-code
```javascript
combineChannelCredentials = function (channel_credential) {
  var current = channel_credential;
  for (var i = 1; i < arguments.length; i++) {
    current = current.compose(arguments[i]);
  }
  return current;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.credentials.createFromGoogleCredential"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>createFromGoogleCredential (google_credential)](#apidoc.element.grpc.credentials.createFromGoogleCredential)
- description and source-code
```javascript
createFromGoogleCredential = function (google_credential) {
  return exports.createFromMetadataGenerator(function(auth_context, callback) {
    var service_url = auth_context.service_url;
    google_credential.getRequestMetadata(service_url, function(err, header) {
      if (err) {
        common.log(grpc.logVerbosity.INFO, 'Auth error:' + err);
        callback(err);
        return;
      }
      var metadata = new Metadata();
      metadata.add('authorization', header.Authorization);
      callback(null, metadata);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.credentials.createFromMetadataGenerator"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>createFromMetadataGenerator (metadata_generator)](#apidoc.element.grpc.credentials.createFromMetadataGenerator)
- description and source-code
```javascript
createFromMetadataGenerator = function (metadata_generator) {
  return CallCredentials.createFromPlugin(function(service_url, cb_data,
                                                   callback) {
    metadata_generator({service_url: service_url}, function(error, metadata) {
      var code = grpc.status.OK;
      var message = '';
      if (error) {
        message = error.message;
        if (error.hasOwnProperty('code') && _.isFinite(error.code)) {
          code = error.code;
        } else {
          code = grpc.status.UNAUTHENTICATED;
        }
        if (!metadata) {
          metadata = new Metadata();
        }
      }
      callback(code, message, metadata._getCoreRepresentation(), cb_data);
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.credentials.createInsecure"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>createInsecure ()](#apidoc.element.grpc.credentials.createInsecure)
- description and source-code
```javascript
createInsecure = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.grpc.credentials.createSsl"></a>[function <span class="apidocSignatureSpan">grpc.credentials.</span>createSsl ()](#apidoc.element.grpc.credentials.createSsl)
- description and source-code
```javascript
createSsl = function () { [native code] }
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
