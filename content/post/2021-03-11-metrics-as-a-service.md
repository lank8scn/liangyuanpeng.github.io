---
layout:     post 
slug:      "metrics-as-a-service"
title:      "metrics托管服务即将发布"
subtitle:   ""
description: "在云原生时代,每时每刻都有metrics被prometheus定时抓取.."
date:       2021-03-11
author:     "lyp"
image: "https://res.cloudinary.com/lyp/image/upload/v1544363191/hugo/blog.github.io/743a4e9227e1f14cb24a1eb6db29e183.jpg"
published: true
tags:
    - Metrics
    - Prometheus
    - SAAS
categories: 
    - CloudNative
---  

# 前言  

现在很多人都在使用静态博客来记录自己的内容，但动态博客依然还有很多存在，也许永远也不会消失。最近几年一个基于SpringBoot编写的Blog正在慢慢变得火热起来，那就是Halo，而Java编写的其他博客或其他系统也不少,这些系统都像烟囱一样部署在各自的服务器上。  

一般人们不会专门为了自己的一个小网站专门去部署监控的内容，毕竟在大流量来临之前没必要去花这些功夫，但是了解自己线上系统运行情况还是非常需要有一个监控存在的。  

#  产品介绍  

用户只需要暴露标准的prometheus exporter给平台抓取metrics即可，然后可以在专属的Grafana页面看到自己的程序运行时情况，下面以JVM程序为例给个图：   

![metrics-jvm](https://res.cloudinary.com/lyp/image/upload/v1615419259/hugo/blog.github.io/saas/prometheus/metrics-jvm.png)    

## 支持的exporter类型  

1. JVM Micrometer exporter
2. Node exporter  
3. Redis exporter  
4. Nginx exporter  

#  产品定价   


|  |  天使用户|  基础版   | 高级版  |
|  ----|  ----|  ----  | ----  |
| 价格 | 30/年| 69/年  | 待定/年 |
| metrics应用数 | 3| 3  | 待定 |
| 数据保存 | 两个月| 两个月  | 一年 |
| Node Exporter | √| √  | √ |
| Redis Exporter | √| √  | √ |
| Nginx Exporter | √| √  | √ |
| 邮件告警 | √| √ | √ |
| 钉钉告警 | ×| ×  | √ |
|独立Prometheus实例 | ×| × | √ |
|独立Grafana实例 | ×| × | √ |
|存储空间 | 待定| 待定 | 待定 |
|自定义Grafana DashBoard id | 待定| 待定 | 待定 |
|自定义Metrics抓取间隔 | ×| × | √ |
|Prometheus自定义远程数据存储 | ×| × | √ |
|部署节点 | 香港| 香港 | 香港 |    


现在我们正在寻找天使用户`50名`,可拥有以30元(一顿快餐的事)购买基础版的永久账号,如果你有想法请联系我们!可以直接在下面评论也可以发邮件给我,甚至是加我的微信联系我(请备注Metrics托管服务天使用户).  

除了基础版和高级版还计划会推出一个尊享版,可完全掌控的Prometheus实例、Grafana实例和AlertManager实例,当然数据存储依然是另算了.  

我们还将计划支持Apache、tomcat等exporter,由于基础版只支持3个exporter数,如果您希望在基础版使用更多exporter可付费支持,每增加一个exporter将需要付费12元/年,平均一个月只需1块钱.

如果使用了[Halo as a service](https://liangyuanpeng.com/post/2021-03-11-halo-as-a-service/)，则可免费享用基础版.
