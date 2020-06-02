# 从零开始学python

团队内部学习python 的进阶路线图，从初级开始

## 0. 学习路线：

0. 基础语法

0. pip 等相关用法

0. 团队协作额外技巧

0. python 各领域最佳实践

0. 其他说明

0. 友情提示

0. 常见错误解决办法

## 1.模块化

### 1.1 基础语法

参考

1. [基础语法](https://www.runoob.com/python/python-basic-syntax.html)
1. [变量类型](https://www.runoob.com/python/python-variable-types.html)
1. [运算符](https://www.runoob.com/python/python-operators.html)
1. [条件语句](https://www.runoob.com/python/python-if-statement.html)
1. [循环语句](https://www.runoob.com/python/python-loops.html)
    1. [while 循环](https://www.runoob.com/python/python-while-loop.html)
    1. [for 循环](https://www.runoob.com/python/python-for-loop.html)
    1. [循环嵌套](https://www.runoob.com/python/python-nested-loops.html)
    1. [break 语句](https://www.runoob.com/python/python-break-statement.html)
    1. [continue](https://www.runoob.com/python/python-continue-statement.html)
1. [数字](https://www.runoob.com/python/python-numbers.html)
1. [字符串](https://www.runoob.com/python/python-strings.html)
1. [列表](https://www.runoob.com/python/python-lists.html)
1. [字典](https://www.runoob.com/python/python-dictionary.html)
1. [函数](https://www.runoob.com/python/python-functions.html)
1. [模块](https://www.runoob.com/python/python-modules.html)
1. [文件IO](https://www.runoob.com/python/python-files-io.html)

要求:

基础要求：熟读,能快速查找对应文档并使用

升级要求：熟练使用不需要文档

周期：

1-2 周

### 1.2 pip 等相关用法

[官方资料](https://pip.pypa.io/en/stable/)

常用功能:

1. 安装
    
    1. pip install  `[package name]`
    1. pip install  `[package name]`==`[version]`
1. 卸载
    
    pip uninstall `[pakcage name]`

注:
    
    此模块文档由后期需要增加

### 1.3 团队协作技能

1. freeze 冻结环境
    
    `pip freeze > requirements.txt` 可以将本地开发环境所用到的库文件做冻结,在同一项目多人写作时,可以有效的分享依赖库,以及一键安装依赖库
    
    `pip install -r requirements.txt` 一键安装所有依赖库
    
    
1. logging 的使用
    
    在团队工作中尽量避免使用print ,请采用logging 模块做输出.通过logging.level 控制输出级别
    
    [相关资料](https://zhuanlan.zhihu.com/p/69071435)

1. README.md 文件引入
    
    在团队协作中,通常会引入README.md 作为说明文件,用于说明项目的使用方法,或者相关思考或者更新.在多人协作的工作中请尽量使用说明。

1. git or svn 工具的使用
    
    git / svn 是作为代码版本管理工具存在的。他主要解决的问题是
    
    1. 多人代码同步
    1. 代码版本记录
    
    注:
    
        在日常工作中,发现同学们有这么一个现象,就是,担心代码丢失,或者某个时间的代码效果比较好,很喜欢对代码做备份, 
        但是在备份期间以及备份后,很容易混乱代码,以及混乱项目结构.这在团队工作中很不可取.熟练使用git 或者svn ,
        可以省去做代码备份等工作。

1. 单元测试
    
    官方资料 [unittest](https://docs.python.org/3/library/unittest.html) [pytest](https://docs.pytest.org/en/latest/)
    
        python 提供多种单元测试模块,包括unittest 和pytest 等。
        
        在团队合作时，确保自己代码在满足要求的调用时，正确的运行是十分重要的。在个人项目以及团队合作中，单元测试都是值得完善的。
        
    
### 1.4 各领域最佳实践

参考
[python 最佳实践指南](https://pythonguidecn.readthedocs.io/zh/latest/)

重点阅读部分:

1. python 虚拟环境

    1. 资料:
        [python 虚拟环境](https://pythonguidecn.readthedocs.io/zh/latest/dev/virtualenvs.html#virtualenvironments-ref)
    1. 为什么要使用虚拟环境开发
        [相关搜索](https://zhuanlan.zhihu.com/p/108534526)
1. Cython 以及 setup tools打包
    
    [官方资料](https://pythonguidecn.readthedocs.io/zh/latest/scenarios/speed.html#id2)
    
    Cython 适用于c/c++ 代码扩展的.而setuptools 适用于代码打包的。两者可以结合使用.
    
    注:
        
        cython 的引入是为了防止代码泄露，特别是针对论文未发表的同学，是有很大意义的。
        同时setuptools 打包,可以避免算法团队和开发团队的耦合。
        一个好的使用案例是,钢筋识别编译成whl 文件,交付时给与编译后的whl 以及训练好的模型文件。

### 1.5 其他说明        

1. 相关库查询
    
    [pypi](https://pypi.org/) 是python 所有公共库的存放地址,可以直接搜索相关第三方库,从而找到对应的官方文档以及github 源码地址.请不要茫然相信个人博客.优选官方安装使用教程.

1. pip install 安装库文件速度很慢

    1. 搜索python 镜像源
    2. 替换 镜像源
        
        1. [windows 下替换镜像源](https://blog.csdn.net/rainraincn/article/details/86687900)


### 1.6 友情提示


请不要优先选择 conda

## 2 常见错误

- 错误提示无法定位到自己写的脚本的某行
    
    
    通常，通过pycharm run 一个脚本发生错误时，蓝色字体会由错误的位置开始报错，会逐层往上提示，
    直到我们所写的脚本的某个位置，通常把这个位置叫做顶层错误位置。
    
    如果在错误提示输出信息中，未找到自己编写的程序，则较大可能是系统环境（或者虚拟环境）本身出现错误。
    
    这类错误，可能来自于文件缺失，也有可能是源文件被修改带来的。
    
    可以通过pycharm 的setting 更换虚拟环境（此时一般可以进一步看看环境本身有哪些工具库，换了虚拟环境后，需要重新安装第三方库）
    
