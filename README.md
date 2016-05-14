# RunBPM v1.0发布筹备中 2016-05-13

欢迎加微信/QQ: 914454333
近期正在编写工作台web演示，说明文档中。每2-3天update进度.

#Why RunBPM

1. **易用**。几行代码就可以将完整的BPMN 2.0业界规范运转起来，以轻量级的姿态分分钟嵌入到应用系统提供BPM功能，提供丰富的API,同时考虑到中国本地化的需求。

2. **功能齐全**。具有完整的流程设计器、流程引擎与监控优化功能。强调稳定性与性能。除了内嵌，流程引擎可以集群部署在IBM WAS/Oracle WLS之上；针对并发冲突的任务列表，在数据库模式设计方面适当的考虑了用空间换取时间；实例运行库可以选择关系型数据库，同时支持Redis。

3. **开源**。遵从Apache License 2.0协议的BPM产品，微信技术群随时讨论新功能，联系到作者,分分钟增加到产品中。

#下载

  
* 流程引擎：<https://github.com/liguo-zhang/runbpm-modeler>
  已经基本可用,基于Java，直接下载就是一个Java工程。
  可以运行引擎的单元测试了解所有的功能，一个一个的跑。有任何问题与我联系。
  org.runbpm.service.RuntimeService是最终对外公开API的主要接口。
  org.runbpm.service.ServiceSampleTest是最终对外使用的样例。

* 流程工作台：<https://github.com/liguo-zhang/runbpm-workspace>
  开发中。。。

* 流程设计器：<https://github.com/liguo-zhang/runbpm-engine> 基于Node.js,目前有一个可用的版本：<http://pan.baidu.com/s/1jH7mZTO>,直接打开index.html在浏览器器中使用。
  
![sreenshot](https://raw.githubusercontent.com/liguo-zhang/runbpm-modeler/master/docs/screenshot.png)



#进度

2015年12月21日 
*.[流程引擎]完成核心的分层设计、包设计、类设计：Definition/Model包、Instance包、Container包、USER包、Global包
*.[流程引擎]基于XPDL定义的流程定义的雏形，JAXB流程定义加载设计与实现
*.[流程引擎]内存形式的储存设计与实现，让工作流尽快跑起来
------
2015年12月25日
*.[流程引擎]异常设计与实现、错误信息输出格式
*.[流程引擎]流程引擎核心流转算法实现
*.[流程引擎]JUnit单元测试用例
*.[流程引擎]跳转 流程形参/实参 子流程

2015年12月26日下午7:21:06 
1.[流程引擎]转向BPMN 2.0规范，将定义以及引擎实现重构

2016年01月04日
*.[流程引擎]逻辑表达式支持Juel与AviatorEvaluator
*.[流程引擎]基本的任务分配管理： 组织机构接口模型、Claim抢任务、会签任务
*.[流程引擎]BPMN 2.0的SubProcess模型 - XPDL中的块活动ActivitySet

2016年01年23月
* [流程引擎]BPMN 2.0的CallActivity 流程模型 - XPDL的子流程
* [流程引擎]BPMN 2.0的SubProcess模型支持嵌套
* [流程引擎]Hibernate持久存储/Spring集成
* [流程引擎]Native API
* [流程引擎]REST API

2016年2月15日
* [流程引擎]动态类决定执行人和转移条件
* [流程引擎]流程各种对象挂起、恢复的实现
* [流程引擎]流程定义的扩展属性
* [流程引擎]事件接口,slf4j日志
* [流程引擎]历史库处理
* [流程引擎]引入Redis支持
* [流程引擎]支持流程运行库与流程历史库均使用RDBS并行处理
* [流程引擎]支持流程运行库与流程历史库均使用NoSQL并行处理
* [流程引擎]支持流程运行库使用NoSQL,与流程历史库使用RDBS并行处理
* [流程引擎]支持基于Java POJO模型的流程建模

2016年5月11日
* [设计器]基于bpmn.io完成初版设计器
* [流程引擎]BPMN Schema 
* [流程引擎]用户自定义的扩展属性SCHEMA 
* [流程引擎]特定流程、活动、userTask的监听
* [流程引擎]放回任务

