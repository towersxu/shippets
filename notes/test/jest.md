# 使用jest测试typescript项目

https://www.grzegorowski.com/how-to-mock-global-window-with-jest

测试的目的是什么？

1. 将业务逻辑以测试的形式表现出来，便于监控在后续的迭代过程中，因为代码修改，而导致某些业务逻辑出错的情况。
以“自动触发commit为例”， 在流程执行的过程中，会遇到最后一个用户节点之后，需要前端给擎天柱引擎自动发起一个commit，是引擎继续驱动后面的系统节点。那前端如何知道当前的节点是流程中最后一个用户节点呢?前端是通过判断当前节点对应的表单中，是否存在用户驱动流程执行的按钮来判断的。也就是“下一步”按钮。只要表单中不存在下一步按钮，那就前端自动发起一个commit是流程继续执行。

如果有了测试，我们就知道，当以后的某一天，产品的迭代把下一步按钮形态改变了，比如不在表单固定按钮，而是增加多个按钮。每个按钮都可以使流程的继续。这个时候，我们代码已改，测试就会发现流程执行出现异常。就知道在这些按钮增加判断逻辑。


如何划分测试的粒度