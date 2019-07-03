### spring:

​	概述：EE开发的   *[**一站式**]()*   框架

​			一站式框架 ：有EE开发的每一层的解决方案。

​					WEB层 ：SpringMVC

​					Service :  Spring的bean管理，Spring声明式事务

​					DAO层（持久层）： Spring 的 JDBC 模板，Spring的 ORM 



![1561784995857](C:\Users\Administrator\AppData\Local\Temp\1561784995857.png)

​	

### IOC:(Inversion of Control 控制反转)

​	![1561785168886](C:\Users\Administrator\AppData\Local\Temp\1561785168886.png)



### Spring底层的IOC的实现原理：

​		工厂+反射+配置文件  --》实现程序解耦合

*< bean id="UserDAO" class="xxx.UserDAOImpl"></bean>

class BeanFactory{

​	public static Object getBean(String id){

​		//解析XML

​		//反射

​		Class clazz=Class.forName();

​		return clazz.newInstance();

​	}

}



### DI(依赖注入)：

​	前提必须有IOC的环境，spring管理这个类的时候将类的依赖的属性注入（设置）进来。

#### 面向对象：

##### 	依赖：

​	class A{

}

​	class B{

​		public void xxx(A a){		//B依赖了A

​		}

}

##### 	继承: is a

​	class A{

}

​	class B extends A{

}

##### 	聚合: has a

​	

### bean:

​	标签：

​		id	：使用了约束中的唯一约束，里面不能出现特殊字符的。

​		name：没有使用约束中的唯一约束（理论上可以出现重复的，但实际开发并不能出现的）。可以出现特殊字段

​		class：对应的是要生成实例的类的全路径

​		

#### 作用范围的配置：（重点）

- [ ] ​	**scope**	：Bean的作用范围

​		***`singleton`**	：默认：Spring会用单列模式创建这个对象。*

​		***`prototype`**	：多例模式。*

​		**`request`**		：应用在web项目中，Spring创建这个类以后，将这个类存入到request范围中。

​		**`session`**		：应用在web项目中，Spring创建这个类以后，将这个类存入到session范围中。

​		**`globalsession`** ：应用在web项目中，必须在prolet环境下使用。但是如果没有这种环境，相对于session。



