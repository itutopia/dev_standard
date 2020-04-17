## 系统机构技术选型


    监控平台
    1、cat：CAT基于Java开发的实时应用监控平台，包括实时应用监控，业务监控。
     https://github.com/dianping/cat 点评网
     
    2、Open-Falcon：http://open-falcon.org/    小米 (非java）
    人性化的互联网企业级监控系统 * 数据采集免配置：agent自发现、支持Plugin、主动推送模式
    * 容量水平扩展：生产环境每秒50万次数据收集、告警、存储、绘图，可持续水平扩展。
    * 告警策略自发现：Web界面、支持策略模板、模板继承和覆盖、多种告警方式、支持回调动作。
    * 告警设置人性化：支持最大告警次数、告警级别设置、告警恢复通知、告警暂停、不同时段不同阈值、支持维护周期，支持告警合并。
    * 历史数据高效查询：秒级返回上百个指标一年的历史数据。
    * Dashboard人性化：多维度的数据展示，用户自定义Dashboard等功能。
    * 架构设计高可用：整个系统无核心单点，易运维，易部署。
 
    RPC框架
     1、 pigeon : https://github.com/dianping/pigeon     点评网
     2、 dubbo：http://dubbo.io/           阿里
     3、 dubbox：https://github.com/dangdangdotcom/dubbox   当当网
    支持REST风格远程调用（HTTP + JSON/XML)
    支持基于Kryo和FST的Java高效序列化实现
    支持基于Jackson的JSON序列化
    支持基于嵌入式Tomcat的HTTP remoting体系
    升级Spring
    升级ZooKeeper客户端
    支持完全基于Java代码的Dubbo配置
    调整Demo应用
    修正了dubbo的bug 包括配置、序列化、管理界面等等的bug
        

    4、motan: github.com/weibocom/motan    新浪微博
    概述
    Motan 是一套高性能、易于使用的分布式远程服务调用(RPC)框架。
    功能
    支持通过spring配置方式集成，无需额外编写代码即可为服务提供分布式调用能力。
    支持集成consul、zookeeper等配置服务组件，提供集群环境的服务发现及治理能力。
    支持动态自定义负载均衡、跨机房流量调整等高级服务调度能力。
    基于高并发、高负载场景进行优化，保障生产环境下RPC服务高可用。
         
    5、harpc ：https://github.com/baifendian/harpc    百分点
     基于Thrift的跨语言、高可用、高性能、轻量级的RPC框架。
     功能介绍
     跨语言通信
     方便的使Java、Python、C++三种程序可以相互通信
     负载均衡和容灾处理
     方便的实现任务的分布式处理
     支持服务的水平扩展，自动发现新的服务节点
     能够兼容各种异常情况，如节点的异常down机
     可视化管理
     通过服务管理系统可以方便查看服务状态和统计信息
     与原生thrift通信
     支持与原生thrift服务进行通信


    分布式统一框架
     1、 Albianj2：https://github.com/crosg/Albianj2    阅文集团
    Albianj是我们设计并开发的一套分布式统一框架。他主要是面向海量数据处理、海量数据 访 问、并解决互联网开发中经常会碰到的数据海量增长问题，也一并解决 互联网开发团队 中，因开发人员的水平参差不齐而导致的代码质量不可控问题。它主要有简单小巧的IoC， ORM，数据路由，缓存集成，分布式唯一id等等功能
     1. 一个简单的Service服务，比spring轻量很多很多 
     2. 一个简单的ORM框架 
     3. 数据路由服务 
     4. 分布式事务服务（支持强、弱两种模型） 
     5. 简单的缓存服务 
     6. 统一的Id服务 
     7. 日志服务（这部分有待扩展） 
     8. 密码安全服务 
     9. 简单的restful服务 
     10. 一个轻量级的配置服务 
     
    数据库访问层中间件：
     1、zebra：https://github.com/dianping/zebra     点评网
        1. 配置集中管理，动态刷新
        2. 支持读写分离、分库分表
        3. 丰富的监控信息在CAT上展现
    
     2、mango：https://github.com/jfaster/mango/     乐视
        1、超高性能，响应速度接近直接使用JDBC
        2、采用接口与注解的形式定义DAO，完美结合db与cache操作
        3、支持动态sql，可以构造任意复杂的sql语句
        4、支持多数据源，分表，分库，事务
        5、内嵌“函数式调用”功能，能将任意复杂的对象，映射到数据库的表中
        6、高效详细的实时统计系统，方便开发者随时了解自己的系统
        7、独立jar包，不依赖其它jar包
        8、提供便捷的spring插件，与spring无缝集成

    3、Mycat：http://www.mycat.org.cn/
        国内最活跃的、性能最好的开源数据库中间件
        关键特性
        支持SQL92标准
        支持MySQL、Oracle、DB2、SQL Server、PostgreSQL等DB的常见SQL语法
        遵守Mysql原生协议，跨语言，跨平台，跨数据库的通用中间件代理。
        基于心跳的自动故障切换，支持读写分离，支持MySQL主从，以及galera cluster集群。
        支持Galera for MySQL集群，Percona Cluster或者MariaDB cluster
        基于Nio实现，有效管理线程，解决高并发问题。
        支持数据的多片自动路由与聚合，支持sum,count,max等常用的聚合函数,支持跨库分页。
        支持单库内部任意join，支持跨库2表join，甚至基于caltlet的多表join。
        支持通过全局表，ER关系的分片策略，实现了高效的多表join查询。
        支持多租户方案。
        支持分布式事务（弱xa）。
        支持XA分布式事务（1.6.5）。
        支持全局序列号，解决分布式下的主键生成问题。
        分片规则丰富，插件化开发，易于扩展。
        强大的web，命令行监控。
        支持前端作为MySQL通用代理，后端JDBC方式支持Oracle、DB2、SQL Server 、 mongodb 、巨杉。
        支持密码加密
        支持服务降级
        支持IP白名单
        支持SQL黑名单、sql注入攻击拦截
        支持prepare预编译指令（1.6）
        支持非堆内存(Direct Memory)聚合计算（1.6）
        支持PostgreSQL的native协议（1.6）
        支持mysql和oracle存储过程，out参数、多结果集返回（1.6）
        支持zookeeper协调主从切换、zk序列、配置zk化（1.6）
        支持库内分表（1.6）
        集群基于ZooKeeper管理，在线升级，扩容，智能优化，大数据处理（2.0开发版）。
                
                
         4、Cobar
         Cobar是阿里巴巴开源(官方github)的一个对应用保持透明的MySQL数据库分布式处理中间件。
         Cobar功能
             将一张表拆分到不同的库。
             将不同的表放入不同的库。
             提供HA方案
             Cobar约束
             不支持跨库情况下的 join、分页、排序、子查询操作
             SET 语句执行会被忽略，事务和字符集设置除外 
             分库情况下，insert 语句必须包含拆分字段列名 
             分库情况下，update 语句不能更新拆分字段的值 
             不支持 SAVEPOINT 操作 
             暂时只支持 MySQL 数据节点
         
    软负载：
        1、camel
            https://github.com/dianping/camel    点评网
            是大众点评开发的软负载一体解决方案，承担了F5硬负载层后的软负载工作。
            Camel已成为大众点评网络流量中必不可缺的一层
 
    分布式存储:
        1、FastDFS 
            https://github.com/happyfish100/fastdfs
            开源的轻量级分布式文件系统，对文件进行管理，功能包括：文件存储、文件同步、文件访问（文件上传、文件下载）等，解决了大容量存储和负载均衡的问题。特别适合以文件为载体的在线服务，如相册网站、视频网站等等。
            FastDFS服务端有两个角色：跟踪器（tracker）和存储节点（storage）。跟踪器主要做调度工作，在访问上起负载均衡的作用。
            存储节点存储文件，完成文件管理的所有功能：存储、同步和提供存取接口，FastDFS同时对文件的meta data进行管理。所谓文件的meta data就是文件的相关属性，以键值对（key value pair）方式表示，如：width=1024，其中的key为width，value为1024。文件meta data是文件属性列表，可以包含多个键值对
        
        2、zimg
            http://blog.buaa.us/zimg-v2-release/
            一个图片存储程序，主要的优点是可以根据请求实时处理图片，并且进行压缩和存储，
            一是方便前端用户，二来降低流量。zimg设计之初就是面向中小型应用，是存储量小于
            TB级别的单机存储方案。它的1.0版本主要竞争对手是基于Nginx+PHP的图片服务器，
            因为采用了特殊的策略，zimg会比PHP快出很多
 
    分布式缓存：
        1、redis：
            https://redis.io/
            Redis是一个开源（BSD许可），内存存储的数据结构服务器，可用作数据库，高速缓存和消息队列代理。它支持字符串、哈希表、列表、集合、有序集合，位图，hyperloglogs等数据类型。内置复制、Lua脚本、LRU收回、事务以及不同级别磁盘持久化功能，同时通过Redis Sentinel提供高可用，通过Redis Cluster提供自动分区，可通过一致hash实现分布式存储
        
        2、ignite：
            http://ignite.apache.org/
            Apache Ignite内存数据架构是一种高性能，集成和分布式的内存平台，用于实时计算和处理大规模数据集，比使用传统基于磁盘或闪存技术的可能性快几个数量级
        3.coherence
            付费：http://www.oracle.com/technetwork/middleware/coherence/overview/index.html
            Oracle Coherence是行业领先的内存数据网格解决方案，通过提供对常用数据的快速访问，组织可以可预测地扩展关键任务应用程序。 随着数据量和客户期望的增加，由“物联网”，社交，移动，云和永远连接的设备驱动，因此需要实时处理更多的数据，卸载超负荷的共享数据服务，并提供 可用性保证。无须集群就可以操作多节点共享内存，多几节点聚合计算能力
         
    性能分析工具：
         1、 TProfiler：https://github.com/alibaba/TProfiler    阿里
          TProfiler是一个可以在生产环境长期使用的性能分析工具.它同时支持剖析和采样两种方式,记录方法执行的时间和次数,生成方法热点 对象创建热点 线程状态分析等数据,为查找系统性能瓶颈提供数据支持.
          TProfiler在JVM启动时把时间采集程序注入到字节码中,整个过程无需修改应用源码.运行时会把数据写到日志文件,一般情况下每小时输出的日志小于50M.
          业界同类开源产品都不是针对大型Web应用设计的,对性能消耗较大不能长期使用,TProfiler解决了这个问题.目前TProfiler已应用于淘宝的核心Java前端系统.
          部署后低峰期对应用响应时间影响20% 高峰期对吞吐量大约有30%的降低(高峰期可以远程关闭此工具).
     
    数据库连接池：
         1、druid：https://github.com/alibaba/druid   阿里
     
    消息中间件mq：
         1、ActiveMq：
           ActiveMQ 是Apache出品，最流行的，能力强劲的开源消息总线。ActiveMQ 是一个完全支持JMS1.1和J2EE 1.4规范的 JMS Provider实现，尽管JMS规范出台已经是很久的事情了，但是JMS在当今的J2EE应用中间仍然扮演着特殊的地位
         
         2、RocketMQ：https://github.com/alibaba/RocketMQ    阿里
           1、RocketMQ 是一款分布式、队列模型的消息中间件，具有以下特点：
           2、能够保证严格的消息顺序
           3、提供丰富的消息拉取模式
           4、高效的订阅者水平扩展能力
           5、实时的消息订阅机制
           6、亿级消息堆积能力
           7、Metaq3.0 版本改名，产品名称改为RocketMQ
         
         3、Kafka：http://kafka.apache.org/
           Kafka是一种高吞吐量的分布式发布订阅消息系统，它可以处理消费者规模的网站中的所有动作流数据。 这种动作（网页浏览，搜索和其他用户的行动）是在现代网络上的许多社会功能的一个关键因素。 这些数据通常是由于吞吐量的要求而通过处理日志和日志聚合来解决。 对于像Hadoop的一样的日志数据和离线分析系统，但又要求实时处理的限制，这是一个可行的解决方案。Kafka的目的是通过Hadoop的并行加载机制来统一线上和离线的消息处理，也是为了通过集群来提供实时的消费
     
         4、RabbitMq：http://www.rabbitmq.com/
            应用程序的健壮消息传递
            易于使用
            在所有主要操作系统上运行
            支持大量的开发者平台
            开源和商业支持
     
    
    序列化：
        1、fastjson：https://github.com/alibaba/fastjson   阿里
            fastjson 是一个性能很好的 Java 语言实现的 JSON 解析器和生成器。
            主要特点：
            快速FAST (比其它任何基于Java的解析器和生成器更快，包括jackson）
            强大（支持普通JDK类包括任意Java Bean Class、Collection、Map、Date或enum）
            零依赖（没有依赖其它任何类库除了JDK）
         
        2、Jackson：https://github.com/FasterXML/jackson/    
            Jackson 是一个 Java 用来处理 JSON 格式数据的类库，性能非常好
         
        3、gson：https://github.com/google/gson    google
            提供简单的tojson()和fromjson()方法将java对象的JSON
            允许存在不可修改的对象被转换为从JSON
            java泛型的广泛支持
            允许对象的自定义表示
            支持任意复杂对象（具有深层继承层次和泛型类型的广泛使用）
        
        4、kryo：
            诸如Hessian和GPB这些三方的序列化框架或多或少的都对Java原生序列化机制做出了一些改进；而对于Kryo来说，改进无疑是更彻底一些；在很多评测中，Kryo的数据都是遥遥领先的；
            Kryo的处理和Google Protobuf类似。但有一点需要说明的是，Kryo在做序列化时，也没有记录属性的名称，而是给每个属性分配了一个id，但是他却并没有GPB那样通过一个schema文件去做id和属性的一个映射描述，所以一旦我们修改了对象的属性信息，比如说新增了一个字段，那么Kryo进行反序列化时就可能发生属性值错乱甚至是反序列化失败的情况；而且由于Kryo没有序列化属性名称的描述信息，所以序列化/反序列化之前，需要先将要处理的类在Kryo中进行注册，这一操作在首次序列化时也会消耗一定的性能。
            另外需要提一下的就是目前kryo目前还只支持Java语言。
     
    分布式协调服务（可作为配置中心服务）：
         
         1、zookeeper：http://zookeeper.apache.org/
            ZooKeeper是以Fast Paxos算法为基础的，Paxos 算法存在活锁的问题，即当有多个proposer交错提交时，有可能互相排斥导致没有一个proposer能提交成功，而Fast Paxos作了一些优化，通过选举产生一个leader (领导者)，只有leader才能提交proposer，具体算法可见Fast Paxos。因此，要想弄懂ZooKeeper首先得对Fast Paxos有所了解。
            ZooKeeper的基本运转流程：
                1、选举Leader。
                2、同步数据。
                3、选举Leader过程中算法有很多，但要达到的选举标准是一致的。
                4、Leader要具有最高的zxid。
                5、集群中大多数的机器得到响应并follow选出的Leader。
    
    前端选型：
        1、bootstrap：http://getbootstrap.com/
            Bootstrap，来自 Twitter，是目前很受欢迎的前端框架。Bootstrap 是基于 HTML、CSS、JAVASCRIPT 的，它简洁灵活，使得 Web 开发更加快捷。它由Twitter的设计师Mark Otto和Jacob Thornton合作开发，是一个CSS/HTML框架
         
        2、vue：http://vuejs.org/
            vue是一套构建用户界面的 渐进式框架。与其他重量级框架不同的是，Vue 采用自底向上增量开发的设计。Vue 的核心库只关注视图层，并且非常容易学习，非常容易与其它库或已有项目整合。另一方面，Vue 完全有能力驱动采用单文件组件和 Vue 生态系统支持的库开发的复杂单页应用。
            Vue.js 的目标是通过尽可能简单的 API 实现响应的数据绑定和组合的视图组件
     
        3、React：http://reactjs.cn/react/index.html
         
        4、AngularJS：https://angularjs.org/
            核心的是：MVC、模块化、自动化双向数据绑定、语义化标签、依赖注入等等。
         
        5、ztree：http://www.treejs.cn/v3/main.php#_zTreeInfo
         
        6、weex：https://weex-project.io/index.html     阿里跨平台前端
       
        7、easyui：http://www.jeasyui.com
            easyui是一种基于jQuery的用户界面插件集合。
            easyui为创建现代化，互动，JavaScript应用程序，提供必要的功能。
            使用easyui你不需要写很多代码，你只需要通过编写一些简单HTML标记，就可以定义用户界面。
            easyui是个完美支持HTML5网页的完整框架。
            easyui节省您网页开发的时间和规模。
            easyui很简单但功能强大的。
    
        8、amaze：http://amazeui.org/     
            国产开源 HTML5 跨屏前端框架
    
    微服务
        1、springboot
        2、MSF4J： 
    

    目前系统采用
    1、后端
        服务框架：Dubbo、zookeeper
        缓存：Redis、ehcache
        消息中间件：ActiveMQ，kafka
        负载均衡：Nginx
        分布式文件：FastDFS
        数据库连接池： c3p0
        核心框架：Spring framework
        安全框架：Apache Shiro 1.2
        视图框架：Spring MVC 4.0
        服务端验证：Hibernate Validator 5.1
        工作流引擎：Activiti 5.15
        任务调度：quartz 1.8.5
        持久层框架：MyBatis 3.2
        日志管理：SLF4J 1.7、Log4j
        工具类：Apache Commons、Jackson 2.2、
        服务器中间件：Tomcat 7、Jetty
        数据库支持：mysql数据库的支持
