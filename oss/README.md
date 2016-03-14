# OpenSource Libraries for software development


## ZeroMQ

ZeroMQ is low level and blazing fast networking library. It provides some very good abstractions for designing systems that interact via network-io and has bindings in almost all languages. You might like to read ZmqGuide for brushing up your system design concepts.

Site : http://zeromq.org/  
Download: http://zeromq.org/intro:get-the-software  
Guide: http://zguide.zeromq.org/page:all  


## Folly: Facebook Open-source Library

Folly contains variety of core library components used extensively at Facebook. One of the best thing is that it has buch of libraries built around to write performant asynhronous code execution (e.g. Futures, EventBase) and asynchronous IO. 

Site/Download: https://github.com/facebook/folly  
Overview: https://github.com/facebook/folly/blob/master/folly/docs/Overview.md  

You might have to dig into header files of associated file for learning about how to use them. Code is very well documented with example usecases.

### What I use this for
- **io/** : Collection of useful abstractions for high performance sync/async network/disk IO
- **async/**: Provides bunch of libraries for writing asynchronous C++ applications (EventBase, AsyncTimeout)
- **futures/**: C++ version of Twitter-Finagle framework for writing asynchronous C++ applications using Promise/Future pattern
- **Conv.h**: Variety of data conversion routines (to and from string)
- **MPMCQuery.h**: One of the best thing for doing pipleline execution with multiple producer and consumers
- **stats/**: Collection of efficient utilities for collecting statistics
- **Synchronized.h**: High level synchronization library


## FbThrift

Thrift is a software framework for scalable cross-langauage service deplyoment (RPC with Server-Client architecture). FbThrift is a fork of Thrift with C++11 support and some Facebook specific modifications. 

Site: http://thrift.apache.org/ (Apache Thrift)  
Download: https://github.com/facebook/fbthrift  
Documentation: http://thrift.apache.org/docs/  
Tutorial: http://thrift.apache.org/tutorial/py (Very easy to get started with)  

### Thrift protocols and ZeroMQ combination
You can also use thrift to serialize/deserialize objects. E.g. ZeroMQ combined with thrift encoding is a powerful, robust and easy way to write distributed networking applications.
