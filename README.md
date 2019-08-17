# StudentManagementSystem
SpringBoot+Layui搭建的学生管理系统，加入了shiro安全框架和Ehcache缓存框架

  最近新学习了前端框架Layui、安全框架Shiro、缓存框架Ehcache的基本用法，边学习边练习，写了这个学生管理系统。

      
  ### 介绍
   该系统相对于以前的练手项目，最主要就是新增了shiro权限。我在菜单栏用了shiro标签对菜单进行控制，根据登录用户的不同，显示不同的菜单和操作按钮。
新接触的Layui的表单可以说是非常实用了，但是我用ehcache缓存对list集合进行缓存时，layui的表格分页功能就会失效（比如我查询学生列表，并且对这个list添加了缓存，那么在前端展示时，layui的分页功能就会失效，转而显示所有的学生），目前还没有找到解决办法，所以在项目中就没有对list查询进行缓存。


  基本的环境：
  * Spring+SpringMVC+Mybatis
  * 前端：Layui+Thymeleaf模板
  * 安全框架：shiro
  * 缓存：抽象缓存Ehcache
  * 简单的Restful风格开发
  * pagehelper分页助手
  * 加入了Druid数据监控
  
  ### 数据库文件
    数据库的文件放在了display目录下，可作为学习参考使用
  
  ### 模块说明(大体框架是这样，不做细分)
  
      src|——
            |——main |——
                    ├── java/com/braisedpanda |——
                                              |——bean               --:javabean
                                              |——config             --:自定义的各种配置类
                                              |——controller         --:controller层
                                              |——mapper             --:mapper借口层
                                              |——service            --:service层
                                              |——serviceimpl        --:service实现层，可以和service放在一起
                                              |——xxxxApplication    --:项目的启动类

                    ├── resource  |——
                                  |——mybatis     --：放置mybatis文件
                                  |——static      --:放置静态资源（图片、js、css之类的）
                                  |——templates   --:themeleaf模板
                                  |——application --：spring配置文件
                
  
  ### 预览
  

#### `学生列表`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/studentlist.jpg)<br><br><br>
#### `班级列表`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/classlist.jpg)<br><br><br>
#### `添加学生`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/addstudent.jpg)<br><br><br>
#### `我的考试成绩`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/mygrades.jpg)<br><br><br>
#### `各班级考试成绩`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/classgrades.jpg)<br><br><br>
#### `所有角色一览`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/allroll.jpg)<br><br><br>
#### `各角色对应的权限`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/role_permission.jpg)<br><br><br>
#### `新建权限角色（可定制可观看的菜单和对应的操作按钮）`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/addnewpermission.jpg)<br><br><br>
#### `授予某个用户权限`<br><br>
![](https://github.com/BraisedPanda/StudentManagementSystem/raw/master/display/givepermission.jpg)<br><br><br>


