# 编译系统调试

## 调试开关

* 在`make ...`命令行中, 设置`TOP_Q`变量为空, 可打印工程顶层的执行逻辑, 例如硬件平台的选择, SDK主库的生成等

        make .... TOP_Q=

* 在`make ...`命令行中, 设置`Q`变量为空, 可打印模块内部的编译过程, 例如目标文件的生成, 头文件搜寻路径的组成等

        make .... Q=

## 对单个编译单元调试

* 可以用`make foo/bar`单独对`foo/bar`进行构建, 不过, 这可能需要先执行`make reconfig`
* 可以进入`.O/foo/bar`路径, 看到完整的编译临时目录, 有makefile和全部源码, 所以在这里执行`make`, 效果和`make foo/bar`等同