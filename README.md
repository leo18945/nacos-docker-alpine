# Nacos Docker
[![automated](https://badgen.net/badge/icon/docker?icon=docker&label)](https://hub.docker.com/r/leo18945/alpine-jre8-nacos "Go to Docker hub")
![](https://img.shields.io/github/last-commit/leo18945/nacos-docker-alpine.svg)
![](https://badgen.net/docker/size/leo18945/alpine-jre8-nacos/1.3.0)

![](https://img.shields.io/badge/alpine-green.svg?logo=alpine-linux)
![](https://img.shields.io/badge/jdk-1.8-green.svg?logo=java)
![](https://img.shields.io/badge/nacos-1.3.0-green.svg)

[![Try in PWD](https://raw.githubusercontent.com/play-with-docker/stacks/master/assets/images/button.png)](https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/leo18945/nacos-docker-alpine/master/docker-compose.yml)

This project is rebuild of official nacos(1.3.0) based on **alpine**, please refer to official website(https://github.com/alibaba/nacos).

## Project directory

* build：The source code of make a docker image for nacos server.
* env: Environment variable file for compose yaml, please change the default settings.
* init.d: The properties file for customize your nacos server.


## Quick Start

Run the following command：

* Clone project

  ```shell
  git clone --depth 1 https://github.com/leo18945/nacos-docker-alpine.git

  cd nacos-docker-alpine
  ```

* Standalone Mysql

  ```shell
  docker-compose up -d
  ```

* Open the Nacos console in your browser

  link：http://127.0.0.1:8848/nacos/  
  The default username & password are nacos.
