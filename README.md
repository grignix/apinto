# Apinto

[![Go Report Card](https://goreportcard.com/badge/github.com/eolinker/apinto)](https://goreportcard.com/report/github.com/eolinker/apinto) [![Releases](https://img.shields.io/github/release/eolinker/apinto/all.svg?style=flat-square)](https://github.com/eolinker/apinto/releases) [![LICENSE](https://img.shields.io/github/license/eolinker/apinto.svg?style=flat-square)](https://github.com/eolinker/apinto/blob/main/LICENSE)![](https://shields.io/github/downloads/eolinker/apinto/total)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT_CN.md)

------------
![](http://data.eolinker.com/course/eaC48Js3400ffd03c21e36b3eea434dce22d7877a3194f6.png)

**Apinto is a high-performance, scalable, and easy-to-maintain cloud-native API gateway. **

Apinto Gateway is developed based on the GO language modularization, can be deployed in 5 minutes, is simple to configure, easy to maintain, supports clustering and dynamic expansion, and provides dozens of gateway plug-ins and practical enterprise-level plug-ins, allowing users to use it out of the box.

## Demo 
Experience Address：[demo-dashboard.apinto.com](https://demo-dashboard.apinto.com/)

Provides three trial accounts to avoid being squeezed out by other users

account：apinto-1

password：12345678

account：apinto-2

password：12345678

account：apinto-3

password：12345678

Quick Start：https://help.apinto.com/docs/dashboard-v2/quick/quick_start.html

Apinto Dashboard github地址： https://github.com/eolinker/apinto-dashboard

## Apinto functional architecture diagram:
<img width="1664" alt="img_v2_22590d84-f8a4-4d3a-9c67-b481ecfdf1fg" src="https://user-images.githubusercontent.com/18322454/228448223-515a7feb-0c65-496e-85bc-1581b7a89cfe.png">

## Apinto Highlights
 Apinto API Gateway features an excellent user experience and a console suitable for various enterprise-level business scenarios. The console has four highlight functions: cluster management, application management, fine-grained service governance and enterprise plug-ins, which can meet the requirements of enterprises for more advanced scenario-based needs of API gateways.
### Cluster Management
 Apinto provides cluster management functions, which can configure services at one time and publish them to the corresponding clusters. This solves the problem of maintaining multiple sets of business configurations in multiple clusters, significantly improves operation and maintenance efficiency, and reduces the accident rate during complex configurations.
![](http://data.eolinker.com/course/Cdkvdtkdcc50a65d3e5b068bae658c343d7b6a188730218.png)
### Application Management
Apinto Gateway introduces the concept of application management to uniformly manage applications and their lifecycles. As the initiator of business communication, applications run through the entire call chain. Apinto Gateway authenticates and manages the traffic requested by applications, monitors and alerts the requested traffic, and counts the application calls.
### Fine-grained service governance
Apinto proposes a fine-grained traffic management solution, that is, all request traffic from the caller passes through the gateway, and the request traffic is filtered by combining conditions such as application, API, upstream service, request method, IP, request path, and application custom tags, and policy rules such as limit, access, fuse, grayscale, and cache are implemented to help enterprises quickly and flexibly formulate strategies to meet the needs of different business scenarios and manage services in all aspects.
![](http://data.eolinker.com/course/zqIaYaa0ac1273511504a4bad96e0e78de56e8e12850677.png)
### Enterprise plugins
Apinto Gateway will soon launch enterprise plugin modules, and will continue to provide business-oriented enterprise plugins such as: user role permissions, monitoring alarms, logs, API documents, open platforms, security protection, data analysis, call chains, mocks, online debugging, security testing, national encryption, multiple protocols, etc. Support user-defined enterprise plugins and independent deployment.
## Apinto Features
Apinto Gateway can be used as the entrance to business traffic and can process business traffic, such as dynamic routing, load balancing, service discovery, circuit breaking and downgrading, identity authentication, monitoring and alarming, etc.
Apinto Gateway is not restricted by cloud platforms and can also run on Kubernetes.


### Product Features
| Features | Description |
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

## Iteration plan
![image](https://user-images.githubusercontent.com/18322454/226301243-d69a1a5e-22eb-48d4-8fd1-52ec1cf8237b.png)
If you are an individual developer, you can develop valuable gateway plug-ins or enterprise-level plug-ins based on business scenarios related to the API gateway, and are willing to share them with Apinto. You will become an outstanding contributor to Apinto or get certain benefits.
If you are an enterprise, you can develop enterprise-level plug-ins based on the Apinto gateway and become an Apinto partner.

### Star History

[![Star History Chart](https://api.star-history.com/svg?repos=eolinker/apinto&type=Date)](https://star-history.com/#eolinker/apinto&Date)


## Benchmarks


![image](https://user-images.githubusercontent.com/25589530/149748340-dc544f79-a8f9-46f5-903d-a3af4fb8b16e.png)

## deploy
* Direct deployment: [Deployment tutorial](https://help.apinto.com/docs/apinto/quick/arrange)
* [Quick start tutorial](https://help.apinto.com/docs/dashboard-v2/quick/quick_start.html)
* [Source code compilation tutorial](https://help.apinto.com/docs/apinto/quick/arrange)
* [Docker deployment](https://hub.docker.com/r/eolinker/apinto-gateway)
* Kubernetes deployment: Subsequent support

## Start

1. Download the installation package and unzip it (here is the installation package of version v0.12.1 as an example)

```
wget https://github.com/eolinker/apinto/releases/download/v0.12.1/apinto_v0.12.1_linux_amd64.tar.gz && tar -zxvf apinto_v0.12.1_linux_amd64.tar.gz && cd apinto
```

Apinto supports running on arm64 and amd64 architectures.

Please download the installation package for the corresponding architecture and system as needed. For installation package download, please click [click](https://github.com/eolinker/apinto/releases/) to jump

2. Install the gateway:
```shell
./install.sh install
```
Executing this step will generate configuration files `/etc/apinto/apinto.yml` and `/etc/apinto/config.yml`, which can be modified as needed.

3. Start the gateway:

```
apinto start
```

### Bug and demand feedback
If you want to report bugs and provide product feedback, you can create a Github issue to contact us, thank you very much!

If you want to communicate closely with the Apinto team, discuss product usage tips and learn more about the latest product developments, welcome to join the following channels.

- ## **Contact us**


* **Help documentation**: [https://help.apinto.com](https://help.apinto.com/docs)

- **Official website**: [https://www.apinto.com](https://www.apinto.com/)

- **Forum**: [https://community.apinto.com](https://community.apinto.com/)

- **WeChat group**: <img src="http://data.eolinker.com/course/2HdT4zd10b670318462bec90f0f390bef896c21cad66172.png" style="width:150px" />


