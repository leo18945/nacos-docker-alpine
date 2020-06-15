# Nacos Docker

![Docker Pulls](https://img.shields.io/docker/pulls/nacos/nacos-server.svg?maxAge=60480)

This project is rebuild of official nacos based on **alpine**, please refer to official website(https://github.com/alibaba/nacos).

## Project directory

* build：The source code of make a docker image for nacos server.
* env: Environment variable file for compose yaml, please change the default settings.
* init.d: The properties file for customize your nacos server.


## Quick Start

Run the following command：

* Clone project

  ```shell
  git clone --depth 1 https://github.com/leo18945/nacos-docker-alpine.git
  cd nacos-docker
  ```

* Standalone Mysql

  ```shell
  docker-compose up -d
  ```

* Open the Nacos console in your browser

  link：http://127.0.0.1:8848/nacos/  
  The default username & password are nacos.
