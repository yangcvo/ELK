# 搭建（ElasticSearch-2.x Logstash-2.x Kibana-4.5.x zookeeper3.4.6）Kafka为消息中心的ELK日志平台

![image](https://i.v2ex.co/2Zo3bPa3.png)
前言
Elasticsearch + Logstash + Kibana（ELK）是一套开源的日志管理方案，分析网站的访问情况时我们一般会借助Google/百度/CNZZ等方式嵌入JS做数据统计，但是当网站访问异常或者被攻击时我们需要在后台分析如Nginx的具体日志，而Nginx日志分割/GoAccess/Awstats都是相对简单的单节点解决方案，针对分布式集群或者数据量级较大时会显得心有余而力不足，而ELK的出现可以使我们从容面对新的挑战。
* Logstash：负责日志的收集，处理和储存
* Elasticsearch：负责日志检索和分析
* Kibana：负责日志的可视化


## 介绍

ELK是业界标准的日志采集，存储索引，展示分析系统解决方案

logstash提供了灵活多样的插件支持不同的输入/输出

主流使用redis / kafka作为日志/消息的中间环节

如果已有kafka的环境了，使用kafka比使用redis更佳

以下是一个最简化的配置做个笔记，弹性官网提供了非常丰富的文档

不要用搜索引擎去搜索，没多少结果的，请直接看官网文档

## ELK(Elasticsearch + Logstash + Kibana)
阅读我博客原文 - [搭建（ElasticSearch-2.x Logstash-2.x Kibana-4.5.x zookeeper3.4.6）Kafka为消息中心的ELK日志平台](http://blog.yangcvo.me/2016/12/29/%E6%97%A5%E5%BF%97%E5%88%86%E6%9E%90%10%E5%B9%B3%E5%8F%B0/Elasticsearch/%E6%90%AD%E5%BB%BA(ElasticSearch-2.x%20Logstash-2.x%20Kibana-4.5.x%20zookeeper3.4.6)%20Kafka%E4%B8%BA%E6%B6%88%E6%81%AF%E4%B8%AD%E5%BF%83%E7%9A%84ELK%E6%97%A5%E5%BF%97%E5%B9%B3%E5%8F%B0/)

### 组件预览
* JDK - http://www.oracle.com/technetwork/java/javase/downloads/index.html
* Elasticsearch - https://www.elastic.co/downloads/elasticsearch
* Logstash - https://www.elastic.co/downloads/logstash
* Kibana - https://www.elastic.co/downloads/kibana
* redis - http://redis.io/download


#### 个人blog：blog.yangcvo.me  

* elk的安装和使用配置，集群的搭建，tomcat，Java日志收集，都有写。
* elk走kafka存储消费，定期清理日志。

有什么问题可以联系我或者加我QQ：1155958741

Mail: yangcvo@gmail.com
