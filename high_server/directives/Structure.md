# 指令结构

通常而言，指令的结构可以解剖如下：

```scala
name(arguments) { extractions =>
  ... // inner route
}
```

指令具有：

* 一个名字
* 0 个或多个参数
* （可选的）内部路由（`RouteDirectives` 比较特殊，因为它们经常用于叶子节点，所以没有内部路由）

指令还可以 **提取** 一定数量的值，并将它们作为内部路由的参数暴露，从外部看来，路由与其内部路由一同组成类型为 `Route` 的表达式。
