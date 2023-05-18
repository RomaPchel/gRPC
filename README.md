gRPC in 3 minutes (Node.js)
===========================

PREREQUISITES
-------------

- `node`: This requires Node 0.12.x or greater.

INSTALL
-------

   ```sh
   $ # Get the gRPC repository
   $ export REPO_ROOT=grpc # REPO root can be any directory of your choice
   $ git clone -b RELEASE_TAG_HERE https://github.com/grpc/grpc $REPO_ROOT
   $ cd $REPO_ROOT

   $ cd examples/gRPC
   $ npm install
   ```

TRY IT!
-------

There are two ways to generate the code needed to work with protocol buffers in Node.js - one approach uses [Protobuf.js](https://github.com/dcodeIO/ProtoBuf.js/) to dynamically generate the code at runtime, the other uses code statically generated using the protocol buffer compiler `protoc`. The examples behave identically, and either server can be used with either client.

 - Run the server

   ```sh
   $ # from this directory
   $ gRPC ./dynamic_codegen/agri_server.js &
   $ # OR
   $ gRPC ./static_codegen/agri_server.js &
   ```

 - Run the client

   ```sh
   $ # from this directory
   $ gRPC ./dynamic_codegen/agri_client.js
   $ # OR
   $ gRPC ./static_codegen/agri_client.js
   ```

TUTORIAL
--------
You can find a more detailed tutorial in [gRPC Basics: Node.js][]

[Install gRPC Node]:../../src/node
[gRPC Basics: Node.js]:https://grpc.io/docs/languages/node/basics
