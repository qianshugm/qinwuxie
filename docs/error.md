# 记错本

* doPost请求方式报错:HTTP Status 405 - HTTP method GET is not supported by this URL
  * 原因:doPost请求只可以通过表单提交方式(不可以直接访问Servlet),而 *<li>* 标签是通过doGet方式请求,需要先跳转到JSP页面,然后在通过表单提交跳到Servlet.
  * 错误信息:![1577190358907](C:\Users\Lenovo\AppData\Local\Temp\1577190358907.png)

  

  

  ----

  2019年12月25日10:44:36

* BeanUtils.populate 报错 java.lang.NoClassDefFoundError: 

  * 错误信息: 没有找到 org/apache/commons/beanutils/BeanUtils 这个类
    * ![1577241768448](C:\Users\Lenovo\AppData\Local\Temp\1577241768448.png)
  * 原因: 
    * jar包导入到了编辑器,Tomcat服务器没有导入工具包
  * 解决方法:
    * 将jar包直接复制在Tomcat目录下的lib文件夹,或者从编辑器将jar包导入Tomcat服务器
