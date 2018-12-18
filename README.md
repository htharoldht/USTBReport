# USTBReport 文档类说明

效果见[这里](https://github.com/htharoldht/USTBReport/blob/master/USTBReport-demo.pdf)

本模板符合北京科技大学实验报告的模板, 并添加了一份计算机与通信工程学院的实验报告封面.

主要用于对实验报告的撰写, 提供一个实验报告的实现机制.
设置采用 xkeyval 包, 实现了键值对的方式指定常量.

## 接口

``` tex
\USTBset{
  Course      = 微机原理与应用,  % 实验名称
  Instructor  = 万亚东,          % 指导老师
  Location    = 机电信息楼320,   % 实验地点
  School      = 计通学院,        % 学院
  Major       = 信息安全,        % 专业
  Class       = 信安1601,        % 班级
  Name        = 黄腾,            % 姓名
  Number      = 416245xx,        % 学号
  Year        = \the\year,       % 年
  Month       = \the\month,      % 月
  Day         = \the\day,        % 日
}
```

## 字体
如果使用

``` tex
\documentclass[CustomFont=true]{USTBReport}
```

才启用用户字体

以下为用户字体
- 衬线字体：

  本实验报告使用了思源黑体 Medium、DemiLight
  可以在[这里](https://mirrors.tuna.tsinghua.edu.cn/adobe-fonts/source-han-serif/OTF/SimplifiedChinese/)下载

- 非衬线字体：

  思源宋体 Bold、ExtraLight, Adobe 仿宋 Regular
  可以在[这里](https://mirrors.tuna.tsinghua.edu.cn/adobe-fonts/source-han-sans/OTF/SimplifiedChinese/)下载

- 等宽字体:

  文泉驿等宽微米黑
  可以在[文泉驿官网](http://wenq.org/wqy2/index.cgi)去下载

- 其他字体

  此外还需要有Times New Roman、Arial、AdobeFangsongStd-Regular

## 代码

如果使用

``` tex
\documentclass[Code=true]{USTBReport}
```

才启用 minted 排版代码

注: 如果需要两者同时开启, 则需要使用以下命令

``` tex
\documentclass[Code=true, CustomFont=true]{USTBReport}
```

HTNotes-code 中使用了 minted 以及tcolorbox 排版. 具体使用方法见文件(感谢夜神的代码)

### minted环境配置
1、先装python，装比较新的版本，会有自动安装pip和添加环境变量，就不用配置了
     （下载地址：Download Python | Python.org
                        https://www.python.org/downloads/）
     %注意将那个  设置路径  选项选上！！！

2、装好后，管理员命令行运行 pip install pygments

3、更新的话是这个命令： python -m pip install --upgrade pip

---------------------------------------------------------------------------------------

    文件位置：

    C:\software_of_me\Python\Lib\site-packages   （这里面有你安装的pygments目录）

    ===================================================

    PS C:\Users\Administrator> pip install pygments

    >>
    >
    Requirement already satisfied: pygments in c:\software_of_me\python\lib\site-packages (2.2.0)

    You are using pip version 10.0.1, however version 18.0 is available.

    You should consider upgrading via the 'python -m pip install --upgrade pip' command.

    PS C:\Users\Administrator> python -m pip install --upgrade pip

    Collecting pip

    Downloading https://files.pythonhosted.org/packages/5f/25/

    e52d3f31441505a5f3af41213346e5b6c221c9e086a166f3703d2ddaf940/pip-18.0-py2.py3-none-any.whl (1.3MB)

    100% |████████████████████████████████| 1.3MB 3.4MB/s

    Installing collected packages: pip

    Found existing installation: pip 10.0.1

    Uninstalling pip-10.0.1:

    Successfully uninstalled pip-10.0.1

    Successfully installed pip-18.0

    PS C:\Users\Administrator>


    ===================================================

以上是pygments安装成功的信息。

## 插图

- 插图初始定义了一系列文件夹, 用于图片的存放(在任一路径下均可)

- 子图采用的是较新的 subcaption 包

## 数学常见符号定义

见 HTNotes-math

## 其他见源代码

## TODO

- [ ] 制作一个说明文档
- [ ] 完善其余内容
