# 项目简介
本项目是《使用Spring Cloud与Docker实战微服务》：

http://git.oschina.net/itmuch/spring-cloud-book

http://www.github.com/eacdy/spring-cloud-book

Docker章节的配套代码，如有疑问，请移步至spring-cloud-book地址。



微服务架构交流QQ群：157525002，欢迎加入。

微服务架构讨论社区：[http://ask.itmuch.com/](http://ask.itmuch.com/)，欢迎加入。



内容主要包含：

| 微服务角色                 | 对应的技术选型                              |
| --------------------- | ------------------------------------ |
| 注册中心(Register Server) | Eureka                               |
| 服务提供者                 | spring mvc、spring-data-jpa、h2等       |
| 服务消费者                 | Ribbon消费服务提供者的接口                     |
| 熔断器                   | Hystrix，包括Hystrix Dashboard以及Turbine |
| API Gateway           | Zuul                                 |

本篇旨在使用spring-cloud和docker构建一个最为简单的运行环境，有关Spring Cloud的系统讲解，请前往

http://git.oschina.net/itmuch/spring-cloud-book

http://www.github.com/eacdy/spring-cloud-book



# 准备

## 环境准备：

| 工具     | 版本或描述                |
| ------ | -------------------- |
| JDK    | 1.8                  |
| IDE    | STS 或者 IntelliJ IDEA |
| Maven  | 3.x                  |
| Docker | 1.12.1               |



## 主机规划：

| 项目名称                                     | 端口   | 描述                  | URL             |
| ---------------------------------------- | ---- | ------------------- | --------------- |
| microservice-api-gateway                 | 8050 | API Gateway         | 详见文章            |
| microservice-consumer-movie-ribbon-with-hystrix | 8011 | Ribbon Hystrix Demo | /ribbon/1       |
| microservice-discovery-eureka            | 8761 | 注册中心                | /               |
| microservice-hystrix-dashboard           | 8030 | hystrix监控           | /hystrix.stream |
| microservice-hystrix-turbine             | 8031 | turbine             | /turbine.stream |
| microservice-provider-user               | 8000 | 服务提供者               | /1              |
|                                          |      |                     |                 |

