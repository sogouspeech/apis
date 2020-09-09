# Sogou AI Platform APIs

This repository contains the original interface definitions of public
Sogou AI Platform APIs that support both REST and gRPC protocols. Reading the
original interface definitions can provide a better understanding of
Sogou AI Platform APIs and help you to utilize them more efficiently. You can also
use these definitions with open source tools to generate client
libraries, documentation, and other artifacts.

For more details on Sogou Speech APIs and developer tools, see the [Sogou AI Documentation](https://ai.sogou.com/docs/) site.

## Overview

Sogou AI Platform APIs are typically deployed as API services that are hosted
under different DNS names. One API service may implement multiple APIs
and multiple versions of the same API.

Sogou AI Platform APIs use [Protocol Buffers](https://github.com/google/protobuf)
version 3 (proto3) as their Interface Definition Language (IDL) to
define the API interface and the structure of the payload messages. The
same interface definition is used for both REST and RPC versions of the
API, which can be accessed over different wire protocols.

There are several ways of accessing Sogou AI Platform APIs:

1.  JSON over HTTP: You can access all Sogou AI Platform APIs directly using JSON
over HTTP.

2.  Protocol Buffers over gRPC: You can access Sogou AI Platform APIs published
in this repository through [GRPC](https://github.com/grpc), which is
a high-performance binary RPC protocol over HTTP/2. It offers many
useful features, including request/response multiplex and full-duplex
streaming.

3.  [Sogou AI Platform SDKs](https://ai.sogou.com):
You can use these sdks to access Sogou Speech APIs. They are based
on gRPC for better performance and provide idiomatic client surface for
better developer experience.

## Discussions

This repo contains copies of Sogou Speech API definitions and related files.  For
discussions or to raise issues, please visit our [official site](https://ai.sogou.com/),
see the contact us section or follow our wechat public account.

## Repository Structure

This repository uses a directory hierarchy that reflects the Sogou Speech
API product structure. In general, every API has its own root
directory, and each major version of the API has its own subdirectory.
The proto package names exactly match the directory: this makes it
easy to locate the proto definitions and ensures that the generated
client libraries have idiomatic namespaces in most programming
languages.

**NOTE:** The major version of an API is used to indicate breaking
change to the API.

## Generate gRPC Source Code

To generate gRPC source code for Sogou Speech APIs in this repository, you
first need to install both Protocol Buffers and gRPC on your local
machine, then you can follow the instructions of [gRPC official site](https://grpc.io/docs/) to generate the
source code. You need to integrated the generated source code into
your application build system.

### Go gRPC Source Code
It is difficult to generate Go gRPC source code from this repository,
since Go has different directory structure.
Please use [this repository](https://github.com/sogouspeech/go-genproto) instead.
