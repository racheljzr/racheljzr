---
layout: post
title: 【Java】
categories: Interview
---
【目录】

##### 1.加载顺序
##### 2.多线程
##### 3.相等
##### 4.类型
##### 5.trycatchfinally
##### 6.String
##### 7.SpringMVC重定向
##### 8.ArrayList容量扩充
##### 9.集合接口
##### 10.case 穿透
##### 11.Contructor
##### 12.单例
##### 13.反射
##### 14.线程池
##### 15.Redis
##### 16.Dubbo
##### 17.Foreach
##### 18.Spring
##### 19.web程序的启动顺序
##### 20.生产消费者模式
##### 21.ClassLoader双亲委派机制
##### 22.volatile和synchronized的区别
##### 23.Myqsql常见优化
##### 24.Mysql有哪些常见的引擎，区别是什么，使用场景
##### 25.session和cookie的联系以及区别，分布式session实现
##### 26.redis memcached比较
##### 27.Nginx负载均衡
##### 28.JVM内存模型及其常见调优
##### 29.GC算法
##### 30.分布式事务
##### 31.消息机制
##### 32.并发包java.util.concurrent下常见类及其与普通类区别
##### 33.zookeeper原理及其作用
##### 34.mysql表锁和行锁
##### 35.同步原理
##### 36.分布式同步锁
##### 37.APP请求加密及其合法性验证(涉及到非对称加密)
##### 38.sql语句
##### 39.常见问题
##### 40.Git
##### 41.附带一张2016年面试时的思维导图
##### 42.MyBatis最重要的类(???)以及如何与spring整合
##### 43.intellij idea技巧

1.加载顺序
![A](http://aragron.com/images/posts/A.png)
![B](http://aragron.com/images/posts/B.png)
![TestAB](http://aragron.com/images/posts/TestAB.png)

2.多线程

【1】
![worldhello](http://aragron.com/images/posts/worldhello.png)

【2】
![Demo_MultiThread](http://aragron.com/images/posts/Demo_MultiThread.png)
【2】- result1
![Demo_MultiThread_result1](http://aragron.com/images/posts/Demo_MultiThread_result1.png)
【2】- result2
![Demo_MultiThread_result2](http://aragron.com/images/posts/Demo_MultiThread_result2.png)
【2】- result3
![Demo_MultiThread_result3](http://aragron.com/images/posts/Demo_MultiThread_result3.png)
【2】- result4
![Demo_MultiThread_result4](http://aragron.com/images/posts/Demo_MultiThread_result4.png)

3.相等
![==](http://aragron.com/images/posts/==.png)

4.类型
![worldhello](http://aragron.com/images/posts/type.png)

5.trycatchfinally

【1】
![trycatchfinally1](http://aragron.com/images/posts/trycatchfinally1.png)
【2】
![trycatchfinally2](http://aragron.com/images/posts/trycatchfinally2.png)

6.String
![TestString](http://aragron.com/images/posts/TestString.png)

7.SpringMVC重定向
![redirect](http://aragron.com/images/posts/redirect.png)

8.ArrayList容量扩充
![ArrayListCapacity1](http://aragron.com/images/posts/ArrayListcapacity1.png)
![ArrayListCapacity2](http://aragron.com/images/posts/ArrayListcapacity2.png)

9.集合接口

【类结构图】
![Collection](http://aragron.com/images/posts/Collection.png)
![Collection_detail](http://aragron.com/images/posts/Collection_detail.png)
【ArrayListDemo】
![ArrayListDemo1](http://aragron.com/images/posts/ArrayListDemo1.png)
![ArrayListDemo](http://aragron.com/images/posts/ArrayListDemo.png)
![ArrayListDemo_result](http://aragron.com/images/posts/ArrayListDemo_result.png)
【LinkedListDemo】
![LinkedListDemo1](http://aragron.com/images/posts/LinkedListDemo1.png)
![LinkedListDemo](http://aragron.com/images/posts/LinkedListDemo.png)
【HashSetDemo】
![HashSetDemo](http://aragron.com/images/posts/HashSetDemo.png)
【LinkedHashSetDemo】
![LinkedHashSetDemo](http://aragron.com/images/posts/LinkedHashSetDemo.png)
【TreeSetDemo】
![TreeSetDemo](http://aragron.com/images/posts/TreeSetDemo.png)
【HashMapDemo】
【todo: HashMap的底层实现及不同JDK版本之间的区别】
![HashMapDemo1](http://aragron.com/images/posts/HashMapDemo1.png)
![HashMapDemo2](http://aragron.com/images/posts/HashMapDemo2.png)
【HashMap的底层数据结构】【jdk1.7】
![HashMapDemo3](http://aragron.com/images/posts/HashMapDemo3.png)
![HashMapDemo4](http://aragron.com/images/posts/HashMapDemo4.png)
【ConcurrentHashMap和Hashtable主要区别就是围绕着锁的粒度以及如何锁】
![HashMapDemo5](http://aragron.com/images/posts/HashMapDemo5.png)
![ConcurrentHashMap1](http://aragron.com/images/posts/ConcurrentHashMap1.png)

【LinkedHashMapDemo】
【todo: LinkedHashMap对存储的对象有什么要求】
![LinkedHashMapDemo](http://aragron.com/images/posts/LinkedHashMapDemo.png)
【TreeMapDemo】
【todo: TreeMap对key有什么要求, TreeMap对key的要求(TreeMap的key必须实现Comparable接口)】
![TreeMapDemo](http://aragron.com/images/posts/TreeMapDemo.png)

10.case 穿透
![case](http://aragron.com/images/posts/case.png)

11.Contructor
![duck](http://aragron.com/images/posts/duck.png)
![duck1](http://aragron.com/images/posts/duck1.png)

12.单例
![singleton_dcl](http://aragron.com/images/posts/singleton_dcl.png)

13.反射
![TestReflect](http://aragron.com/images/posts/TestReflect.png)

14.线程池
![Threadpool1](http://aragron.com/images/posts/Threadpool1.png)
![Threadpool2](http://aragron.com/images/posts/Threadpool2.png)
![Threadpool3](http://aragron.com/images/posts/Threadpool3.png)
![Threadpool4](http://aragron.com/images/posts/Threadpool4.png)

15.Redis
![redis1](http://aragron.com/images/posts/redis1.png)
![redis2](http://aragron.com/images/posts/redis2.png)
![redis3](http://aragron.com/images/posts/redis3.png)
![redis4](http://aragron.com/images/posts/redis4.png)
![redis5](http://aragron.com/images/posts/redis5.png)
![redis10](http://aragron.com/images/posts/redis10.png)
![redis6](http://aragron.com/images/posts/redis6.png)
![redis7](http://aragron.com/images/posts/redis7.png)
![redis8](http://aragron.com/images/posts/redis8.png)
![redis9](http://aragron.com/images/posts/redis9.png)

16.Dubbo
![dubbo1](http://aragron.com/images/posts/dubbo1.png)

17.Foreach
![for1](http://aragron.com/images/posts/for1.png)
![for2](http://aragron.com/images/posts/for2.png)
【片段1反编译结果】
![for3](http://aragron.com/images/posts/for3.png)

18.Spring

【IOC】
![ioc1](http://aragron.com/images/posts/ioc1.png)
![ioc2](http://aragron.com/images/posts/ioc2.png)
![ioc3](http://aragron.com/images/posts/ioc3.png)

【AOP】

【静态代理】
![proxy_static_1](http://aragron.com/images/posts/proxy_static_1.png)
![proxy_static_2](http://aragron.com/images/posts/proxy_static_2.png)
![proxy_static_3](http://aragron.com/images/posts/proxy_static_3.png)
![proxy_static_4](http://aragron.com/images/posts/proxy_static_4.png)
![proxy_static_5](http://aragron.com/images/posts/proxy_static_5.png)
![proxy_static_6](http://aragron.com/images/posts/proxy_static_6.png)
![proxy_static_7](http://aragron.com/images/posts/proxy_static_7.png)
![proxy_static_8](http://aragron.com/images/posts/proxy_static_8_1.png)
【动态代理】
![proxy_dynamic_1](http://aragron.com/images/posts/proxy_dynamic_1.png)
![proxy_dynamic_2](http://aragron.com/images/posts/proxy_dynamic_2.png)
![proxy_dynamic_3](http://aragron.com/images/posts/proxy_dynamic_3.png)
![proxy_dynamic_4](http://aragron.com/images/posts/proxy_dynamic_4.png)
![proxy_dynamic_5](http://aragron.com/images/posts/proxy_dynamic_5.png)
![proxy_dynamic_6](http://aragron.com/images/posts/proxy_dynamic_6.png)
![proxy_dynamic_7](http://aragron.com/images/posts/proxy_dynamic_7.png)
![proxy_dynamic_8](http://aragron.com/images/posts/proxy_dynamic_8.png)
![proxy_dynamic_9](http://aragron.com/images/posts/proxy_dynamic_9.png)
![proxy_dynamic_10](http://aragron.com/images/posts/proxy_dynamic_10.png)
【动态生成的TankTimeProxy.java】
![proxy_dynamic_12](http://aragron.com/images/posts/proxy_dynamic_12.png)
【编译后的TankTimeProxy.class】
![proxy_dynamic_11](http://aragron.com/images/posts/proxy_dynamic_11.png)
![proxy_dynamic_13](http://aragron.com/images/posts/proxy_dynamic_13_1.png)

19.web程序的启动顺序
![web1](http://aragron.com/images/posts/web1.png)
![web2](http://aragron.com/images/posts/web2.png)

20.生产消费者模式
21.ClassLoader双亲委派机制
22.volatile和synchronized的区别
![volatile_synchronized](http://aragron.com/images/posts/volatile_synchronized.png)
23.Myqsql常见优化
![mysql_optimize1](http://aragron.com/images/posts/mysql_optimize1.png)
24.Mysql有哪些常见的引擎，区别是什么，使用场景
![mysql_engine1](http://aragron.com/images/posts/mysql_engine1.png)
![mysql_engine2](http://aragron.com/images/posts/mysql_engine2.png)
25.session和cookie的联系以及区别，分布式session实现
![session_cookie](http://aragron.com/images/posts/session_cookie.png)
26.redis memcached比较
![redis_memcached1](http://aragron.com/images/posts/redis_memcached1.png)
27.Nginx负载均衡
![nginx1](http://aragron.com/images/posts/nginx1.png)
28.JVM内存模型及其常见调优
29.GC算法
30.分布式事务
![Transaction_Distributed](http://aragron.com/images/posts/Transaction_Distributed.png)
31.消息机制
![mq1](http://aragron.com/images/posts/mq1.png)
![mq2](http://aragron.com/images/posts/mq2.png)
![mq3](http://aragron.com/images/posts/mq3.png)
![mq4](http://aragron.com/images/posts/mq4.png)
![mq5](http://aragron.com/images/posts/mq5.png)
32.并发包java.util.concurrent下常见类及其与普通类区别
33.zookeeper原理及其作用
![zookeeper_dubbo1](http://aragron.com/images/posts/zookeeper_dubbo1.png)
34.mysql表锁和行锁
![mysql_lock1](http://aragron.com/images/posts/mysql_lock1.png)
![mysql_lock2](http://aragron.com/images/posts/mysql_lock2.png)
35.同步原理
36.分布式同步锁
37.APP请求加密及其合法性验证(涉及到非对称加密)
38.sql语句

39.常见问题
![frequently_ask_1](http://aragron.com/images/posts/frequently_ask_1.png)
![frequently_ask_2](http://aragron.com/images/posts/frequently_ask_2.png)
![frequently_ask_3](http://aragron.com/images/posts/frequently_ask_3.png)
![frequently_ask_4](http://aragron.com/images/posts/frequently_ask_4.png)

40.Git
![Git](http://aragron.com/images/posts/Git.png)

41.附带一张2016年面试时的思维导图
![interview_2016_MindNode](http://aragron.com/images/posts/interview_2016_MindNode.png)

42.MyBatis最重要的类(???)以及如何与spring整合

43.intellij idea技巧
![log_template1](http://aragron.com/images/posts/log_template1.png)
![log_template2](http://aragron.com/images/posts/log_template2.png)
![log_template3](http://aragron.com/images/posts/log_template3.png)
![class_header1](http://aragron.com/images/posts/class_header1.png)
![class_header2](http://aragron.com/images/posts/class_header2.png)


  




