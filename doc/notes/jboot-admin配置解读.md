Jboot-admin配置文件解读

#  jboot-admin

##  app info

``` 
# app info
jboot.admin.app.name=jboot-admin管理系统
jboot.admin.app.org=Rlax
jboot.admin.app.orgWebsite=https://gitee.com/rlaxuc/jboot-admin
jboot.admin.app.resourceHost
jboot.admin.app.copyRight=2017 © copyright 京ICP备12345678号
```

##  jboot 运行模式

dev, prod, test

``` 
jboot.mode=dev
jboot.bannerEnable=true
jboot.bannerFile=banner.txt
jboot.cron4jEnable=false
jboot.cron4jFile=cron4j.properties
```

##  server engine

``` 
jboot.server.type=undertow
jboot.server.host=
jboot.server.port=8888
jboot.server.contextPath=
```

##  容错隔离jboot.hystrix 
 
 ``` 
 jboot.hystrix.url=/hystrix.stream
 jboot.hystrix.propertie
 #jboot.hystrix.keys=findPage:findPage;findById:findById
 jboot.hystrix.closeAutoHystrix=false
  ```

##  jboot.metrics
 
 ``` 
 jboot.metric.url=/metric.html
 jboot.metric.reporter=console
  ```

##  链路跟踪

``` 
jboot.tracing.type=zipkin
jboot.tracing.serviceName=jboot-admin
jboot.tracing.url=http://127.0.0.1:9411/api/v2/spans
```

##  注册中心

``` 
type default motan (support:local,motan,dubbo)
#use motan + consul
jboot.rpc.type = motan
jboot.rpc.registryType = consul
jboot.rpc.registryAddress = 127.0.0.1:8500

#use dubbo + zookeeper
jboot.rpc.type = dubbo
jboot.rpc.registryType = zookeeper
jboot.rpc.registryAddress = 127.0.0.1:2181
```

##  RPC治理

```
jboot.rpc.requestTimeOut=5000
jboot.rpc.callMode=registry
jboot.rpc.registryName=register
jboot.rpc.registryUserName
jboot.rpc.registryPassword
#rpc service config
jboot.rpc.host=127.0.0.1
jboot.rpc.defaultPort
jboot.rpc.defaultGroup=system-service
jboot.rpc.defaultVersion=1.0
#rpc hystrix config
jboot.rpc.proxy
jboot.rpc.hystrixEnable=true
jboot.rpc.hystrixTimeout=30000
jboot.rpc.hystrixKeys
jboot.rpc.hystrixAutoConfig=true
jboot.rpc.hystrixFallbackFactory
jboot.rpc.serialization=fst
```

## swagger config

``` 
jboot.swagger.path=/swaggerui
jboot.swagger.title=jboot-admin API
jboot.swagger.description=jboot-admin API
jboot.swagger.version=1.0
jboot.swagger.termsOfService=https://gitee.com/rlaxuc/jboot-admin
jboot.swagger.contactEmail=rlaxuc@gmail.com
jboot.swagger.contactName=Rlax
jboot.swagger.contactUrl=https://gitee.com/rlaxuc/jboot-admin
jboot.swagger.host=127.0.0.1:8888
```

## 配置中心

``` 
jboot.config.remoteEnable=false
jboot.config.remoteUrl
#作为配置中心
jboot.config.serverEnable=false
jboot.config.path
jboot.config.exclude
```

## 安全框架shiro  

``` 
 jboot.shiro.loginUrl=/login
 jboot.shiro.successUrl
 jboot.shiro.unauthorizedUrl=/login
```

## 缓存框架 cache config : type default ehcache (support:ehcache,redis,ehredis)
 
 ``` 
 #jboot.cache.type=redis
 #jboot.cache.redis.host=127.0.0.1
 #jboot.cache.redis.password=123456
 #jboot.cache.redis.database=0
 ```

## 消息队列 mq config : type default redis (support: redis,activemq,rabbitmq,hornetq,aliyunmq )

``` 
 #jboot.mq.type=redis
 #jboot.mq.redis.host=127.0.0.1
 #jboot.mq.redis.port=6379
 #jboot.mq.redis.password=123456
 #jboot.mq.redis.channel=message-channel
 #jboot.mq.redis.database=0  
```

![](jboot.png)