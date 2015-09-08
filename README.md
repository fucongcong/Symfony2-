# Symfony2-
##1.登陆机制（思想可以参考）
内部提供了登陆验证机制，路由地址为/login
它提供了UserAuthenticationProvider，供我们继承。
实现其内部的retrieveUser（获取数据库中得用户，我们需要实现UserProvider类继承自UserProviderInterface，来提供loadUserByUsername方法，获取用户）
拿到用户之后，实现checkAuthentication进行验证，当前拿到的用户与输入的用户是否一致！

##2.事件派发解耦机制（EventDispatcher，思想可以参考）
向EventDispatcher中添加 实现了EventSubscriberInterface接口的 用户类
在事件派发时，直接Dispatcher 对应得 用户类（实现了EventSubscriberInterface接口）中得方法 即可！

##3.监听器机制（Listener）
应该是进行try，catch时候，或者具体的比如是ajax请求，登陆时，退出时向代码中增加监听器，一旦触发时，比如登陆失败，则会触发该监听器。

##4.服务提供机制（ServiceProvider）

##5.模块化机制（许多框架都已实现，类似Bundle）
