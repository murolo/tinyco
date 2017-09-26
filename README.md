# tinyco
[![Build Status](https://travis-ci.org/daoluan/tinyco.svg?branch=master)](https://travis-ci.org/daoluan/tinyco)

tinyco is a framework with **high performance and high efficiency** focusing on business with which you can build a server in only couple lines of code. It use coroutine implemented in ucontext syscall.

# Features
- High performance. Make full use of CPU and process requests concurrently which makes server's throughput greatly improved
- Perfect http/dns components
- Small kernel in size
- Business code can be easy to read and maintained. No more async framework

# How to start ?
Clone tinyco and build it:

    % git clone https://github.com/daoluan/tinyco.git
    % cd tinyco
    % git submodule update --init --recursive

    % make thirdparty
    
    % cd ./third-party/c-ares/ && cmake -DCARES_STATIC=ON . && make; cd -
    % cd ./third-party/libevent/ && cmake . && make && cd -
    % cd ./third-party/jsoncpp/ && cmake . && make && cd -
    % cmake . && make

It's very easy to DIY your tinyco-server. You can refer to [this](https://github.com/daoluan/tinyco/blob/master/example/server/main.cc). 

For more usages, Read [here](https://github.com/daoluan/tinyco/tree/master/example).
