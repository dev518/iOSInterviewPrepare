## 1. 为什么说Objective-C是一门动态的语言？
动态类型：运行时接受
动态绑定
动态栽入
## 2.简要概括一下 MVC 和 MVVM，MVP三种模式。

## 3.为什么代理要用weak？代理的delegate和dataSource有什么区别？block和代理的区别?

## 4.属性的实质是什么？包括哪几个部分？属性默认的关键字都有哪些？@dynamic关键字和@synthesize关键字是用来做什么的？
 1. `@property = ivar + getter + setter;`
 2. 属性可以拥有的特质分为四类:
 
* 原子性--- nonatomic 特质,在默认情况下，由编译器合成的方法会通过锁定机制确保其原子性(atomicity)。如果属性具备 nonatomic 特质，则不使用自旋锁。请注意，尽管没有名为atomic的特质(如果某属性不具备 nonatomic 特质，那它就是“原子的” ( atomic) )，但是仍然可以在属性特质中写明这一点，编译器不会报错。若是自己定义存取方法，那么就应该遵从与属性特质相符的原子性。
* 读/写权限---readwrite(读写)、readonly (只读)
* 内存管理语义---assign、strong、 weak、unsafe_unretained、copy
* 方法名 - getter= 、setter=
3. 属性的默认关键字:
* 在 ARC 下，如果如果修饰的是 Objective-C 对象
`@property (atomic，strong,readwrite) UIView *view;`

* 如果如果修饰的是基本数据类型。
`@property (atomic，assign,readwrite) int num;`
4. “自动合成”( autosynthesis)
`完成属性定义后，编译器会自动编写访问这些属性所需的方法，此过程叫做**“自动合成”(autosynthesis)。需要强调的是，这个过程由编译 器在编译期执行，所以编辑器里看不到这些“合成方法”(synthesized method)的源代码。除了生成方法代码 getter、setter** 之外，编译器还要自动向类中添加适当类型的实例变量，并且在属性名前面加下划线，以此作为实例变量的名字。 也可以在类的实现代码里通过**@synthesize** 语法来指定实例变量的名字.`
5. @dynamic
`告诉编译器,属性的setter与getter方法由用户自己实现，不自动生成`
如果@synthesize和@dynamic都没写，那么默认的就是
`@syntheszie var = _var;
// @synthesize的语义是如果你没有手动实现setter方法和getter方法，那么编译器会自动为你加上这两个方法。
// @dynamic告诉编译器,属性的setter与getter方法由用户自己实现，不自动生成。`
## 5.NSString为什么要用copy关键字，如果用strong会有什么问题？
https://github.com/liberalisman/iOS-Interview-Question-Answer
## 6.为什么IBOutlet修饰的UIView使用weak关键字
## 7.是否了解链式编程
  
* Block 作为当前对象的属性
* Block 返回值是当前对象。
https://github.com/liberalisman/iOS-InterviewQuestion-collection/blob/master/其他问题/6.第六题.md
## 8.ios 历年新特性

* 开发者所需要知道的 WWDC 2018 新特性
  https://onevcat.com/2018/06/wwdc-2018/
* 开发者所需要知道的 iOS 11 SDK 新特性
https://onevcat.com/2017/06/ios-11-sdk/
* 开发者所需要知道的 iOS 10 SDK 新特性 https://onevcat.com/2016/06/ios-10-sdk/
* 开发者所需要知道的 iOS 9 SDK 新特性
   https://onevcat.com/2015/06/ios9-sdk
* 开发者所需要知道的 iOS8 SDK 新特性
  https://onevcat.com/2014/07/developer-should-know-about-ios8/

## 9.喵神MVC讲解
https://onevcat.com/2018/05/mvc-wrong-use/

## 10.apns
 * 活久见的重构 - iOS 10 UserNotifications 框架解析https://onevcat.com/2016/08/notification/


