# Apinto

[![Go Report Card](https://goreportcard.com/badge/github.com/eolinker/apinto)](https://goreportcard.com/report/github.com/eolinker/apinto) [![Releases](https://img.shields.io/github/release/eolinker/apinto/all.svg?style=flat-square)](https://github.com/eolinker/apinto/releases) [![LICENSE](https://img.shields.io/github/license/eolinker/apinto.svg?style=flat-square)](https://github.com/eolinker/apinto/blob/main/LICENSE)![](https://shields.io/github/downloads/eolinker/apinto/total)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT_CN.md)

------------
![](http://data.eolinker.com/course/eaC48Js3400ffd03c21e36b3eea434dce22d7877a3194f6.png)

**Apinto是一款高性能、可扩展、易维护的云原生API网关。**

Apinto网关基于GO语言模块化开发，5分钟极速部署，配置简单、易于维护，支持集群与动态扩容，并且提供几十款网关插件和实用的企业级插件，让用户开箱即用。

## Demo 
体验地址：[demo-dashboard.apinto.com](https://demo-dashboard.apinto.com/)

提供了三个试用账号，避免被使用者挤下来

账号：apinto-1

密码：12345678

账号：apinto-2

密码：12345678

账号：apinto-3

密码：12345678

快速入门：https://help.apinto.com/docs/dashboard-v2/quick/quick_start.html

Apinto Dashboard github地址： https://github.com/eolinker/apinto-dashboard

## Apinto功能架构图：
<img width="1664" alt="img_v2_22590d84-f8a4-4d3a-9c67-b481ecfdf1fg" src="https://user-images.githubusercontent.com/18322454/228448223-515a7feb-0c65-496e-85bc-1581b7a89cfe.png">

## Apinto亮点特性
 Apinto API 网关以出色的用户体验和适用于各种企业级业务场景的控制台为特色。控制台具有四大亮点功能：集群管理、应用管理、精细服务治理和企业插件，能够满足企业对 API 网关更高级场景化需求的要求。 
### 集群管理
 Apinto 提供集群管理功能，可以一次性配置业务并将其发布到相应的集群。这解决了多集群维护多套业务配置的问题，显著提高了运维效率，并降低了繁杂配置时的事故率。
![](http://data.eolinker.com/course/Cdkvdtkdcc50a65d3e5b068bae658c343d7b6a188730218.png)
### 应用管理
 Apinto 网关推出应用管理概念，统一管理应用及其生命周期。作为业务通讯的发起者，应用贯穿整个调用链。Apinto 网关对应用请求的流量进行鉴权认证和服务治理，并对请求的流量进行监控告警，统计应用调用情况。
### 精细化服务治理
Apinto提出精细化流量管理方案，即所有调用方的请求流量都经过网关，通过对应用、API、上游服务、请求方式、IP、请求路径、应用自定义标签等组合条件筛选请求流量，执行限量、访问、熔断、灰度、缓存等策略规则，帮助企业快速、灵活地制定策略，以满足不同业务场景的需求，并全方位治理好服务。
![](http://data.eolinker.com/course/zqIaYaa0ac1273511504a4bad96e0e78de56e8e12850677.png)
### 企业插件
Apinto网关即将推出企业插件模块，并且陆续提供业务型企业插件如：用户角色权限、监控告警、日志、API文档、开放平台、安全防护、数据分析、调用链、mock、在线调测、安全测试、国密、多协议等。支持用户自定义企业插件，支持独立部署。
## Apinto功能
Apinto网关可以作为业务流量的入口，可以对业务流量进行处理，如动态路由、负载均衡、服务发现、熔断降级、身份认证、监控与告警等。
Apinto网关不受云平台限制，也能在Kubernetes运行。


### 产品特性

| 功能         | 描述                                                         |
| ------------ | ------------------------------------------------------------ |
| Cluster | The cluster does not limit the gateway nodes, and the gateway nodes can be removed or added freely. The master and slave gateway nodes have seamless switching functions to improve the high availability of the gateway |
| Dynamic routing | You can match the corresponding service by setting parameters such as location, query, header, host, method, etc. |
| Service discovery | Supports docking with Eureka, Nacos, and Consul |
| Load balancing | Supports polling weight algorithm |
| User authentication | Anonymous, Basic, Apikey, JWT, AK/SK authentication |
| SSL certificate | Manage multiple certificates |
| Access domain name | You can set the access domain name for the gateway |
| Health check | Support health checks on the nodes of the load to ensure the robustness of the service |
| Protocol | HTTP/HTTPS, Webservice, Restful, gRPC, Dubbo2, SOAP |
| Plug-in | Process plug-in, load required modules on demand |
| OPEN API | Support the use of open api configures gateway |
| Log | Provides node operation logs, which can be output according to the level of log settings |
| Multiple log outputs | Node request logs can be output to different log receivers, such as file, nsq, kafka, etc. |
| Cli command support | Control the gateway through Cli commands, and operations such as plug-in installation, download, and gateway opening and closing can all be controlled with one-click commands |
| Blacklist and whitelist | Support multi-dimensional traffic filtering, set blacklist and whitelist IPs, and intercept illegal IPs |
| Access policy | Support multi-dimensional traffic filtering, and set blacklist and whitelist for multi-dimensional combinations such as application, IP, application and IP, application and API, application and upstream |
| Traffic policy | Support multi-dimensional traffic filtering, control the number of requests and request message size limits between applications, applications and APIs, and applications and upstreams |
| Circuit breaker policy | Support multi-dimensional traffic filtering, circuit breaker upstream or API |
| Grayscale policy | Support multi-dimensional traffic filtering, grayscale traffic to target nodes by percentage or advanced rules |
| Cache policy | Support multi-dimensional traffic filtering, cache API response content |
| Parameter Mapping | Map the client's request parameters to the forwarding request, and change the position and name of the parameters as needed |
| Additional Parameters | When forwarding a request, add additional backend verification parameters, such as apikey, etc. |
| Forward Rewrite | Supports rewriting of `scheme`, `uri`, and `host`, and supports adding or deleting the value of the request header of the forwarded request |
| Traffic Mirroring | Copy online traffic or request content to the mirror service |
| MOCK | Simulate the response of the web server-side API |
| CORS | Support cross-domain API requests |
| Synchronous API | Provide OpenAPI synchronous API documents, support swagger3.0 json or yaml format files |

## 迭代计划
![image](https://user-images.githubusercontent.com/18322454/226301243-d69a1a5e-22eb-48d4-8fd1-52ec1cf8237b.png)
如果您是个人开发者，可基于API网关相关的业务场景开发有价值的网关插件或企业级插件，并且愿意分享给Apinto，您将会成为Apinto的杰出贡献者或得到一定的收益。
如果您是企业，可基于Apinto网关开发企业级插件，成为Apinto的合作伙伴。

### Star历史

[![Star History Chart](https://api.star-history.com/svg?repos=eolinker/apinto&type=Date)](https://star-history.com/#eolinker/apinto&Date)


## 基准测试


![image](https://user-images.githubusercontent.com/25589530/149748340-dc544f79-a8f9-46f5-903d-a3af4fb8b16e.png)

## 部署

* 直接部署：[部署教程](https://help.apinto.com/docs/apinto/quick/arrange)
* [快速入门教程](https://help.apinto.com/docs/dashboard-v2/quick/quick_start.html)
* [源码编译教程](https://help.apinto.com/docs/apinto/quick/arrange)
* [Docker部署](https://hub.docker.com/r/eolinker/apinto-gateway)
* Kubernetes部署：后续支持

## 启动

1.下载安装包并解压（此处以v0.12.1版本的安装包示例）

```
wget https://github.com/eolinker/apinto/releases/download/v0.12.1/apinto_v0.12.1_linux_amd64.tar.gz && tar -zxvf apinto_v0.12.1_linux_amd64.tar.gz && cd apinto
```

Apinto支持在arm64、amd64架构上运行。

请根据需要下载对应架构及系统的安装包，安装包下载请[点击](https://github.com/eolinker/apinto/releases/)跳转

2. 安装网关：
```shell
./install.sh install
```
执行该步骤将会生成配置文件`/etc/apinto/apinto.yml`和`/etc/apinto/config.yml`，可根据需要修改。

3.启动网关：

```
apinto start
```

### Bug 和需求反馈
如果想要反馈 Bug、提供产品意见，可以创建一个 Github issue 联系我们，十分感谢！

如果你希望和 Apinto 团队近距离交流，讨论产品使用技巧以及了解更多产品最新进展，欢迎加入以下渠道。


- ## **联系我们**


* **帮助文档**：[https://help.apinto.com](https://help.apinto.com/docs)

- **官网**：[https://www.apinto.com](https://www.apinto.com/)
- **论坛**：[https://community.apinto.com](https://community.apinto.com/)
- **微信群**：<img src="http://data.eolinker.com/course/2HdT4zd10b670318462bec90f0f390bef896c21cad66172.png" style="width:150px" />


