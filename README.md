# springboot-
SpringBoot之定时任务详解

1.概要说明

  该项目是根据数据库的定时生命周期来定时执行任务。
  数据库备份


2.结构说明

  根据数据库中的定时周期来动态执行任务，动态的定时任务类：com.mmzs.springboot.springbootschedule.controller.DynamicScheduleTask
  静态定时任务类：com.mmzs.springboot.springbootschedule.controller.SaticScheduleTask
  多任务的定时任务类：com.mmzs.springboot.springbootschedule.controller.MultithreadScheduleTask
  备份数据库控制类：com.mmzs.springboot.springbootschedule.controller.MySqlBackupController
 
3.部分参数配置说明

spring.application.name=bakcup
#定时备份的数据库配置
mango.backup.datasource.host= 备份的MySQL的IP地址
mango.backup.datasource.userName= MySQL的连接用户名
mango.backup.datasource.password= MySQL的连接密码
mango.backup.datasource.database= 备份的数据库
spring.datasource.driverClassName=com.mysql.jdbc.Driver
#如果是高版本的MySQL，需要配置成如下，不然会报版本不兼容的问题
spring.datasource.url=jdbc:mysql://localhost:3306/socks?useUnicode=true&useJDBCCompliantTimezoneShift=true&useLegacyDatetimeCode=false&serverTimezone=UTC
spring.datasource.username= .....
spring.datasource.password=....

4.需要的软件环境

  mysql数据库版本:ySQL5.7.27；
  Java环境：jdk1.8_231；
  开发工具：idea ；
  开发语言框架：spring boot2.2版本；
