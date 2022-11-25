1. 基础语法

```
const hello : string = "Hello World!"
console.log(hello)
```

2. 基础类型

| 数据类型 | 关键字 | 	描述 |
| ----------- | ----------- | ----------- |
| 任意类型 | 	any | 	声明为 any 的变量可以赋予任意类型的值。
| 数字类型 | number | 	双精度 64 位浮点值。它可以用来表示整数和分数。支持进制指定，0b二进制，0o八进制，0x十六进制
| 字符串类型 | string | 一个字符系列，使用单引号（'）或双引号（"）来表示字符串类型。反引号（`）来定义多行文本和内嵌表达式。 内嵌用法同JS。
| 布尔类型 | boolean | 	表示逻辑值：true 和 false。达式。
| 数组类型 | 无 | 	声明变量为数组。// 在元素类型后面加上[]，let arr: number[] = [1, 2];   // 或者使用数组泛型  let arr: Array<number> = [1, 2];
| 元组 | 无 | 	元组类型用来表示已知元素数量和类型的数组，各元素的类型不必相同，对应位置的类型需要相同。 let x: [string, number];   x = ['Runoob', 1];    // 运行正常   x = [1, 'Runoob'];    // 报错   console.log(x[0]);    // 输出 Runoob
| 枚举 | enum | 枚举类型用于定义数值集合。enum Color {Red, Green, Blue}; 输出0base整型值
| void | void | 	用于标识方法返回值的类型，表示该方法没有返回值。
| null | null | 	空对象
| undefined | undefined | 	用于初始化变量为一个未定义的值
| never | never | never 是其它类型（包括 null 和 undefined）的子类型，代表从不会出现的值。

3. 变量声明

var [变量名] : [类型] = 值;

**类型断言**

<类型>值

值 as 类型

```
var str = '1' 
var str2:number = <number> <any> str   //str、str2 是 string 类型
console.log(str2)
```

4. 运算符

与c#一致

5. 条件语句

if

if...else

if...else if....else

switch

6. 循环

for 

for...in 循环 数组

 for…of 、forEach、every 和 some 循环

 for...of 允许你遍历 Arrays（数组）, Strings（字符串）, Maps（映射）, Sets（集合）等可迭代的数据结构等。

 while 循环

 do...while 循环

 break 语句

 continue 语句

 无限循环
 for(;;)
 while(true) 


7.  Number 对象

Number 对象是原始数值的包装对象。

```
var num = new Number(value);
```

8. String 对象

String 对象用于处理文本（字符串）。

```
var txt = new String("string");
或者更简单方式：
var txt = "string";
```

9. Array(数组)对象

数组对象是使用单独的变量名来存储一系列的值。
```
var sites:string[]; 
sites = ["Google","Runoob","Taobao"]
```

声明
```
var numlist:number[] = [2,4,6,8]
```

10. Map对象

TypeScript 使用 Map 类型和 new 关键字来创建 Map：

```
let myMap = new Map();
```

初始化 Map，可以以数组的格式来传入键值对：

```
let myMap = new Map([
        ["key1", "value1"],
        ["key2", "value2"]
    ]); 
```

11. 元组


如果存储的元素数据类型不同，则需要使用元组。
声明一个元组并初始化

```
var mytuple = [10,"Runoob"];
```

12. 联合类型

联合类型（Union Types）可以通过管道(|)将变量设置多种类型，赋值时可以根据设置的类型来赋值。

```
Type1|Type2|Type3 
```

**联合类型数组**
```
var arr:number[]|string[]; 
```

13. 接口

接口是一系列抽象方法的声明，是一些方法特征的集合，这些方法都应该是抽象的，需要由具体的类去实现.

```
interface interface_name { 
}
```

**接口继承**

14. 类

TypeScript 是面向对象的 JavaScript。

```
class class_name { 
    // 类作用域
}
```

**instanceof 运算符**

instanceof 运算符用于判断对象是否是指定的类型，如果是返回 true，否则返回 false。

15. 对象

对象是包含一组键值对的实例。  值可以是标量、函数、数组、对象等，如下实例：

```
var object_name = { 
    key1: "value1", // 标量
    key2: "value",  
    key3: function() {
        // 函数
    }, 
    key4:["content1", "content2"] //集合
}
```

16. 命名空间

TypeScript 中命名空间使用 namespace 来定义，语法格式如下：
```
namespace SomeNameSpaceName { 
   export interface ISomeInterfaceName {      }  
   export class SomeClassName {      }  
}
```

**嵌套命名空间**

命名空间支持嵌套，即你可以将命名空间定义在另外一个命名空间里头。

```
namespace namespace_name1 { 
    export namespace namespace_name2 {
        export class class_name {    } 
    } 
}
```

17. 模块

两个模块之间的关系是通过在**文件级别**上使用 import 和 export 建立的。

模块导出使用关键字 export 关键字，语法格式如下：

```
// 文件名 : SomeInterface.ts 
export interface SomeInterface { 
   // 代码部分
}
```
要在另外一个文件使用该模块就需要使用 import 关键字来导入:
```
import someInterfaceRef = require("./SomeInterface");
```
18. 声明文件

