IOS原生项目

包括：
	12生肖（慕课网视频）

语言：
	swift

开发工具：
	xcode ps 

测试工具 ：
	暂不测试



这是swift项目 

Swift 环境搭建
Swift 基本语法
Swift 数据类型
Swift 变量
Swift 可选类型
Swift 常量
Swift 字面量
Swift 运算符
Swift 条件语句
Swift 循环
Swift 字符串
Swift 字符
Swift 数组
Swift 字典
Swift 函数
Swift 闭包
Swift 枚举
Swift 结构体
Swift 类
Swift 属性
Swift 方法
Swift 下标脚本
Swift 继承
Swift 构造过程
Swift 析构过程
Swift 可选链
Swift 自动引用计数
Swift 类型转换
Swift 扩展
Swift 协议
Swift 泛型
Swift 访问控制
=======================================
【swift教程】

苹果于2014年WWDC（苹果开发者大会）发布，用于开发 iOS，OS X 和 watchOS 应用程序。
Swift 结合了 C 和 Objective-C 的优点并且不受 C 兼容性的限制。
Swift 在 Mac OS 和 iOS 平台可以和 Object-C 使用相同的运行环境。
2015年6月8日，苹果于WWDC 2015上宣布，Swift将开放源代码，包括编译器和标准库。

var myString = "hello,world!"

print(myString)

====================================
【Swift 环境搭建】
Swift 开发工具Xcode下载

xcode => file => new => playground


【ios playground 的程序】
import UIKit
var str = "Hello, playground"

【os x  playground 的程序】
import Cocoa
var str = "Hello, playground"

Cocoa 本身由 Objective-C 语言写成，Objective-C 又是 C 语言的严格超集，所以在 Swift 应用中我们可以很简单的混入 C 语言代码，甚至是 C++ 代码。

项目

xcode => file => new => project [Single View Application]  

Main.storyboard  大小为平板界面大小。 如果开发都只需要开发兼容iphone手机的app,那么可以把Use Auto Layout的勾去掉（默认为勾上）。

iPhone或iTouch的宽为320像素，高为480像素，状态栏高为20像素，toobar高为44像素，tabbar高为49像素，导航栏高为44像素。


运行一下模拟器（command+R 快捷键或在菜单栏中选择 Product => Run)。


====================================
【Swift 基本语法】

标记可以是：单词 标识符 常量 字符串 符号

注释 
//  
/**/   
/*
	/**/  
 */ 
 
标识符 区分大小写  可由_ 字母开始但不可以是数字  其它字符可以_ 字母 数字


关键字  声明相关  语句相关 表态式 类型相关   特定上下文中使用的关键字


空格 let a = 1 + 2;  // 编码规范推荐使用这种写法


字面量
42                 // 整型字面量
3.14159            // 浮点型字面量
"Hello, world!"    // 字符串型字面量
true               // 布尔型字面量

====================================
【Swift 数据类型】
变量的数据类型决定了如何将代表这些值的位存储到计算机的内存中。在声明变量时也可指定它的数据类型。


内置数据类型
int 
UInt
浮点数


















