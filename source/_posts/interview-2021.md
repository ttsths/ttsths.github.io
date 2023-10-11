---
cover: ""
category: ""
tags:
  - interview
status: 已发布
date: "2023-09-28 16:49:00"
catalog:
  - 面试
urlname: interview-2021
title: 21年初后端社招面试经历
summary: ""
sort: ""
updated: "2023-10-11 16:47:00"
---

- [**背景**](https://www.notion.so/samhalii/55559b9aa5d84e9b9fff82a01b581b51?v=cbbd193f3f054488b1b09b07f5770e13&p=506a13fb16d44473bd9130fc21fe1608&pm=s#%E8%83%8C%E6%99%AF)
- [**准备**](https://www.notion.so/samhalii/55559b9aa5d84e9b9fff82a01b581b51?v=cbbd193f3f054488b1b09b07f5770e13&p=506a13fb16d44473bd9130fc21fe1608&pm=s#%E5%87%86%E5%A4%87)
- [**面试汇总**](https://www.notion.so/samhalii/55559b9aa5d84e9b9fff82a01b581b51?v=cbbd193f3f054488b1b09b07f5770e13&p=506a13fb16d44473bd9130fc21fe1608&pm=s#%E9%9D%A2%E8%AF%95%E6%B1%87%E6%80%BB)
- [**总结**](https://www.notion.so/samhalii/55559b9aa5d84e9b9fff82a01b581b51?v=cbbd193f3f054488b1b09b07f5770e13&p=506a13fb16d44473bd9130fc21fe1608&pm=s#%E6%80%BB%E7%BB%93)

  ## **背景**

  双非本科，计科专业的五年弱鸡。base:SH，在老东家-EM，待了两年多。迫于上海从 20 年底的房价飞涨，思考对比之后决定回 HZ 发展，看看外面的机会。毕业这么多年还没有在大厂待过，所以进大厂一直是自己的一个目标。结合自身的情况，给自己制定了一份面试计划，大概分为以下阶段：

  - 知识体系总结回顾
  - 定位目标:个人在工程和架构上的优势？软技能方便的长处？想找什么样的工作去什么样的团队
  - 内推面试：感谢 v2 及帮我内推的大佬
  - 面试复盘

  ## **准备**

  知识体系总结其实是个日积月累的，但是我比较懒，之前都是零散的学习。没有很体系的记录和总结，所以在复习的时候也花了不少时间。有了知识体系之后给自己制定了一个复习计划-1 个月，但是计划赶不上变化-\_-||。大体方向上分为以下几个部分：

  - Java 基础&JUC&JVM
  - 过往项目经历
  - 中间件及系统设计
  - 操作系统&计算机网络
  - 算法

  ### **准备简历**

  简历我用的[**wondercv**](https://www.wondercv.com/)在线简历网站写的，用的免费的 Markdown 模板（非广告）。重要的是对自己简历上的东西要烂熟于心，熟练的技术栈，项目设计，为什么这么设计，项目的亮点、难点。

  ## **面试汇总**

  我总结了下出现比较频繁的面试题

  ### **Java 基础&JUC**

  - 面向对象的设计原则
  - HashMap 的数据结构和`put()`方法的过程
  - 强引用、软引用、弱引用、虚引用？
    - JDK 中哪些使用到了虚引用
  - ConcurrentHashMap 下 1.7 和 1.8 的区别
    - `put()`方法的插入过程
    - `get()`方法为什么不加锁也是线程安全的
  - 线程池的参数&任务执行过程-**【高频必问】**
    - 线程数如何设置？队列如何选择？
    - 线程处理任务时抛异常后线程池如何处理
    - `Tomcat`的默认线程池为什么是 200
  - `Synchronized`和`ReentrantLock`的原理及区别
    - AQS 的实现，扩展类
    - `Synchronized`锁优化
  - `volatile`的作用及原理
    - 内存屏障在编译和运行时如何使用
    - 总线风暴了解吗
  - `ThreadLocal`的原理、实际的使用场景
  - JDK 中常见的设计模式
  - JVMTI\JDPA

  ### **Java 虚拟机**

  - 内存模型
  - 类加载机制
    - 如何破坏双亲委派机制
      - Spi jdbc
      - 如何自定义加载器
    - new Object 的过程
  - 方法调用过程，栈是如何创建的
  - 常见的垃圾回收算法和垃圾回收器
    - CMS 和 G1 的使用和调优实践
  - 分代假说
  - 线上 OOM 排查思路
  - 内存泄漏

  ### **数据库**

  - MySQL 的索引结构以及使用
  - 事务的隔离级别和常见问题
    - 脏读与幻读的区别
    - 大事务如何处理？子事务之间如何保证一致性
  - 锁
    - next key lock ,gap 行锁，表锁
  - SQL 优化的过程
  - update 的执行过程（走索引&不走索引）
    - 普通索引
      - gap 锁 or next-key lock
    - 聚簇索引
    - 无索引
      - 表记录和间隙全部锁
  - MongoDB 的优劣

  ### **中间件**

  ### **Redis**

  - 单线程的 Redis 为什么快
  - 常见的数据结构及使用到的场景
  - IO 多路复用在 Redis 中是如何实现
  - 持久化机制有哪些，底层原理
  - 淘汰机制有哪些？
    - LRU 如何实现
  - 分布式锁的实现？锁过期？
    - Redison&RedLock
  - 哨兵模式和集群模式的区别？
    - Raft 算法的过程
    - 集群模式下节点的新增和移除过程
  - BigKey 和 HotKey 如何处理
  - 缓存一致性的解决方案
  - 高级的数据结构
    - bloomfilter

  ### **分库分表**

  - Sharding-JDBC 的执行过程
  - Sharding-JDBC 不支持的语法
  - 如何解决不走分片键的复制查询
  - 数据倾斜如何设计一个移动数据最少的方案

  ### **MQ**

  - 如何保证消息的可靠性
  - 如何保证消息的顺序性
  - 如何处理消息堆积
  - RocketMQ&Kafka&ActiveMQ 的区别
  - RocketMQ 是如何设计
    - 延迟消息如何设计
    - 死信队列
    - 消息重投
  - 生产者和消费者的负载均衡策略有哪些

  ### **框架**

  - Spring

    - IOC
      - Autowired 和 Resource 的区别
    - AOP

      Spring 如何实现一个自定义扩展点

      - cglib
      - Jdk 动态代理
      - 实例化之前 AutoConfigruation BeanPostProcessor；实例化之后，判断是要需要增强，增强的话需要设置代理

    - 如何解决循环依赖
      - 三级缓存，最后一集缓存的 factoryBean 先实例化，在初始化
    - 事务如何实现，如何开启和关闭，传播机制
      - 传播机制的实现：安全点
    - SpringMVC 响应请求的步骤
    - Controller 是线程安全的吗

  ### **分布式**

  - SpringBoot 的配置装配
  - Hystrix 实现的原理
    - 如何实现一个滑动窗口
  - Apollo 的配置热部署如何实现
  - Eureka 是如何在高并发下的可靠性
    - 自我保护机制的原理
    - CAP
  - SkyWalking 如何实现链路追踪
    - 如何实现日志追踪
      - 服务调用传递
      - 父子线程的传递
      - 线程池之间的传递

  ### **系统设计**

  - 100 个日志文件（10M~1000G 之间）找出指定日期的日志并排序
  - 卡券系统设计
  - 秒杀系统的设计
  - 12306 抢票设计
  - 大数据量的评论系统如何设计
  - 红包雨设计--总共发 1 亿，假设 1000w，每个人最多拿 15 块，不能超卖，点点点，是有概率的，汇总
    - Redis 主从，主节点宕机

  ### **计算机网络**

  - TCP 和 UDP 有什么区别?

    UDP 流媒体应用

    - 拥塞控制、滑动窗口
      - 2msl
    - 怎么实现 UDP 实现可靠传输

  - TCP 的粘包问题如何解决
  - IO 模型，IO 多路复用的差异
  - http 和 resultFul 接口的区别 rpc 的区别
    - resultFul 是一种规范
    - rpc 有自己的序列化，协议，响应快

  ### **算法**

  - 数据结构
  - [**有序数组排序-LeetCode88**](https://leetcode-cn.com/problems/merge-sorted-array/)
  - [**无重复字符的最长子串-LeetCode-3**](https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/)
  - [**排序链表-LeetCode148**](https://leetcode-cn.com/problems/sort-list/)
  - [**翻转字符串里的单词**](https://leetcode-cn.com/problems/reverse-words-in-a-string/)
  - [**较小的三数之和-LeetCode259**](https://leetcode-cn.com/problems/3sum-smaller/)
  - 二叉树后续遍历

  ### **软技能**

  - 你的优点和缺点
    - 举例说明优点
  - 过往经历给你带来影响最深的成长是什么
  - 未来 3 年的职业规划

  ## **总结**

  面了近 20 家公司，有好多不尽人意的地方，最后能够拿到 offer 还是很幸运的。补充一些小结：

  - 简历里的项目一定要好好准备
  - 如果想进大厂，算法还是要好好刷一刷

    - 《[**编程珠玑**](https://book.douban.com/subject/3227098/)》
    - 《[**剑指 offer**](https://book.douban.com/subject/27008702/)》
    - [**CodeTop**](https://codetop.cc/#/home)
    - 平时一定要多思考和总结，不积跬步无以至千里

    到这里就全写完了, 你可以直接通过我的邮箱留言交流, 感谢您耐心地看完全文!
