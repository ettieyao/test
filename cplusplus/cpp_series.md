[toc]
# how c++ works
### solution platform
x86 - 32 bit windows
x64 - 64 bit 
### text -> excutable binary
- compling
- linking
### compiler
.h - when #include
.cpp - compiler
.obj - intermediate format
### linker ( resolve symbols )
.exe 
- resolving 解析多个.obj

# how the c++ compiler works
### complier -> .obj
#### pre-process
include, define, if, endif 
(pragma statement)告诉编译器具体要做什么
###### 预处理
C/C++ - 预处理器，生成.i文件（不生成.obj）
可以看到预处理过程。

#### tokenizing(标记解释)
#### parsing(解析)
abstract syntax tree 语法抽象树 - machine code(cpus can execute)
constant data/instructions(指令)
constant variables

.cpp files - translation unity

##### 代码生成，机器码
C/C++ - 优化 - 最大优化（优先速度O2）
C/C++ - 输出文件 - 汇编程序输出（仅有程序集的列表/FA）

register寄存器

运行时检查
constant folding常量折叠 - 常量在编译时就计算了。

# how the c++ linker works
linking：c++ 源码 -> .exe可执行二进制
找到每个符号和函数的位置，链接在一起
### error的类型
C - 编译错误
LNK - 链接错误
### 程序的入口
Linker - 高级 - 入口点
- 无main函数会发生linking错误
- 程序入口不一定必须是main函数
### 函数前的static
若无static，该函数可能在其他的cpp中使用。linking时可能报错。
若有static，只在当前文件中使用。
### 头文件通常不放definition，放declaration，最多只放一个inline
一个头文件中的Log同时被两个cpp去include
用static or inline
头文件不放定义，最多只放一个inline

# variables in c++
变量被创建，存储在memory中的stack or heap
primitive data types:(size)
how much memory does this variable occupy when it comes down to it?
int - 4 bytes
-2billion ~ 2billion

