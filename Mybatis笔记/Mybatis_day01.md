## Mybatis:（类似于hibernate的持久层框架）

​		概述：持久层框架

​		MyBatis 是一款优秀的持久层框架，它支持定制化 SQL、存储过程以及高级映射。MyBatis 避免了几乎所有的 JDBC 代码和手动设置参数以及获取结果集。MyBatis 可以使用简单的 XML 或注解来配置和映射原生信息，将接口和 Java 的 POJOs(Plain Ordinary Java Object,普通的 Java对象)映射成数据库中的记录。 



每个MyBatis应用程序主要都是使用Sql[Session](https://baike.baidu.com/item/Session)Factory实例的，一个SqlSessionFactory实例可以通过SqlSessionFactoryBuilder获得。SqlSessionFactoryBuilder可以从一个xml配置文件或者一个预定义的配置类的实例获得。

用xml文件构建SqlSessionFactory实例是非常简单的事情。推荐在这个配置中使用类路径资源（classpath resource)，但你可以使用任何Reader实例，包括用文件路径或file://开头的url创建的实例。MyBatis有一个实用类----Resources，它有很多方法，可以方便地从类路径及其它位置加载资源。



## 持久层框架

编辑

[Hibernate](https://baike.baidu.com/item/Hibernate)

Hibernate [1]  是一个[开放源代码](https://baike.baidu.com/item/%E5%BC%80%E6%94%BE%E6%BA%90%E4%BB%A3%E7%A0%81)的[对象关系映射](https://baike.baidu.com/item/%E5%AF%B9%E8%B1%A1%E5%85%B3%E7%B3%BB%E6%98%A0%E5%B0%84)框架，它对JDBC进行了非常轻量级的对象封装，使得Java程序员可以随心所欲的使用对象编程思维来操纵数据库。 Hibernate可以应用在任何使用JDBC的场合，既可以在Java的客户端程序使用，也可以在Servlet/JSP的Web应用中使用，最具革命意义的是，Hibernate可以在应用EJB的J2EE架构中取代CMP，完成[数据持久化](https://baike.baidu.com/item/%E6%95%B0%E6%8D%AE%E6%8C%81%E4%B9%85%E5%8C%96)的重任。[Eclipse](https://baike.baidu.com/item/Eclipse)平台下的Hibernate辅助开发工具:【**Hibernate Synchronizer**】【**MiddlegenIDE**】

[MyBatis](https://baike.baidu.com/item/MyBatis)

使用MyBatis 提供的ORM机制，对业务逻辑实现人员而言，面对的是纯粹的Java对象， 这一层与通过Hibernate 实现ORM 而言基本一致，而对于具体的数据操作，Hibernate 会自动生成SQL 语句，而MyBatis则要求开发者编写具体的SQL 语句。相对Hibernate等 “[全自动](https://baike.baidu.com/item/%E5%85%A8%E8%87%AA%E5%8A%A8)”ORM机制而言，MyBatis 以SQL开发的工作量和数据库移植性上的让步，为系统 设计提供了更大的自由空间。作为“全自动”ORM 实现的一种有益补充，MyBatis 的出现显 得别具意义。

- 