### Vue 源码第二步

#### 当前 Vue 的版本 V2.2.2

#### 生命周期 相关介绍

    我们可以从 setp1 中 去看到那张 vue 的生命周期图中看到，vue 的生命周期钩子。 具体的钩子时干什么的？ 以及在源码中是如何展示的。

##### create new Vue 时， 会先进行 create 创造出 Vue 对象

##### mounte 根据 el template render 方法属性，会生成 DOM，并添加到对应 位置

##### update 当数据发生变化的时候，会重新渲染 dom ,并进行替换

##### distory 销毁时 运行

    那么接下来这 四个过程 在源码中的实现过程是 什么样子的呢？
    ，不要着急。 我们一步步来看

再开始之前，我们先看一张 结构图。当然这张和 囧克斯 的那张区别还是有点不一样。


![](http://images2015.cnblogs.com/blog/675289/201703/675289-20170326234803830-659549447.jpg)


1. 首先对应的是 new Vue() 的时候。 代码进入 core/instance/index.js


