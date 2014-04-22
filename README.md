#GreenChrome

##简介
* 这是一个绿化Chrome的工具，通过winmm.dll劫持的方式，本程序会随着Chrome启动。如果检测到外部程序打开Chrome，则自动追加配置文件中的参数到Chrome命令行。所谓外部程序打开，也就是指不是由Chrome自己启动新进程，例如双击运行(Explorer.exe)，点击QQ面板上的邮箱(QQ.exe)。

##其它
* 虽然说的一直是Chrome，但其实程序内部并未指定可执行程序必须是"Chrome.exe"，所以也能把它用在其它能够使用winmm.dll劫持的程序上。
* 为了使得生成的dll比较小，所以工程用的是vc6编译。但是其中使用了psapi.h，你可能需要到新版SDK中提取头文件和库文件。
* 双图标的问题，在我电脑上win7、win8.1，把pin后的快捷方式设置为只读确实可以解决，但是似乎也有人不灵，希望有能力的同学帮忙找到最终解决办法。
* 报毒？我不知道有没有报毒的情况，但是通过dll劫持的方式运行，确实不是一个正常的操作。本来Chrome需要winmm.dll的时候，会去系统目录找的，但是当我们在它的目录下放了一个winmm.dll的时候，就会优先加载我们的dll了，正常的dll功能我们会转发给系统的dll去做，然后还可以加入我们自己的操作。

##版权
版权没有，随便复制。