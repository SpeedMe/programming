Spring框架倡导基于POJO(Plain Old Java Object,简单Java对象)的 轻量级开发理念.
为了能够让这些基础的POJO构建出健壮而强大的应用,Spring框架就好像那包裹地球的大气层一样,为构筑应用的POJO提供了各种服务,
进而创造了一套适宜用POJO进行轻量级开发的环境。

Spring框 架为POJO提供的各种服务共同组成了Spring的生命之树,如图所示:
![img](http://leihuang.qiniudn.com/2016-04-19%2015-53-16.png)

Spring提供了两种容器类型:BeanFactory和ApplicationContext。

- BeanFactory。基础类型IoC容器,提供完整的IoC服务支持。如果没有特殊指定,默认采用延迟初始化策略(lazy-load)。,才对 该受管对象进行初始化以及依赖注入操作。
所以,相对来说,容器启动初期速度较快,所需 要的资源有限。对于资源有限,并且功能要求不是很严格的场景,BeanFactory是比较合适的 IoC容器选择。
- ApplicationContext在BeanFactory的基础上构建,是相对比较高 级的容器实现,除了拥有BeanFactory的所有支持,ApplicationContext还提供了其他高级特性,
比如事件发布、国际化信息支持等,这些会在后面详述。ApplicationContext所管理 的对象,在该类型容器启动之后,默认全部初始化并绑定完成。所以,相对于BeanFactory来 说,
ApplicationContext要求更多的系统资源,同时,因为在启动时就完成所有初始化,容器启动时间较之BeanFactory也会长一些。在那些系统资源充足,并且要求更多功能的场景中, ApplicationContext类型的容器是比较合适的选择.

![img](http://leihuang.qiniudn.com/20151030111239.png)