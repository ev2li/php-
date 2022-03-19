### 3.1 php代码编译

c程序在编译时将一行行的代码编译为机器码，每一个操作都认为是一条机器指令，这些指令写入到编译后的二进制程序中，执行的时候将二进制程序load进相应的内存区域（常量区、数据区、代码区）分配支行栈，然后从代码区起始位置开始执行

![内存分部](https://img-blog.csdn.net/20180209110441881?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvdTAxNDQ3MDM2MQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)



php的解析过程任务就是将php代码转化为opcode数组，代码里的所有信息都保存在opcode中，然后将opcode数组交给zend引擎执行，opcode就是内核具体执行的命令，比如赋值，加减操作，函数调用，每一条opcode都对应一个handle，这些handle是提前定义好的c函数

![php编译](https://box.kancloud.cn/9a0103061fc5248a683d1ccfcb7e2ace_378x63.png)



php编译阶段如图：

![php编译过程](https://box.kancloud.cn/d9c4996f3723b6cde73658ed06145ccd_863x151.png)



### 3.2 词法分析、语法分析

re2c：词法分析器，将输入分割为一个个有意义的词块，称为token

bison：语法分析器，确定词法分析器，分割出的token是如何彼此关联的



$a = 3 + 4 -6

![img](https://box.kancloud.cn/16bf76a3daca3fe633e9f71216cb4290_479x293.png)

### 3.3抽象语法树编译流程