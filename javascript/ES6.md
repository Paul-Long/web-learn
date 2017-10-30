# JavaScript 学习笔记
## 基本数据类型
<p>基础数据类型包含以下几种：</p>
<p>字符串（String）、数字(Number)、布尔(Boolean)、数组(Array)、对象(Object)、空（Null）、未定义（Undefined）。</p>
<p>可以通过typeof 来检测数据类型</p>

```bash
typeof "John"                // 返回 string
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
typeof null                  // 返回 object
```

## 变量

- var 以及es6中的let 和 const

- var 存在变量提升效用， let 和const不存在

## 语句
- if (...) {...} else if (...) {...} else {...}
- switch 语句
- for 循环
- while 循环 , break 跳出循环 , continue 继续循环

## 变量提升
* JavaScript中， 函数及变量的声明都将被提升到函数的最顶部.
* JavaScript中， 变量可以在使用后声明， 也就是变量可以先使用在声明。
* 初始化不会提升
* 使用严格模式 ， 在js 开头是使用 "use strict";

## JavaScript void
* href="#"与href="javascript:void(0)"的区别：
包含了一个位置信息，默认的锚是#top 也就是网页的上端。
而javascript:void(0), 仅仅表示一个死链接。
在页面很长的时候会使用 # 来定位页面的具体位置，格式为：# + id。
如果你要定义一个死链接请使用 javascript:void(0) 。

## JavaScript 函数定义
* 关键字function ， function functionName(params) {
    执行代码
}
```bash
function myFunction(a, b) {
    return a * b;
}
```

* 匿名函数

```bash
var func = () => {}
```

* 显式参数(Parameters)

```bash
functionName(parameter1, parameter2, parameter3) {
    // 要执行的代码……
}
```

* 隐式参数(Arguments)

```bash
x = findMax(1, 123, 500, 115, 44, 88);

function findMax() {
    var i, max = arguments[0];

    if(arguments.length < 2) return max;

    for (i = 0; i < arguments.length; i++) {
        if (arguments[i] > max) {
            max = arguments[i];
        }
    }
    return max;
}
```

## JavaScript 闭包

* 作用域: 全局变量 和 局部变量, Javascript 语言的特殊之处，就在于函数内部可以直接读取全局变量。在函数外部无法读取函数内部的局部变量。
* 如何从外部读取局部变量？
```bash
　　function f1(){
　　　　var n=999;
　　　　function f2(){
　　　　　　alert(n);
　　　　}
　　　　return f2;
　　}
　　var result=f1();
　　result(); // 999
```
<p>函数f2就被包括在函数f1内部，这时f1内部的所有局部变量，对f2都是可见的。但是反过来就不行，f2内部的局部变量，对f1就是不可见的。这就是Javascript语言特有的"链式作用域"结构（chain scope），子对象会一级一级地向上寻找所有父对象的变量。所以，父对象的所有变量，对子对象都是可见的，反之则不成立。</p>

* 闭包就是能够读取其他函数内部变量的函数。
  由于在Javascript语言中，只有函数内部的子函数才能读取局部变量，因此可以把闭包简单理解成"定义在一个函数内部的函数"。
  所以，在本质上，闭包就是将函数内部和函数外部连接起来的一座桥梁。
* 闭包的用途： 一个是前面提到的可以读取函数内部的变量，另一个就是让这些变量的值始终保持在内存中。

* 注意点： 使用不当，耗内存。