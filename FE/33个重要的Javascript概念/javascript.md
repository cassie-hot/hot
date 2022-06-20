# 1.调用栈

调用栈就是解释器（如web浏览器中的javascript解释器）跟踪其在调用多个函数的脚本中的位置的机制——当前正在运行什么函数以及从函数中又调用了哪些函数等。


# 2.原始类型（Primitive Types）

除了对象之外的所有类型都定义了不可变的值（即不能更改的值）。例如（不同于C语言），字符串时不可改变的。我们将这些类型的值称为”原始值“。


# 3.值类型和引用类型

分配了非原始值的变量将获得对该值的引用。引用指向对象在内存中的地址。变量实际上并不包含值。


# 4.隐式、显式、标称、结构化和鸭子类型

类型强制意味着当运算符的操作数是不同的类型时，其中一个将被转换为另一个操作数类型的”等价“值。


# 5.== 和 === 和 typeof

let primateOne = '777'
let primateTwo = 777
primateOne == primateTwo  // true
primateOne === primateTwo // false

typeof primateOne  //'string'
typeof primateTwo //'number'


# 6.函数作用域、 块作用域和词法作用域

function foo(a) {
    var b = a * 2;
    function bar(c) {
        console.log(a, b, c);
    }
    bar(b * 3);
}
foo(2); //2, 4, 12

词法作用域： 定义在词法阶段的作用域。是由你在写代码时将变量和块作用域写在哪里来决定的。

函数作用域：属于这个函数的全部变量都可以在整个函数的范围内使用（事实上也可用于嵌套的作用域）。


# 7.表达式与语句

表达式可以像语句一样工作，这就是我们也有Expression语句的原因。但是，另一方面，语句不能像表达式那样工作。


# 8.IIFE、模块和命名空间

常用的函数编码模式有一个花哨的名字：Immediately-invoked Function Expression（立即调用函数表达式）。或者更广为人知的是被写作IIFE。


# 9.消息队列和事件循环

问： Javascript如何异步和单线程？
答： Javascript语言是单线程的，异步行为不是Javascript语言本身的一部分，而是构建在浏览器（或编程环境）中的核心Javascript语言之上，并通过浏览器API访问。


# 10.setTimeout、setInterval和requestAnimationFrame

我们可以决定现在不执行函数，而在以后的某个时间执行。


# 11.Javascript引擎

在写JS代码有时感觉有点神奇，因为开发人员编写的一系列字符就像魔术一样，在浏览器中变成具体的图像、文字和动作。

这一切都是由JS引擎在背后默默支持着。


# 12.位运算符、类型数组和数组缓冲区

好的，从技术上讲，对于计算机来说，一切都归结于1和0。因为计算机不使用数字，也不使用字符或字符串，它只使用二进制数字（位）。即一切都以二进制形式进行存储。然后计算机使用UTF-8等编码将保存的位组合映射到字符、数字或不同的符号（ELI5版本）。


# 13.DOM和布局树

文档对象模型，通常称为DOM，是使网站具有交互性的重要部分。它是一个界面，允许编程语言操作网站的内容、结构和风格、Javascript是链接到Internet浏览器DOM的客户端脚本语言。


# 14.工厂和类

Javascript是基于原型的语言，意味着可以通过具有克隆和扩展能力的通用对象来共享对象属性和方法。这称为原型继承，与类继承不同。


# 15.this、 call、apply和bind

这些函数对每个JavaScript开发人员都非常重要，以为几乎每个Javascript库或者框架中都会用到。


# 16.new、Constructor、instanceof和Instances

每个JavaScript对象都有一个原型。Javascript中的所有对象都是从其原型继承其方法和属性。


# 17.原型继承和原型链

Javascript对于学习基于类的语言（如Java 或C++）的开发人员来说有点困惑，因为它是动态的并且本身不提供类实现（class关键字ES2015引入，但却是语法糖，Javascript仍然基于原型）。


# 18.Object.create和Object.assign

Object.create方法是在Javascript中创建新对象的方法之一。


# 19.map、reduce、filter

即使你不知道什么是函数式编程，也可能一直在使用map、reduce和filter。他们非常有用，可帮助编写更清晰的逻辑。


# 20.纯函数、函数副作用、状态突变和事件传播

我们的许多错误都是植根于IO相关、数据突变、带有副作用的代码，然后在代码库中蔓延——从接受用户输入、通过http调用接收意外响应或写入到文件系统。不幸的是，这是一个我们不得不习惯的残酷现实。


# 21.闭包

闭包是将（封闭的）函数与对其周围状态（词法环境）的引用捆绑在一起的组合。换句话说，闭包使你可以从内部函数访问外部函数的范围。在Javascript中，每次创建函数的同时都会创建闭包。


# 22.高阶函数

Javascript可以接受高阶函数。这种处理高阶函数的能力以及其他特性使Javascript成为非常适合函数式编程的编程语言之一。


# 23.递归

可以扩展你对函数式编程的理解。


# 24.集合与生成器

生成器函数返回Generator对象，同时符合可迭代协议和迭代器协议。


# 25.Promise

Promise对象表示异步操作的最终完成（或失败）及其结果值。


# 26. async/await

async/await是一种可以以更舒适的方式处理Promised特殊语法。非常容易理解和使用。


# 27.数据结构

Javascript每天都在发展。随着React、Angular、Vue、NodeJS、Electron、React Native等框架和平台等快速增长，将Javascript用于大型应用程序已变的相当普遍。


# 28.昂贵的运算和Big O标记法

“什么是Big O标记法？“这是一个非常常见的面试问题。简而言之就是算法运行时间取决于输入时间的数学表达式，通常谈论最坏的情况。


# 29.算法

在数学和计算机科学中，算法是有明确定义的指令的有限序列，通常用于解决一类特定问题或执行计算。


# 30.继承、多态和代码重用

类继承是一个类扩展另一个类的一种方式，因此我们可以在现有的基础上创建新功能。


# 31.设计模式

每个开发人员致力于编写可维护、可读和可重用的代码。随着应用程序变得越来越大，代码结构变得越来越重要。设计模式被证明是解决这一挑战的关键——为特定情况下的常见问题提供组织化的结构。


# 32.部分应用、Currying、Compose和Pipe

函数组合是一种组合多个简单函数以构建更复杂函数的机制。


# 33.干净的代码

编写干净、可理解和可维护的代码时每个开发人员都必须掌握的一项技能。













fatal: unable to access 'https://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@github.com': LibreSSL SSL_connect: SSL_ERROR_SYSCALL in connection to github.com:443 