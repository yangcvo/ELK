# 使用ELK(Elasticsearch + Logstash + Kibana) 搭建日志集中分析平台实践

![image](https://i.v2ex.co/2Zo3bPa3.png)
前言
Elasticsearch + Logstash + Kibana（ELK）是一套开源的日志管理方案，分析网站的访问情况时我们一般会借助Google/百度/CNZZ等方式嵌入JS做数据统计，但是当网站访问异常或者被攻击时我们需要在后台分析如Nginx的具体日志，而Nginx日志分割/GoAccess/Awstats都是相对简单的单节点解决方案，针对分布式集群或者数据量级较大时会显得心有余而力不足，而ELK的出现可以使我们从容面对新的挑战。
* Logstash：负责日志的收集，处理和储存
* Elasticsearch：负责日志检索和分析
* Kibana：负责日志的可视化
### ELK(Elasticsearch + Logstash + Kibana)
阅读原文 - http://wsgzao.github.io/post/elk

* CentOS 7.x安装ELK(Elasticsearch+Logstash+Kibana) - 
* * http://www.chenshake.com/centos-install-7-x-elk-elasticsearchlogstashkibana/
     Centos 6.5 安装nginx日志分析系统 elasticsearch + logstash + redis + kibana -          
http://blog.chinaunix.net/xmlrpc.php?r=blog/article&uid=17291169&id=4898582
     logstash-forwarder and grok examples - https://www.ulyaoth.net/threads/logstash-forwarder-and-grok-examples.32413/
*    三斗室 - http://chenlinux.com/
elastic - https://www.elastic.co/guide
LTMP索引 - http://wsgzao.github.io/index/#LTMP

###组件预览
* JDK - http://www.oracle.com/technetwork/java/javase/downloads/index.html
* Elasticsearch - https://www.elastic.co/downloads/elasticsearch
* Logstash - https://www.elastic.co/downloads/logstash
* Kibana - https://www.elastic.co/downloads/kibana
* redis - http://redis.io/download
