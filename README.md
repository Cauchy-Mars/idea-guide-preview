# 关于IDEA的那些事

说到Java的IDE，似乎eclipse和Idea是目前的主流。然而，OO的课程组却一直在推荐使用eclipse，于是很多人就这样错过了Idea这样强大的IDE工具。本文将会对于Idea和Idea的一些常见（实际上，很多是Jetbrains系列IDE的代表性操作）操作进行一些介绍。

## Jetbrains的那些事
### Jetbrains
Jetbrains是捷克的一家企业（[Jetbrains官网](https://www.jetbrains.com/)），目前其主打产品是各个现代主流语言的IDE，包含`Python`、`Ruby`、`PHP`、`SQL`等语言（对于企业用户还提供一些teamwork管理工具）。其IDE用过的人都知道，颇具现代感，很多功能解决了令不少程序猿们头疼多年的难题（_后面将会详细讲到_）。

### Idea

Idea则是Jetbrains全家桶的一员（[Idea官网](https://www.jetbrains.com/idea/)），其除了Jetbrains一些共性的王牌功能之外，还针对Java这门语言的一些特性进行了进一步的用户体验优化。（_后文也将详细阐述_）


## Idea的那些事
### 下载安装Idea
初次打开Idea的下载页面，一下子就懵了：
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401170622526-507795689.png)

499刀一年。。。看的有些肾疼。那是不是我们Idea之旅就要就此止步了呢？Of course, **NO!**

让我们继续往下看：
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401171002449-1960143244.png)

果然，`Intellij Idea`和`Pycharm`一样，都提供了**完全免费的社区版**，可以直接下载使用。

然而，对于本科生，我们依然**可以通过注册学生账号的方式来免费使用Ultimate版**（准确的说，Jetbrains大礼包里面除了完全面向企业的团队工具之外，所有的专业版工具都可以凭学生优惠免费下载使用）

大家可以自己去**按照[官网的引导](https://www.jetbrains.com/student/)或者网上的教程等进行认证操作和许可证的免费申请**，本文中不再赘述。

安装的过程也并不复杂，也没有什么坑点，大家可以自行完成。

（注：本文中接下来的图片示范均以Ultimate版为例）

### 开始使用

（**在开始本节之前，请一定保证你已经妥善完成了JDK的安装与环境配置**）

初次打开软件时，可能会需要你设置一些风格主题一类的东西，这个按照自己的喜好设置就好（笔者本人力荐`Darcula`黑色风格<del>，通宵爆肝护眼必备</del>），而且在进入软件之后，也可以在Setting中继续进行设置。

创建新工程时，我们只需要按照一般的套路来：`File`-->`New`-->`Project...`

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/idea-new-project-1.png)

在我们的作业项目中，我们不使用框架，使用原生Java。所以一路Next到最后一步。

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/idea-new-project-2.png)

在这里，我们需要设置一下项目名，然后点击`Finish`，即可完成项目创建。

接下来，只需要在`src`路径下创建程序文件，并运行即可，如下图所示。

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/idea-new-project-3.png)

### 代码风格

笔者做了三次OO作业，看了三份不同的代码。老实说这三个人的代码思维能力都是挺不错的，然而，代码风格却不是很能看，或者说，这样的代码即便没有任何bug，也根本不可能用在真正的团队工程中。

研读过[阿里巴巴java开发代码规范手册](https://files.cnblogs.com/files/han-1034683568/%E9%98%BF%E9%87%8C%E5%B7%B4%E5%B7%B4Java%E5%BC%80%E5%8F%91%E6%89%8B%E5%86%8Cv1.2.0.pdf)的同学们应该知道，在真正的工程代码中，处于**代码可维护性**和**提高团队合作效率**的考量，会有很多代码规范性的要求。

然而，可能不少同学已经写了规模不小的代码，而且从未参照过代码规范。不必担心，jetbrains给我们提供了很方便的代码风格工具：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401195908010-176794999.png)

可以看到，使用`tab`还是空格缩进，以及缩进几格都是可以自由调整的（实际上，**一般企业的代码工程规范是使用4个空格作为缩进**）。此外，在别的标签页下，还有很多可以调整的代码风格相关的东西（**包括你们圣战了无数年的大括号换行不换行问题**）。

而这样的代码习惯调整，只需要**Menu -> File -> Settings -> Editor -> Code Style -> Java**即可找到并调整（可以看到，除了java还有非常多种的语言。没错，一般的jetbrains IDE都支持多种语言的编辑，如果你有同时使用多种语言的需求的话，可以在其他语言对应的区域进行编辑。）

在我们调整好了之后，我们在代码位置按下`Ctrl`+`Alt`+`L`（Pycharm中是`Alt`+`F8`）即可**完成代码规范化**（或者**Menu -> Code -> Reformat Code**），效果如下：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401200645513-2033023354.png)

只需要按下`Ctrl`+`Alt`+`L`，代码立刻就变成了这样：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401200708862-882021272.png)

代码瞬间变得干净整洁，清清爽爽。

### 高度智能的联想
说到代码联想，大家可能对这一概念并不陌生。事实上很多的IDE也都已经在支持这一功能了。

但是，等你一用idea的代码联想功能，你就会再也放不下来了。

说到代码联想，大家肯定会很快的想到eclipse的联想功能：
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401184917013-1978250277.png)

然而，eclipse的代码联想实际上存在一些局限性（以及其他很多的IDE也是这样）：

* **写类名的时候没有联想** 例如，开始写System这个类时，整个过程不会出现任何的联想
* **联想出来的方法快捷键操作不便** 例如，当System按下`.`之后输入`e`，联想到了`exit`，但总还是需要一些比较不优雅的操作（比如鼠标操作，比如并不符合人类直觉的一些其他操作）来快速输入

这意味着什么呢？这意味着，**当你对一门语言或者某些类不够熟悉（甚至根本不知道它们的存在）时，你连自我尝试和探索的可能性都没有**，只能去翻阅冗长且并不友好的java文档，这显然不符合程序猿的探索精神。以及，如此不优雅的快速输入，多年的码农表示怎么用怎么觉得**别扭**。

然而在idea中，这些问题都得到了极大地改善：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401185837058-1931272267.png)

* **从输入类名的第一个字起，就可以进行智能的联想** 仔细观察上图的话还可以发现一件有趣的事情，输入`LC`后，连我们的LiftController类都联想到了。是的，idea的代码联想完全支持英文音序联想。
* **根据用户近期使用的情况来智能调节联想顺序** 这是idea代码联想另一个很神奇很贴心的feature，如果你近期频繁使用`LC`来输入LiftController类的话，你会发现LiftController类会在列表中越来越靠前，最多两三次过后就跑到了顶部。
* **可以直接按上下键和回车来进行快速键入** 这一点相比eclipse等其他ide有了非常大的改善，整个过程非常符合一般人的操作直觉，且全过程**不依赖任何键盘以外**的操作。

有了idea强大的代码联想功能（准确的说，jetbrains全家桶IDE都有这些特性），我们的代码产出速度可以大幅度提升。不仅如此，我们还可以**对于并不熟悉或者未知的一些代码或库进行大胆的尝试**，不得不说，这一功能还很适合进行自我探索。

### import自动添加

在Idea中，我们实际上不需要一条一条在顶上打`import`语句。

我们只需要想到了某个类或者某个方法，直接在程序中写上去，然后ide就会提示该类未导入，就像这样

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/class-import-1.png)

我们只需要将鼠标或者光标移至该类名上，并使用`Alt`+`Enter`快捷键，从提供的类中选择需要的，完成自动添加。（有时可能只有一个类可供选择，此时将不会出现选择直接完成添加）

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/class-import-2.png)

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/class-import-3.png)

### 批量修改

不知道大家有没有遇到过这样的尴尬状况：
```java
public class Scheduelr {
    // something inside
}
public abstract class Main {
    public static void main(String[] args) {
        Scheduelr s = new Scheduelr();   // execution of the constructor method
        Scheduelr.someStaticMethod();   // execution of the static method
        /*
            LOTS OF CODE HERE THAT USES THE SCHEUDUELR
        */
    }
}
```

没错，细心的你应该已经发现了问题所在——`Scheduelr`类名的拼写是错误的，应该是`Scheduler`。

按照一般的代码规范，这样的拼写错误绝对是不可以容忍的（就算可以容忍，这样的东西也会导致笔者强迫症大犯 -_-||）。

然而，再一看，可能已经有无数的地方已经在用着这个拼写错误的类名调用。想改？烦得很，而且还很容易错改和漏改。不改？强迫症使我面目全非o(╥﹏╥)o。于是，相信很多人最终的选择还是——不改，宁可被自己代码恶心一遍遍也不能有bug。

实际上，idea在这件事情上有很完美的解决方案：
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401194343600-874338075.png)

只需要在类名（实际上方法名、变量名、甚至文件名等也都可以这么做）上右键->Refactor->Rename，或者直接`Shift`+`F6`，即可**直接修改名字**，而且**整个工程中相关的地方也都会一起随之改动**。

更有趣的是，笔者做了一个实验：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401194937198-1568114198.png)

在这样的一个函数中，将第一个for循环内的`x`值进行rename操作，效果如下：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401195011937-1775398880.png)

可以看出来，idea的rename功能完全**不会误伤到不同作用域类的同名实体**，可以说是做到了精确打击。

此外，Refactor中还提供了Safe delete等人性化的功能，等待大家去尝试（Safe delete是在删除类、方法、变量时，检测是否依然在其他的地方对该实体存在依赖，以达到安全删除的目的）。

此外，**IDEA中还提供自动的单词拼写检查**，如果出现错误的单词拼写，则会像word一样第一时间显示出来并提示编程者尽快修复，或者将该单词（因为的确可能有存在专有名词等非常规词汇的情况）添加进工程字典内。

### 代码快速查看

有的时候，代码一旦变得复杂，我们就会需要经常在方法和类之间来回跳跃查找代码。

然而在IDEA中，这一麻烦不复存在，我们可以直接在类名、方法名、变量名上进行`Ctrl`+`鼠标左键`，一键跳跃到想看的类或方法的代码实现位置上。（甚至可以跳到java的底层源代码上，源码党们的福音）

就像在上面的程序的`nextInt`方法上点击`Ctrl`+`鼠标左键`，结果如下：

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/code-approach-1.png)

我们成功跳到了Java底层对`Scanner`类`nextInt`方法的源码实现上。

### 快速寻找我想要的功能

IDEA作为一款真真正正的现代化ide，和其他一些古代编辑器相比，另一大亮点就是可以快速寻找想要的功能。

在菜单栏，点击`Help`-->`Find Action`（快捷键为`Ctrl`+`Shift`+`A`）

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/idea-find-action.png)

可以在这里直接搜索想要找的功能或者设置。（实际上Jetbrains的Find Action功能提供非常精细的查找，不仅仅支持菜单栏的查找，连内部设置的细节甚至都可以找得到）

### javadoc
在正规的工程代码规范中，还有一项很重要的要求——写文档。

然而，这个文档也是有很严格的规范的，不是很多人认为的那样，随便注释一点就可以当做文档。而这种**符合java工程规范的文档形式就称之为javadoc**（类似的代码注释规范还有phpdoc等，更多的规则等细节可以自行查阅代码规范手册或者百度，本文中不作过多讲述）

比如，我们再次来到之前写的`test`方法上，打入`/`、`*`、`*`，再按下回车：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401203524366-2030254843.png)

然后我们按照规定的格式来补齐这个javadoc框架：

![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401203614262-1493533614.png)

一个格式规范且很清晰的方法文档就这样生成了。

除此之外，javadoc规范另外一个很重要的用途就是可以一键生成html页面版项目文档。点击**Menu -> Tools -> Generate Javadoc**，即可自动生成完整的javadoc网页版文档（[具体操作可参考此教程](https://www.cnblogs.com/xiaoming0601/p/6657136.html)）

### Git
除此之外，Idea实际上也像eclipse一样对于git有完美的图形化支持。然而笔者一直使用git命令行进行所有git相关操作，对这一块暂不是很熟悉。所以还请各位搜集资料并自行探索。

### 插件
实际上，在这个网络化体系化作战的时代，jetbrains也有**很多的在线插件支持**。

我们只需要进入**Menu -> File -> Settings -> Plugins**，再点击`Install Jetbrains plugin...`，即可**搜索插件**并直接进行**在线安装**。（实际上，由于大陆内一些神奇的不可言表的原因，经常会出现连接失败或者下载速度极慢的情况。这时候请自行**设置代理**，本文不再赘述）

接下来笔者来安利几款比较好的插件：

#### MetricsReloaded
对于之后的博客作业，我们需要用到的代码分析插件。
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401201902847-173153241.png)

#### Statistic

这个插件没啥别的功能，就是统计代码行数。那意义何在呢？嘿嘿，试想写着代码，看着代码行数不断飚增，是不是一件很带感的事情呢(*^▽^*)。
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401202104776-1117234963.png)


#### .ignore
这是个管理.gitignore的插件，可以用颜色标记出当前项目下所有文件的git状态（包括<b style = "color: gray">Ignored</b>，<b style = "color: red">Untracked</b>，<b style = "color: lightblue">Unmodified</b>，<b style = "color: lightgreen">Modified</b>）

#### Markdown support
对于使用Markdown书写文档的同学来说，能有一款优雅可视的内置插件当然是一件很爽的事情。就像这样
![](https://images2018.cnblogs.com/blog/703546/201804/703546-20180401201137552-1220648807.png)

#### Background Image Plus

对于想要给自己的ide设置壁纸的同学们，可以安装这一插件，并进行相关的配置，就像这样。

![](http://misaka-oss.oss-cn-beijing.aliyuncs.com/cs/oo_assistant_files/idea-usage/backgound-image-plus-chtholly.png)