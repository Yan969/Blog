## 自动配置原理
Spring Boot关于自动配置的源码在spring-boot-autoconfigure-x.x.x.x.jar中.

@EnableAutoConfiguration
这个@EnableAutoConfiguration注解通过@SpringBootApplication被间接的标记在了Spring Boot的启动类上。在SpringApplication.run(...)的内部就会执行selectImports()方法，找到所有JavaConfig自动配置类的全限定名对应的class，然后将所有自动配置类加载到Spring容器中。


[转载自：https://blog.csdn.net/u014745069/article/details/83820511](https://blog.csdn.net/u014745069/article/details/83820511
