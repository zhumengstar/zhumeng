@[TOC](面试题集合)
# 计算机网络
1. TCP三次握手四次挥手?
* 连接服务器指定端口，建立TCP连接,并同步连接双方的序列号和确认号并交换 TCP 窗口大小信息.在socket编程中，客户端执行connect()时。将触发三次握手。
2. 为什么建立连接协议是三次握手，而关闭连接却是四次握手呢？
* 服务器LISTEN状态收到SYN，可以将ACK和SYN放在同一个报文里发送给客户端
* 但关闭连接时，当收到对方的FIN报文通知时，它仅仅表示对方没有数据发送给你了；但未必你所有的数据都全部发送给对方了，所以你可能未必会马上会关闭SOCKET,可能还需要发送一些数据给对方之后，再发送FIN报文给对方来表示你同意现在可以关闭连接
3. 在浏览器上发生Web请求过程![在这里插入图片描述](https://img-blog.csdnimg.cn/20190315153128541.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjEzMzk0MA==,size_16,color_FFFFFF,t_70)
4. OSI七层模型（物理层，数据链路层，网络层，传输层，表示层，会话层，应用层）
5. 在Web浏览器发送请求有涉及哪些协议
6.  TCP和UDP的区别
7. TCP UDP HTTP分别是在哪一层的
8. 把UDP变成TCP怎样实现
9. TCP/IP四层模型，各模型作用，主要协议及其功能
10. 子网掩码，C类IP地址最多可有多少个，网关
11. http的状态码 ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190315153212694.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjEzMzk0MA==,size_16,color_FFFFFF,t_70)
12. HTTP的GET和POST的区别
13. HTTP长连接短连接
14. http的报文格式
15. HTTP 和 HTTPS 有什么区别
## Socket编程
 1. Socket编程中高并发
 2. BIO和NIO  Socket的模式 
# 操作系统
1. 进程的几种状态
2. 进程和线程有什么区别
3. sleep和wait区别
4. 如何终止一个进程
5. 进程为啥阻塞
6. 内核态，用户态
# Java语言
## 数据结构
1. 用两个队列实现栈
## Java基础
1. 讲一下 Java 的反射机制
2. 重载和重写分别是什么
3. StringBuilder和StringBuffer区别
4. io多路复用
5. io的同步异步
6. Object类
7. equals和hashCode
8. 重写和重载
9. volatile
10. Java反射机制 
11. 类加载器的双亲委派机制是怎样的一个过程，String 类是哪个类加载器加载的
12. ==和 equals 方法的区别
13. 序列化和反序列化的过程分别是怎样的
14. 阻塞 IO 模型和非阻塞 IO 模型
15. 缓冲区溢出是一种怎样的现象
## 集合
1. 了解集合类吗，说说 HashSet 怎么实现的--->equals 不同会怎样，相同会怎样(--->怎么解决哈希冲突--->开放定址法是啥
2. HashMap和CurrentHashMap的区别
3. hashMap,hashtable
4. ArrayList 和 LinkedList 的区别
5. HashMap 的 put 方法的实现步骤，扩容解决了什么问题，为什么扩容 2 倍
6. HashMap 在高并发情况下会发生死循环的情况，了解吗?如果并发下要用 Map，要 用怎样的 Map，为什么 ConcurrentHashMap 同步性能好
## 多线程
1. Java中的线程池
2. 创建线程的几种方式
3. 守护线程的特点
4. 线程池的基本原理
5. 如何保证线程安全性？原理是什么
6. 如何避免多线程的并发
7. 了解多线程吗，说说 synchronized--->修饰方法和修饰代码块有什么区别--->还有哪些线 程同步的方式(volitail)--->还有呢，知道 Lock 吗？
8. 用过 Java 线程池吗，创建线程池的参数，添加任务的话线程数量怎么变化的说说过程
## Spring框架
1. SpringMVC模型
2. Controller是如何被调用的，通过浏览器访问的过程
3. Spring MVC的设计
4. AOP IOC
5. spring bean的基本原理
6. 怎么配置spring
7. Tomcat的原理，如何处理并发问题
8. @Qualifier 和@Autowired 这两个注 解是干嘛用的--->说说@Autowired 是怎么实现的--->当我用了@Autowired，它是怎么去查 找我需要的类(有默认 id)--->默认 id 是什么--->指定的 id 和默认 id 有冲突怎么办
9. 单元测试和写一个 main 函数调方法有什么区别
10. Spring、SpringMVC、SpringBoot 的区别 
11. 说说 SpringMVC 的执行流程
12. 对于页面返回 html 和返回 JSON，分别是怎么配置
13. MyBatis 和 JDBC 比起来，有哪些好处
14. MyBatis 中#{...}和${...}的区别
15. 
## JVM虚拟机
1. JVM的存储模型
2. 系统堆和栈的区别
## 锁
1. synchronized怎样使用
2. 对象锁 类锁
# 数据库
1. Mysql底层存储模型（B+树）
2. @Transactional原理
3. Mysql中最终插入到磁盘出错，如何解决错误
4. 主键约束和唯一约束  唯一索引
5. 数据库事务特性
6. 设计数据库的思路
7. 数据库存储引擎
8. 怎么保证 redis 和 rabbitmq 这 两个操作的原子性
9. 事务的隔离级别有哪几种--->解决了哪些问题(脏读、不可重复读、幻读)--->脏读是什 么--->幻读是什么
10. 索引的缺点 
11. MySQL 字段的数据类型有哪些--->varchar 和 text 有什么区别--->int 几个字节-->tinyint 几个字节--->int(4)括号里面的 4 指的是什么
12. SQL 注入会带来什么样的后果，造成这样后果的本质原因是什么，能通过 SQL 注入将 整张表的数据删掉吗
13. 数据库左连接，内连接，有连接
14. 怎么取得两个表的不同数据的行
# 设计模式
1. Filter中的设计模式（过滤器模式）
2. 讲一下代理模式--->还知道其他的设计模式吗
# 分布式
# 并发问题
1. 你认为在高并发情况下会出现什么问题
# 设计题
1. 10G大小的文件要由服务器同时下发到300个客户端上, 如何高效率地下发? (不考虑P2P的模式)
2. 将一个程序部署到服务器上, 要求这个程序只能启动一次, 如何保证?
3. 2000万的数据, 其中有100万热点数据, 设计做一个缓存(先不考虑redis)?
4.  一个小时内, 一个用户只能登录5次, 超出5次之后就不能让他再登录, 如何处理?
5.  如果一个用户在10分钟之内发送100条消息， 则不让他发送， 那么如何判断这个问题
6. 在终端排查java程序加载过慢的原因
7. 海量问题---url去重
8. n个有序数组， 每个数组都有m个元素， 求出这n个有序数组的归并
9. 项目数据量特别大，数据库查找慢，你会考虑从哪几方面进行优化
