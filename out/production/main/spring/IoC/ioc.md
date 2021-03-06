1.谁控制谁？
当然是 IoC 容器控制了对象；

2.控制什么？
那就是主要控制了外部资源获取
（不只是对象包括比如文件等）。


IoC 和 DI
DI—Dependency Injection，即“依赖注入”：
是组件之间依赖关系由容器在运行期决定，
形象的说，即由容器动态的将某个依赖关系注入到组件之中。
依赖注入的目的并非为软件系统带来更多功能，
而是为了提升组件重用的频率，并为系统搭建一个灵活、可扩展的平台。
通过依赖注入机制，我们只需要通过简单的配置，而无需任何代码就可指定目标需要的资源，
完成自身的业务逻辑，而不需要关心具体的资源来自何处，由谁实现。

理解 DI 的关键是：
“谁依赖谁，
为什么需要依赖，
谁注入谁，
注入了什么”，
那我们来深入分析一下：

    谁依赖于谁：当然是某个容器管理对象依赖于 IoC 容器；“被注入对象的对象”依赖于“依赖对象”；
    为什么需要依赖：容器管理对象需要 IoC 容器来提供对象需要的外部资源；
    谁注入谁：很明显是 IoC 容器注入某个对象，也就是注入“依赖对象”；
    注入了什么：就是注入某个对象所需要的外部资源（包括对象、资源、常量数据）。

IoC 和 DI 由什么关系呢？
其实它们是同一个概念的不同角度描述，
由于控制反转概念比较含糊（可能只是理解为容器控制对象这一个层面，
很难让人想到谁来维护对象关系），
所以 2004 年大师级人物 Martin Fowler
又给出了一个新的名字：“依赖注入”，
相对 IoC 而言，“依赖注入”明确描述了“
被注入对象依赖 IoC 容器配置依赖对象”。
