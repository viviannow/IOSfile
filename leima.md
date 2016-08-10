# heima-study
自学黑马IOS教程，看下本大胖的自觉能力  http://www.itheima.com/apply/21265.html

学习IOS为什么要学c语言呢

IOS开发语言为Objective-C，objective-C语言是建立在C语言基础上的，学习开发IOS必须先学习C语言才更容易入手。

objective-C通常写作ObjC和较少用的Objective C或Obj-C，是扩充C的面向对象编程语言。

它主要使用于Mac OS X和GNUstep这两个使用OpenStep标准的系统，而在NeXTSTEP和OpenStep中它更是基本语言。


#内容整理 20160613

IOS是操作系統,直接運行于 IPhone, ipad, ipod touch,  ipad mini, apple tv

IOS开发， 用xcode 

mac os x  =》mac os

ios证书 调试证书 发布证书

pro 个人电脑  或 mac mini 


甩歌 苹果最先有的功能。后来废除了。

苹果各个尺寸
| 英寸       | 像素分辨率px |型号|
| -----      |----        |----|
|3.5         |480*320     ||
|4           |640*1136    |5s|
|4.7         |750*1334    |6|
|5.5         |1080*1920   |6p|

IPAD

IPAD AIR2 指紋解鎖

tv 電視盒子  中国好像没有


MAC OS X系統  macintosh系列 是基于unix内核的图形话操作系统

以下是一些mac下的软件：
```
cleanmymac 2

sketch

screenflow

paintbrush

snip

cornerstone

ipmessenger

teamviewer
```


xcode 可写的语言 ：c c++ objective-c  java


cocoa

command + r 运行
command + . 停止运行

花 <==> command键


快捷键

command + [ 缩小
command +] 放大

command+shift+h  <==>home键  回到模拟器的首页

command+1 2 3  模拟器屏幕大小 123从小到大


#内容整理 20160614

以下是C语言的难点

运算符 :  自增 自减

进制 : 转换 原码 反码 补码

数组 : 一二多纬数组

循环 : 多重循环的嵌套 排序 查找

函数 : 递归 

指针 : 一级 多级 指针和数组 函数 结构体之间的关系

内存管理 : 内存泄露 野指针

有参宏以及条件编译 :

多文件开发 : 多文件编译 多文件开发

程序说明：

每个函数都有自己独立的功能 

一个程序只有一个主函数  没有主函数 不具备运行的能力

函数只有在调用时才会执行,主函数由系统调用 

主函数有一定的书写规范



创建项目时说明：
```

product name  产品 名称  可以中文 但尽量写英文 

organization name 组织名 公司名

organization identifler 组织标识 公司域名倒着写

bundle identifler 程序的标识  

language 开发语言
```


main.c

c源程序的后缀.c

c源程序 由函数构成 只有一个主函数  函数只有调用时才会执行,主函数由系统调用 没有主函数 这个程序无法运行  主函数 main(){}

程序语句结束一定要有分号;

command + r 运行 c 语言

```
int main()
{
	printf("hello world");

	return 0;
}
```

#include <stdio.h> 引入一个头文件 表示stdio.h文件中就有printf这个函数

主函数
```
int main()   
{
	printf("hello world");

	return 0;
}

```
int 表示主函数的返回值

main主函数的名称

()表示是主函数的参数 

{} 函数体

printf("hello world"); printf是一个函数,是系统提供的,输出信息到控制台

\n 表示输出时换行

return 0 表示返回给系统一个0;表示程序正常执行并且推出

黄色叹号 : 这句话有个警告 不会影响程序的执行.

红色 圈  :  有错误,一定会影响程序的执行.


执行流程

源程序 =>编译(目标文件.o) =>链接(系统的库函数) 生成可执行文件.out  =>开始执行

不同的源文件做一个链接


打开 cpro.xcodeproj项目文件 双击打开项目，不要点击.c文件打开项目  



target方法 分支 目标

选中项目 => 中间 target+ 创建新的分支



```
#include<stdio.>
int main()
{
	printf("######\n");
	printf("######\n");
	printf("######\n");
	return 0;
	
}
```

C言语的关键字: 32个

```
auto double int struct break else long switch

case enum register typedef char extern return 

union const float short unsigned continue for 

signed void default goto sizeof volatile do 

if while static
```

关键字编译器中都是有特殊颜色的，以下是分类  

数据相关的关键

基本数据类型 
	void 
	char 
	int  
	float 
	double 


类型修饰关系 
	short 
	long 
	signed 
	unsigned 


复杂类型 
	struct 结构体声明 
	union 共用体 
	enum 枚举 
	typedof 
	sizeof 

存储类型 
	auto 
	static 
	register 
	extern 
	const 
	volatile 


流程相关的关键字  

跳转
	return 
	continue 
	break 
	goto 禁止使用


分支  
	if  
	else 
	switch 
	case 
	default 

循环  
	for  
	do while  
	while  




表识符 名称,
表识符划分: 关键字 预定义标示符 用户标示符



命名规范

	只能用数字 字母下滑线或美元符号组成

	不用数字开头

	不能与关键字重名

	严格区分大小写
```
int main()
{
	int abcd;
	int _a$b

}
```

驼峰命名法 :  
第一个单词的首字符小写其它都大写  userName   
或所有单词首字母都大小  

命名中允许最多有31个字符 多的会补忽视.   

避免命名中出现编号 , 如 value1 value2   



注释 不参与编译

 //  comman+/ 单行注释

/**/ 多行注释


数据类型

```
基本类型

	整型 short int long

	字符型 char

	实型 float double 

构造类型

	数组

	结构体 struct

	公用体 union

	枚举类型enum

指针类型 

空类型void

定义类型 typedef
```

不同的数据类型占用不同的存储空间
```
64位编译器下  字节数

	char      1

	int       4

	float     4

	double    8

	short     2

	long      8

	long long 8 

	void      8 

```
不同的数据类型标示的范围


常量 固定不变的数据

整型常量
	二进制  
	八进制 
	十进制 
	十六进制 

实型常量 
	单精度 
	双精度 

字符常量 
	普通字符 
	转译字符 

字符串常量 


整型常量

```
八进制 0开头 045=>

	二进制  0b 开头

	十六进制 以0x 开头

	十进制

```
实型常量

	单精度 2.3f  

	双精度 默认以这个标示 2.3  


字符常量  

	普通字符 ''单引号括起来 ,只能有一个字符

	转译字符 '\n' '\r'


字符串常量

	""号,可以是字符 数字 符号


变量 


作用域

printf 函数 

scanf 函数 