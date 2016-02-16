Topaz 是一个用于开发EJB+JSP程序的小型框架，
为了演示开发使用方式，还提供了一个名为Turquoise的WEB程序例子。
并附带了我在开发中使用的MySql数据库。（数据库文件使用Navicat导出）
我是用的Eclipse版本为3.6 英文版。
提供的程序，分为 topaz、turquoiseEJB和turquoiseWAR这三个项目。
请在Eclipse中使用Ant编译这三个项目。（需要根据你的目录，修改Ant文件！）
其中，topaz是核心框架，提供了一些Java包以供继承开发之用，
并提供了名为"cn.com.topaz.servlet.ControllerServlet"的一个核心类，实现一个简单的控制器。
turquoiseEJB是一个EJB项目，继承了topaz的部分类，实现EJB例子。
turquoiseWAR是一个JSP WEB项目，提供了几个JSP例子。

EJB和JSP的基本调用流程： 由"cn.com.topaz.servlet.ControllerServlet"实现控制器，
> 对客户端请求，获得其Request内容，并调用相应的EJB，把从EJB返回的结果信息传递给JSP页面程序，
> 对于有状态的SessionBean，可以在JSP生成HTML时选择是否保存此EJB实例，以供下次调用。
> 具体内容，不在此处详述，有兴趣的朋友请参照源代码。（我已经加了注释，并可以直接生成Java的Doc）


注意：支持的EJB版本为3， 且仅支持SessionBean，不支持EntityBean，
> 数据库操作使用Topaz内提供的包"cn.com.topaz.db"来完成。

最后： Topaz（黄水晶）是我的生日石。Turquoise（绿松石）是我妻子的生日石。
> 这个程序是为了给希望学习EJB开发的朋友准备的，
> 同时，你也可以在Topaz的基础上，增加自己需要的功能，完善并开发出实用的系统。
> 除了文件上传的Java 包，所有的类都是我独自完成的。