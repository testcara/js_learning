# JavaScript 学习笔记
- [JavaScript 学习笔记](#javascript-学习笔记)
  - [数据类型](#数据类型)
    - [基本数据类型](#基本数据类型)
      - [Number类型数据转换](#number类型数据转换)
        - [Number() 函数](#number-函数)
        - [parseInt()函数](#parseint函数)
        - [parseFloat()函数](#parsefloat函数)
    - [引用数据类型](#引用数据类型)
      - [Object类型及实例和静态函数](#object类型及实例和静态函数)
        - [new操作符](#new操作符)
        - [Object类型的实例函数](#object类型的实例函数)
        - [Object类型的静态函数](#object类型的静态函数)
          - [Object.create()函数](#objectcreate函数)
          - [Object.defineProperties()函数](#objectdefineproperties函数)
          - [Object.getOwnPropertyName()函数](#objectgetownpropertyname函数)
          - [Object.keys()函数](#objectkeys函数)
      - [Array类型](#array类型)
        - [判断一个变量是数据还是对象](#判断一个变量是数据还是对象)
          - [typeof运算符](#typeof运算符)
          - [instanceof运算符](#instanceof运算符)
          - [判断构造函数](#判断构造函数)
          - [Array.isArray()函数](#arrayisarray函数)
        - [filter()函数](#filter函数)
          - [filter简单类型的数组](#filter简单类型的数组)
          - [filter过滤复杂类型的数组](#filter过滤复杂类型的数组)
        - [reduce()函数](#reduce函数)
          - [求数组每个元素相加的和](#求数组每个元素相加的和)
          - [统计数组中每个元素出现的次数](#统计数组中每个元素出现的次数)
          - [多维度统计数据](#多维度统计数据)
        - [数组遍历的7种方法](#数组遍历的7种方法)
          - [for循环](#for循环)
          - [forEach()函数](#foreach函数)
          - [map()函数](#map函数)
          - [some()函数和every()函数](#some函数和every函数)
          - [find()函数](#find函数)
  - [函数](#函数)
    - [三种函数定义方法](#三种函数定义方法)
      - [函数声明](#函数声明)
      - [函数表达式](#函数表达式)
      - [Function构造函数](#function构造函数)
    - [函数表达式的应用场景](#函数表达式的应用场景)
      - [函数递归](#函数递归)
    - [函数的调用](#函数的调用)
      - [函数调用模式](#函数调用模式)
      - [方法调用模式](#方法调用模式)
      - [call()函数、apply()函数调用模式](#call函数apply函数调用模式)
      - [匿名函数调用模式](#匿名函数调用模式)
      - [自执行函数](#自执行函数)
    - [函数参数](#函数参数)
      - [形参与实参](#形参与实参)
      - [arguments对象](#arguments对象)
    - [闭包](#闭包)
      - [执行上下文环境](#执行上下文环境)
      - [闭包的概念](#闭包的概念)
      - [闭包的用途](#闭包的用途)
        - [结果缓存](#结果缓存)
        - [封装](#封装)
        - [练习](#练习)
        - [小结](#小结)
  - [this使用详解](#this使用详解)
    - [this指向对象实例](#this指向对象实例)
    - [this指向call()函数、apply()函数、bind()函数调用后重新绑定的对象](#this指向call函数apply函数bind函数调用后重新绑定的对象)
  - [对象](#对象)
    - [对象的创建](#对象的创建)
      - [new Object](#new-object)
      - [对象字面量](#对象字面量)
      - [工厂模式](#工厂模式)
      - [构造函数](#构造函数)
      - [原型模式](#原型模式)
    - [克隆对象](#克隆对象)
      - [对象浅克隆](#对象浅克隆)
      - [对象深克隆](#对象深克隆)
    - [原型对象、构造函数和实例之间的关系](#原型对象构造函数和实例之间的关系)
  - [html \& jquery](#html--jquery)
    - [html](#html)
      - [a 标签](#a-标签)
      - [table 标签](#table-标签)
      - [表单标签](#表单标签)
      - [css](#css)
    - [jquery](#jquery)
      - [简介](#简介)
    - [css 选择器](#css-选择器)
    - [使用jquery操作dom](#使用jquery操作dom)
      - [查找元素](#查找元素)
      - [添加元素](#添加元素)
      - [删除元素](#删除元素)
      - [隐藏元素](#隐藏元素)
      - [显示隐藏元素](#显示隐藏元素)
      - [操作属性](#操作属性)
      - [内容操作](#内容操作)
  - [ES6](#es6)
    - [全新的变量定义](#全新的变量定义)
    - [解构赋值](#解构赋值)
    - [字符串升级](#字符串升级)
      - [允许字符串通过for循环遍历](#允许字符串通过for循环遍历)
      - [允许用反引号进行一些简化的字符串定义](#允许用反引号进行一些简化的字符串定义)
    - [proxy代理](#proxy代理)
    - [强化后的数组](#强化后的数组)
      - [快速构建新数组](#快速构建新数组)
      - [新的数组方法](#新的数组方法)
      - [数组复制](#数组复制)
    - [强化后的函数](#强化后的函数)
    - [更加灵活多变的对象](#更加灵活多变的对象)
    - [promise对象和async函数](#promise对象和async函数)
      - [promise对象](#promise对象)
      - [async函数](#async函数)
    - [symbol](#symbol)
    - [类](#类)
      - [类的基本语法](#类的基本语法)
      - [静态成员](#静态成员)
      - [类的继承](#类的继承)
    - [模块化module](#模块化module)
    - [set和map集合](#set和map集合)
    - [...](#)
      - [spread](#spread)
      - [rest](#rest)

## 数据类型

### 基本数据类型

Undefined, Null, Boolean, Number, String

- Undefined类型只有一个唯一的字面值undefined，表示的是一个变量不存在。
- Null类型只有一个唯一的字面值null，表示一个空指针对象。
- Boolean类型的字面值只有两个true和false。
- Number类型数据既包括了整型数据，又包括了浮点型数据。
  
```javascript
var str = "hello world!";
var num = 1;
var flag = true;
var a = null;
var b;
```

#### Number类型数据转换

##### Number() 函数

用于将任何类型转化为Number()类型，它在转换时遵循下列规则。

- 数字会按照对丁的进制数据格式，同一转化为十进制并返回。
- Boolean类型的值，true将返回1，false返回0。
- 值为null，则返回0。
- 值为undefined，则返回NaN。
- 值为字符串类型，
  - 若字符串只包含数字，则直接转换成十进制；若数字有0，则会直接忽略这个0。
  - 若字符串是有效的浮点数形式，则会直接转换成对应的浮点数，前置的多个重复的0会被清空，只保留一个。
  - 若字符串是有效的十六进制形式，则会转换成对应的十进制数值。
  - 若字符串是有效的八进制形式，则不会按照八进制转换，而是直接按照十进制转换并输出，前置的0会被直接忽略。
  - 若字符串为空，则字符串不包含任何字符，或为连续过个空格，则会转换为0。
  - 其他，则会返回NaN。
- 值为对象类型，则会先调用对象的valueOf()函数获取返回值，然后按照上述步骤重新能否转化为Number类型。若不能，则会调用对象的toString()函数获取返回值，并将返回值重新按照对象步骤重新尝试转化为Number类型。
若不能，则返回NaN。

##### parseInt()函数

用于解析一个字符串，并返回指定的基数对应的整数值。格式为```parseInt(string, radix)```  。string表示要被解析的值，如过该参数不是一个字符串，那么会使用toString()函数将其转换成字符串，而字符串前面的空白符会被忽略。radix表示的是进制转换的技术，数据范围时2-36，默认是10。parseInt()函数在做转换时，对于传入的字符串会采用前置匹配的原则，即仅转换第一个满足要求的字符，后面的字符均舍弃。

```javascript
console.log(0.1 + 0.2); // 0.30000000000000004 精度丢失问题
console.log(2.0013 * 1000); //2001.3000000000002 精度丢失问题

function add(a, b) {
  let needAdjust = false;
  let aS = a.toString();
  let bS = b.toString();

  // 整数不需要调整
  if (aS.indexOf(".") < 0 && bS.indexOf(".") < 0) {
    return a + b;
  } else {
    needAdjust = true;
  }
  // 浮点数，当小数点后位数多余2位时为出现精度问题。需要调整。
  // 调整策略为： 补齐为整数，在除以调整倍数。
  if (needAdjust) {
    // 求最多补零数
    let length = [aS, bS].reduce(function (acc, currentValue) {
      currentValue.indexOf(".") > 0
        ? (acc = Math.max(acc, currentValue.split(".")[1].length))
        : 0;
      return acc;
    }, 0);
    // 去掉小数点后，根据实际情况，补0。
    let [asNew, bsNew] = [aS, bS].map(function (currentValue, currentIndex) {
      return currentValue.indexOf(".") > 0
        ? currentValue.replace(".", "") +
            "0".repeat(length - currentValue.split(".")[1].length)
        : currentValue + "0".repeat(length);
    });
    return (parseInt(asNew) + parseInt(bsNew)) / Math.pow(10, length);
  }
}
console.log(add(0.1, 0.2));
console.log(add(0.01, 2.002));
console.log(add(1.00001, 2.002));
console.log(add(1, 1));
console.log(add(1, 0.01));
```

##### parseFloat()函数

没有进制概念。在解析过程中，遇到正负号（只能出现在首位且不能连续出现），数字0-9，小数点或者科学计数法（e/E）以外的字符，则会忽略从该字符开始至结束的所有字符，然后返回当前已经解析的字符的浮点数形式。

### 引用数据类型

Object，Function，Data, Array等都是引用数据类型。引用数据类型描述的是具有属性和函数的对象。
引用数据类型不同于基本数据类型的特点有：

- 引用数据类型的实例需要通过new操作符生成。
- 引用数据类型的值是可变的。
- 引用数据类型变量赋值传递的是内存地址。

#### Object类型及实例和静态函数

##### new操作符

new操作符在执行过程中会改变this的指向。而在javascript中，如果函数没有return值，则默认return this。

```javascript
function Cat(name, age) {
  console.log(this)
  this.name = name;
  this.age = age;
}
console.log(new Cat('mimi', 7))

console.log('---------')
function Cat1(name, age) {
  console.log(this)
  var Cat = {};
  console.log(typeof Cat);
  Cat.name = name;
  Cat.age = age;
}
console.log(new Cat1('mimi', 7))

console.log('---------')
function Cat2(name, age) {
  console.log(this);
  var Cat = {};
  Cat.name = name;
  Cat.age = age;
  return Cat
}
console.log(new Cat2('mimi', 7))
```

输出为：

```javascript
Cat {}
Cat { name: 'mimi', age: 7 }
---------
Cat1 {}
object
Cat1 {}
---------
Cat2 {}
{ name: 'mimi', age: 7 }
```

##### Object类型的实例函数

实例函数是指函数的调用是基于Object类型的实例的。

- hasOwnProperty函数
该实例函数用于判断对象自身是否拥有指定名称的实例属性，此函数不会检查实例对象原型链上的属性。

```javascript
var o = new Object()
o.name = '自定义属性'
console.log(o.hasOwnProperty('name')); // true
console.log(o.hasOwnProperty('toString')); // false

var Student = function(name){
  this.name = name;
}
// 给Student原型添加一个sayHello()函数
Student.prototype.sayHello = function(){
  alert('hello'+this.name);
}
// 给Student原型添加一个age属性
Student.prototype.age = '';
var st = new Student('张三');
console.log(st.hasOwnProperty('name')); // true
console.log(st.hasOwnProperty('sayHello')); // false
console.log(st.hasOwnProperty('age')); // false
```

##### Object类型的静态函数

静态函数指的是方法的调用基于Oject类型自身，不需要通过Object类型的实例。

###### Object.create()函数

该函数的主要作用是创建并返回一个指定原型和指定属性的对象。

```javascript
var obj = Object.create(null, {
  name: {
    value: 'tom',
    writeable: true, // 属性值可改
    enumerable: true, // 它决定了对象的属性是否能够通过某些遍历方法被访问到
    configurable: true // 可删除、添加属性
  },
  age: {
    value: 22
  }
})

console.log(obj.name) // tom
console.log(obj.age) // 22
obj.age = 28;
console.log(obj.age); // 22 age属性的writeable默认为false
for (var p in obj){
  console.log(p) // 只输出name属性； age属性的enumerable默认为
  // false, 不能通过for...in枚举。
}
```

###### Object.defineProperties()函数

该函数的添加或修改对象的属性值。

```javascript
var obj = {};
Object.defineProperties(obj, {
  name: {
    value: "tom",
    enumerable: true,
  },
  age: {
    value: 22,
    enumerable: true,
    writable: true,
  },
});
for (var p in obj) {
  console.log(p); // name age: 输出name & age属性
}
obj.age = 23; // 23
```

###### Object.getOwnPropertyName()函数

获取对象的所有实例属性和函数，不包含原型链继承的属性和函数，数据格式为数组。

```javascript
function Person(name, age, gender) {
  this.name = name;
  this.age = age;
  this.gender = gender;
  this.getName = function () {
    return this.name;
  };
}

// 在Person对象的原型链上添加一个eat函数
Person.prototype.eat = function () {
  return "eat";
};

var p = new Person();
// for...in 循环遍历对象 p 的属性时，实际上是在枚举该对象的
// 所有可枚举属性(包括原型链上继承的)
for (var item in p) {
  console.log(item);
} // name, age, gender, getName, eat
for (var item in p) {
  // 判断是否是自己的属性而不是继承的
  if (p.hasOwnProperty(item)) {
    console.log(item);
  }
} // name, age, gender, getName, eat
// 输出所有自己的属性（无论是否可枚举），不包含原型链上继承的可枚举属性
console.log(Object.getOwnPropertyNames(p)); // [ 'name', 'age', 'gender', 'getName' ]
```

###### Object.keys()函数

获取对象可枚举的实例属性，不包含原链条继承的属性，数据格式为数组。

```javascript
var obj = {
  name: "tom",
  age: 22,
  sayHello: function () {
    alert("hello" + this.name);
  },
};
console.log(Object.keys(obj)); // [ 'name', 'age', 'sayHello' ]
console.log(Object.getOwnPropertyNames(obj)); // [ 'name', 'age', 'sayHello' ]
Object.defineProperty(obj, "name", { enumerable: false });
console.log(Object.keys(obj)); // [ 'age', 'sayHello' ]
console.log(Object.getOwnPropertyNames(obj)); // [ 'name', 'age', 'sayHello' ]
```

#### Array类型

Array类型提供了丰富的函数用于对数组进行处理，例如过滤、去重、遍历等。

##### 判断一个变量是数据还是对象

###### typeof运算符

typeof运算符在判断基本数据类型是会很有用，但是在判断引用数据类型时，总是返回object。

```javascript
var a = [1, 2, 3, 4];
console.log(typeof a); // object
```

###### instanceof运算符

instanceof运算符用于查找原型链来检测某个变量是否为某个类型数据的实例。

```javascript
var a = [1, 2, 3, 4];
console.log(a instanceof Array); // true
console.log(a instanceof Object); // true

var b = { name: "kingx" };
console.log(b instanceof Array); // false
console.log(b instanceof Object); // true

var a = [1, 2, 3, 4];

function getDataType(o) {
  if (o instanceof Array) {
    return Array;
  } else if (o instanceof Object) {
    return Object;
  } else {
    return "param is not object type";
  }
}

console.log(getDataType(a)); // [Function: Array]
```

###### 判断构造函数

判断一个变量是数组还是对象，其实就是判断变量的构造函数是Array类型还是Object类型。

```javascript
var a = [1, 2, 3];
console.log(a.constructor === Array); // true
console.log(a.constructor === Object); // false

var b = { name: "kingx" };
console.log(b.constructor === Array); // false
console.log(b.constructor === Object); // true
```

###### Array.isArray()函数

从javascript 1.8.5 版本中， 增加了isArray()静态函数，用于判断变量是否为数组。

```javascript
// true
Array.isArray([]);
Array.isArray([1]);
Array.isArray(new Array());
Array.isArray(Array.prototype);

// false
Array.isArray();
Array.isArray({});
Array.isArray(null);
Array.isArray(undefined);
Array.isArray(17);
Array.isArray("Array");
Array.isArray(true);
```

##### filter()函数

用于过滤满足条件的数组，返回一个新数组，而不会改变原数组。
filter()函数接收一个函数作为参数，返回值为true的元素会被添加到新的数组中，返回值为false的元素
则不会被添加，最后返回这个新数组，如果没有符合条件的值则返回空数组。

###### filter简单类型的数组

```javascript
// 过滤奇数
var filterFn = function (x) {
  return x % 2; // 0 为false, 其他为true
};
console.log([1, 4, 5, 9].filter(filterFn)); // [ 1, 5, 9 ]
```

###### filter过滤复杂类型的数组

```javascript
var arrObj = [
  {
    name: "a",
    age: 10,
    gender: "female",
  },
  {
    name: "b",
    age: 18,
    gender: "male",
  },
];

var filterFn1 = function (o) {
  if (o instanceof Object) {
    return o.age >= 18 && o.gender === "male";
  } else {
    return false;
  }
};

console.log(arrObj.filter(filterFn1)); // [ { name: 'b', age: 18, gender: 'male' } ]
console.log([].filter(filterFn1)); // []
```

##### reduce()函数

最主要的作用是做累加处理，即接收一个函数作为累加器，将数组中每一个元素从左到右依次执行累加器，返回最终的处理结果。
函数语法如下：

```javascript
arr.reduce(callback(accumulator, currentValue, currentIndex, array),initialValue)
```

- accumulator表示上一次调用累加器的返回值，第一次的值为initialValue或者数组的第一个元素值。
- currentValue表示数组正在处理的值。
- currentIndex表示正在处理值的索引，如果设置了initalValue，则currentIndex从0开始，否则从1开始。
- array表示数组本身。

###### 求数组每个元素相加的和

```javascript
var a = [1, 7, 8, 3, 6];
a.reduce(function (acc, currentValue, currentIndex, array) {
  console.log(
    "index:" + currentIndex + ", currentValue:" + currentValue + ", acc:" + acc
  );
  return acc + currentValue;
}, 0); 
console.log(result);
```

输出为:

```log
index:0, currentValue:1, acc:0
index:1, currentValue:7, acc:1
index:2, currentValue:8, acc:8
index:3, currentValue:3, acc:16
index:4, currentValue:6, acc:19
25
```

###### 统计数组中每个元素出现的次数

```javascript
var a = [1, 2, 3, 2, 2, 5, 1];
var result = a.reduce(function (acc, currentValue, currentIndex, array) {
  acc[currentValue] ? acc[currentValue]++ : (acc[currentValue] = 1);
  return acc;
}, {}); // 初始化acc为{}
console.log(result); // { '1': 2, '2': 3, '3': 1, '5': 1 }
```

###### 多维度统计数据

- 同时求人民币兑换美元和欧元的值

```javascript
var items = [{ price: 10 }, { price: 50 }, { price: 100 }];
// 计算这些值对应的美元值和欧元值，对应的汇率为1：0.14，1:0.13
var reducerFn1 = items.reduce(function (acc, currentValue) {
  acc += currentValue.price * 0.1487;
  return acc;
}, 0);
console.log(reducerFn1);
var reducerFn2 = items.reduce(function (acc, currentValue) {
  acc += currentValue.price * 0.1265;
  return acc;
}, 0);
console.log(reducerFn2);
// 将两个函数合并为一个函数

var initialState = { euros: 0, dollars: 0 };
var result = items.reduce(function (acc, currentValue) {
  acc.euros += currentValue.price * 0.1265;
  acc.dollars += currentValue.price * 0.1487;
  return acc;
}, initialState);
console.log(result); // { euros: 20.240000000000002, dollars: 23.792 }
```

- 同时求数组的最大值和最小值

```javascript
var items = [2, 4, 10, 7, 5, 8, 6];
var result = items.reduce(
  function (acc, currentValue, currentIndex, array) {
    // init the original acc
    if (currentIndex === 0 && array.length > 0) {
      acc = { min: array[0], max: array[0] };
    }
    acc.min > currentValue ? (acc.min = currentValue) : (acc.min = acc.min);
    acc.max < currentValue ? (acc.max = currentValue) : (acc.max = acc.max);
    return acc;
  },
  { min: 0, max: 0 }
);
console.log(result); // { min: 2, max: 10 }
```

##### 数组遍历的7种方法

###### for循环

```javascript
var arr1 = [11, 22, 33];
for (var i = 0; i < arr1.length; i++) {
  console.log(arr1[i]);
}
```

###### forEach()函数

forEach函数接收一个回调函数，参数分别表示当前执行的元素值、当前值的索引和数组本身。

```javascript
var arr1 = [11, 22, 33];
arr1.forEach(function (currentValue, currentIndex, array) {
  console.log(currentValue);
});
```

###### map()函数

用于在数组遍历的过程中，将数组中的每个数据进行处理，得到新的数据，并返回一个新的数组。map()函数接收的函数和forEach()函数一样。后面讲到的some()，every()，find()函数与map()函数的接收函数都一样。

```javascript
var arr1 = [11, 22, 33];
var result1 = arr1.map(function (currentValue, currentIndex, array) {
  return currentValue * currentValue; // 无论是forEach和map，都必须return
});
console.log(result1); // [ 121, 484, 1089 ]
```

###### some()函数和every()函数

这俩函数相似之处在于都用于数组遍历的过程中，判断数组是否有满足条件的元素，满足返回true,不满足返回false。两者的区别是some()函数是只要数组中某个元素满足条件就返回true，不会对后续元素进行判断。而every()函数是数组中每个元素都满足条件才返回true。

```javascript
var items = [1, 2, 3, 4, 5, 6];
function isBig(currentValue, currentIndex, array) {
  return currentValue > 4;
}
console.log(items.some(isBig)); // true
console.log(items.every(isBig)); // false
```

###### find()函数

用于数组遍历的过程中，找到第一个满足条件的元素值，则直接返回该元素值，如果都不满足条件，则返回undefined。

```javascript
var items = [1, 2, 3, 4, 5, 6];
function isBig(currentValue, currentIndex, array) {
  return currentValue > 4;
}
console.log(items.find(isBig)); // 5
```

## 函数

### 三种函数定义方法

#### 函数声明

函数声明是直接使用function关键字接一个函数名，函数名后是接收函数的形参。

```javascript
function sum(num1, num2) {
    return num1 + num2
}
```

#### 函数表达式

类似于普通变量的初始化，只不过初始化的值为一个函数。

```javascript
var sum = function (num1, num2) {
  return num1 + num2;
};
```

这个函数表达式没有名称，属于匿名函数表达式。匿名函数表达式和函数声明都可以直接通过函数名或者变量名访问。

```javascript
var sum = function foo(num1, num2) {
  return num1 + num2;
};
```

这个函数为有名的函数表达式，但是foo这个名字不能在外部使用，而仅是函数内部的一个变量。

#### Function构造函数

使用new操作符，调用Function()构造函数，传入对应的参数，也可以定义函数。

```javascript
var add = new Function("a", "b", "return a+b");
```

这种方法很少使用，因为效率低，且不遵循典型的作用域，它将一直作为顶级函数执行，从而导致访问变量有问题。

### 函数表达式的应用场景

#### 函数递归

通过函数表达式可以定义具有名称的函数，它作为函数内部的一个局部变量，指向函数自身，从而实现递归。

```javascript
var fibonacci = function fn(num) {
  if (num === 1 || num === 2) {
    return 1;
  }
  return fn(num - 2) + fn(num - 1);
};
console.log(fibonacci(1), fibonacci(2), fibonacci(3), fibonacci(4));
```

### 函数的调用

函数的调用存在5种模式，分别是函数调用模式，方法调用模式，构造器调用模式，call()函数，apply()函数调用模式，匿名函数调用模式。

#### 函数调用模式

```javascript
// 函数声明
function add(a1, a2) {
  return a1 + a2;
}

// 函数表达式
var sub = function (a1, a2) {
  return a1 - a2;
};

add(1, 2);
sub(1, 3);
```

#### 方法调用模式

方法属于对象，所以需要先定义一个对象，然后定义方法属性。

```javascript
// 定义对象
var obj = {
  name: "cara",
  getName: function () {
    return this.name;
  },
  setName: function (newName) {
    this.name = newName;
  },
};
// 调用对象方法
console.log(obj.getName());
obj.setName("wlin");
console.log(obj.getName());
```

#### call()函数、apply()函数调用模式

通过call()和apply()函数可以改变函数执行的主体，使得某些不具有特定函数的对象可以直接调用该特定函数。

``` javascript
// 不传参数时
function greeting() {
  // 反引号（``）是用来定义模板字符串
  console.log(`hi, ${this.name}`);
}

const person = {
  name: "cara",
};
// 通过call方法，我们将greet函数中的this值设置为person对象
greeting.call(person); // hi, cara

// 传参数时
function introduce(greeting, others) {
  console.log(`${greeting}, my name is ${this.name} and ${others}`);
}

introduce.call(person, "hi", "i am 18 years old."); // hi, my name is cara and i am 18 years old

// call参数是一个个传值，apply是传入数组
var greetings = ["hi", "i am 18 years old"];
introduce.apply(person, greetings); // hi, my name is cara and i am 18 years old
```

#### 匿名函数调用模式

匿名函数的调用有两种方式，一种是通过函数表达式定义函数，并赋给变量，通过变量进行调用。另一种是使用小括号()将米名函数括起来，然后在后面使用小括号（）传递对应的参数，进行调用。

```javascript
(function (num1, num2) {
  console.log(num1 + num2);
})(1, 2); //小括号表示会立即调用
```

#### 自执行函数

自执行函数即函数定义和函数调用的行为先后连续产生。它需要以一个函数表达式的身份进行函数调用，上面的匿名函数调用也属于自执行函数的一种。
自执行函数虽然会被立即执行，但是只会被执行一次。

```javascript
(function () {
  console.log("done");
})();
```

自执行函数一般可以和闭包配合使用，比如：

```javascript
var inner = (function () {
  var a = 0;
  return function (increment) {
    a = a + increment;
    console.log(a);
  };
})();
inner(2);
inner(2);
inner(2);
```

这样我们可以直接得到闭包环境下的内部函数了，外部函数只是为了产生闭包环境而临时定义的函数。
正因为如此，所以根本没必要给外部函数取一个名字。

### 函数参数

#### 形参与实参

函数定义的形式参数，实参是调用函数时传递给函数的参数。实参可以是常量、变量、表达式、函数等类型。

#### arguments对象

arguments对象是所有函数都具有的一个内置局部变量，表示的是函数实际接收的参数，时一个类数组结构（只具有length属性，不具有其他数组的属性）。arguments对象只能在本函数内部访问。
其可以用来判断实参个数，任意个数的参数处理。

### 闭包

正常情况下，定义了一个函数就会产生一个函数的作用域，在函数体中的局部变量会在这个函数作用域中使用。一旦函数执行完成，存在于函数体中局部变量同样会被回收，回收后就不会访问到。如果还想访问该局部变量就需要用到闭包。

#### 执行上下文环境

```javascript
var a = 10; // 1. 进入全局上下文
var fn = function (x) {
  var c = 10;
  console.log(c + x);
};

var bar = function (y) {
  var b = 5;
  fn(y + b); // 3. 进入fn()函数执行上下文环境
};

bar(20); // 2. 进入bar()函数执行上下文环境
```

刚改代码段执行时， 首先进入1，然后进入2，然后进入3，fn()函数执行完成后，销毁3的上下文，然后销毁2的上下文，最后销毁1的上下文。

#### 闭包的概念

在javascript中存在一种内部函数，即函数声明和函数表达式位于另一个函数的函数体内。内部函数可以访问外部函数声明的变量，当这个内部函数在除该外部函数之外被调用时，就会形成闭包。

```javascript
function fn() {
  // 外部函数fn
  var max = 10;
  // 内部函数bar
  return function bar(x) {
    // 引用了外部函数的变量
    if (x > max) {
      console.log(x);
    }
  };
}

var f1 = fn(); // 返回函数bar, fn()执行完毕了，但是max还能被访问
f1(11); // 11
```

没有闭包的时候，函数体执行完，变量就都释放了，但是存在闭包的时候，就不能释放，必须等到返回的函数执行完才能释放，所有就会消耗更多的内存。

#### 闭包的用途

##### 结果缓存

如果一个处理很耗时的函数对象，每次调用都消耗很长时间，我们可以将结果存在内存的缓存中。这样在执行代码时，如果内存中有，就直接返回。如果内存没有，则调用函数进行计算，更新缓存并返回结果。

```javascript
// cachedBox 为立即执行匿名函数返回的函数对象
// 当开始执行时，会被放入全局上下文中
var cachedBox = (function () {
  // 缓存的容器
  var cache = {};
  return {
    // 可以通过searchBox()来访问该匿名函数
    searchBox: function (id) {
      // 如果在内存中，则直接返回
      if (id in cache) {
        return "查找的结果为：" + cache[id];
      }
      var result = dealFn(id);
      cache[id] = result;
      return "计算的结果为：" + result;
    },
  };
})();

function dealFn(id) {
  console.log("这是一段很耗时的操作");
  return id;
}

console.log(cachedBox.searchBox(1)); // 计算结果
console.log(cachedBox.searchBox(1)); // 查到的结果
```

##### 封装

模块化思想希望将具有一定特征的属性封装在一起，只需要对外暴露对应的函数，并不需要关心内部逻辑的实现。

例如，借助数组实现一个栈，只对外暴露出表示入栈和出栈的push()函数和pop()函数，以及表示栈长度的size函数。

```javascript
// stack现在为一个有push,pop,size的函数属性的对象
var stack = (function () {
  var arr = [];
  return {
    push: function (value) {
      arr.push(value);
    },
    pop: function () {
      arr.pop();
    },
    size: function () {
      return arr.length;
    },
    items: function () {
      return arr;
    },
  };
})();
stack.push("abc"); // 入栈
stack.push("def");
console.log(stack.size()); // 2
stack.pop(); // 后入先出
console.log(stack.items()); // ["abc"]
console.log(stack.size()); // 1
```

##### 练习

- 定时器功能

```javascript
// output one, two, three each 1000s
var arr = ["one", "two", "three"];
for (var i = 0; i < arr.length; i++) {
  setTimeout(function () {
    // setTimeout和for是两个上下文，setTimeout不认识arr
    console.log(arr[i]);
  }, i * 1000);
} // undefined

for (var i = 0; i < arr.length; i++) {
  (function (interalI) {
    setTimeout(function () {
      console.log(interalI);
      console.log(arr[interalI]);
    }, interalI * 1000);
  })(i); // 立即执行函数将索引i作为参数传入，使得setTimeout与for同一个上下文
} // one two three
```

##### 小结

闭包如果使用合理，在一定程度上提高代码执行效率，如果使用不合理，则会造成内存浪费，性能下降。

优点：

- 保护函数内变量的安全，实现封装，防止变量流入其他环境发生命名冲突，造成环境污染。
- 在适当的时候，可以在内存中维护变量并缓存，提高执行效率。
  
缺点：

- 消耗内存
- 可能泄漏内存

## this使用详解

在javascript中，this指向的永远是函数的调用者。

### this指向对象实例

```javascript
var value = 10; //全局变量

var obj = {
  value: 100,
  method: function () {
    var foo = function () {
      console.log(this.value); 
      //console.log(this);
    };
    foo(); // 没有所属对象
    return this.value;
  },
};
console.log(obj.method()); // 100
```

### this指向call()函数、apply()函数、bind()函数调用后重新绑定的对象

```javascript
var value = 10;
var obj = {
  value: 20,
};

var method = function () {
  console.log(this.value);
};
method();

method.call(obj); //20
method.apply(obj); //20

var newMethod = method.bind(obj); // call 总是立即执行
newMethod(); //20 bind在新方法被调用的时候执行
```

## 对象

### 对象的创建

对象是一组无序属性的集合，其属性值可以包含基本属性的集合，其属性值可以包含基本类型值，对象或者函数等。

#### new Object

创建对象的最简单的方式就是创建一个object的实例，然后在为他添加属性和方法。

```javascript
var person = new Object();
person.name = "cara";
person.age = 29;
person.job = "software engineer";

person.sayName = function () {
  alert(this.name);
};
```

#### 对象字面量

后来，对象字面量成为创建这种对象的首选模式。

```javascript
var person = {
  name: "Nicholas",
  age: 29,
  job: "software engineer",
  sayName: function () {
    alert(this.name);
  },
};

```

虽然利用object构造函数或对象字面量都可以用来创造单个对象，但这些方式有个明显的缺点：使用同一个接口创建很多对象，就会产生很多重复代码。

#### 工厂模式

为解决这一个问题，人们开始使用工厂模式创建对象。

```javascript
function createPerson(name, age, job) {
  var o = new Object();
  o.name = name;
  o.age = age;
  o.job = job;
  o.sayName = function () {
    alert(this.name);
  };
  return o;
}

var person1 = createPerson("Nicholas", "29", "software engineer");
var person2 = createPerson("Cara", "20", "QE");
```

工厂模式虽然解决了创建多个相似对象的问题，但却没有解决对象识别的问题（这里所有的对象都是object)。

#### 构造函数

构造函数模式解决了这个问题。

```javascript
function Person(name, age, job) {
  this.name = name;
  this.age = age;
  this.job = job;
  this.sayName = function () {
    alert(this.name);
  };
}

var person1 = new Person("Nicholas", "29", "software engineer");
var person2 = new Person("Cara", "20", "QE");

console.log(person1.constructor); // [Function: Person]
console.log(person1 instanceof Person); // true
console.log(person1.sayName); // [Function (anonymous)]
console.log(person1.sayName === person2.sayName); // false 不同实例上的同名函数是不相等的
```

构造函数模式没有显示的创建对象，直接将属性和方法给了this对象，没有return语句。
要创建实例，必须使用new操作符，以这种方式调用构造函数实际上经历了一下四步：

- 创建一个新对象
- 将构造函数的作用域赋给新对象（this指向了新对象）
- 执行构造函数中的代码
- 返回新对象
对象的constructor属性最初是用来标识对象类型的。但是提到检测对象类型，还是instanceof操作符要更可靠一些。

构造函数并非没有缺点，使用构造函数的主要问题是每个方法都要在每个实例上重新创建一遍。然而，创建两个完成同样任务的Function实例完全没有必要，因此，可以将函数定义转移到构造函数外部来解决这个问题。

```javascript
function Person(name, age, job) {
  this.name = name;
  this.age = age;
  this.job = job;
}

function sayName() {
  console.log(this.name);
}
var person1 = new Person("Nicholas", "29", "software engineer");
sayName.call(person1); // Nicholas
var person2 = new Person("Cara", "20", "QE");
sayName.call(person2); // Cara
```

然而，这样实现的话，如果对象需要定义很多方法，那么就需要定义很多全局函数，就丝毫没有封装性可言了。好在，这些问题都可以通过使用原型模式来解决。

#### 原型模式

我们创建的每个函数都有一个prototype(原型)属性，这个属性是一个指针，指向一个对象，而这个对象的用途是包含可以由特定类型的所有实例共享的属性和方法。

```javascript
function Person() {}
Person.prototype.name = "cara";
Person.prototype.age = 18;
Person.prototype.job = "Software Engineer";
Person.prototype.sayName = function () {
  console.log(this.name);
};
var person1 = new Person();
var person2 = new Person();
console.log(person1.sayName === person2.sayName); // true
```

这样，sayName()方法就为共享的方法了。

要理解原型模式的工作原理，必须先了解原型对象。
无论什么时候，只要创建了一个新函数，就会根据一组特定的规则为该函数创建一个prototype属性，这个属性指向函数的原型对象。在默认情况下，所有原型对象都会自动获得一个constructor属性，这个属性是一个指向prototype属性所在函数的指针。

### 克隆对象

#### 对象浅克隆

浅克隆由于只克隆对象最外层的属性，如果对象存在更深层的属性，则不进行处理，这就回导致克隆对象和原始对戏那个的深层属性仍然指向同一块内存。

- 简单的引用复制
简单的引用复制，即遍历对象最外层的所有属性，直接将属性值复制到另一个变量中。

```javascript
function shallowClone(origin) {
  var result = {};
  for (var key in origin) {
    if (origin.hasOwnProperty(key)) {
      result[key] = origin[key];
    }
  }
  return result;
}

var origin = {
  a: 1,
  b: [2, 3, 4],
  c: { d: "name" },
};

var result = shallowClone(origin);
console.log(result); // { a: 1, b: [ 2, 3, 4 ], c: { d: 'name' } }
console.log(origin); // { a: 1, b: [ 2, 3, 4 ], c: { d: 'name' } }

result.a = 2;
result.b.push(5);
result.c.d = "cara";
console.log(origin); // { a: 1, b: [ 2, 3, 4, 5 ], c: { d: 'cara' } }
console.log(result); // { a: 2, b: [ 2, 3, 4, 5 ], c: { d: 'cara' } }
```  

我们发现，当属性值为引用数据类型时，则对克隆对象的值的修改会影响到原始对象的值。

#### 对象深克隆

- json序列化和反序列化
如果一个对象中的全部属性都是可以序列化的，那么我们可以先试用json.stringify()函数将原始对象序列化为字符串，再使用json.parse()函数将字符串反序列化为一个对象，这样得到的对象就是深克隆的对象。

```javascript
var origin = {
  a: 1,
  b: [2, 3, 4],
  c: { d: "name" },
};

// 先反序列化为字符串，再序列化为对象，得到深克隆后的对象
var result = JSON.parse(JSON.stringify(origin));

console.log(origin); // { a: 1, b: [ 2, 3, 4 ], c: { d: 'name' } }
console.log(result); // { a: 1, b: [ 2, 3, 4 ], c: { d: 'name' } }

result.a = 3;
result.b.pop();
result.c.d = "cara";

console.log(origin); // { a: 1, b: [ 2, 3, 4 ], c: { d: 'name' } }
console.log(result); // { a: 3, b: [ 2, 3 ], c: { d: 'cara' } }
```

但是，当属性值为函数、正则表达式、对象实例时，则这种方法就不能完全实现对象的深克隆。
这个时候我们可以遍历这些对象，依次实现深处理。

- 自定义深克隆

```javascript
function Animal(name) {
  this.name = name;
}

var animal = new Animal("tom");

// 原始对象
var origin = {
  // 属性为函数
  a: function () {
    return "a";
  },
  // 属性为正则表达式
  b: new RegExp("d", "g"),
  c: animal,
};

var result = JSON.parse(JSON.stringify(origin));

console.log(origin); // { a: [Function: a], b: /d/g, c: Animal { name: 'tom' } }
console.log(result); // { b: {}, c: { name: 'tom' } }
```

值为function类型的a属性丢失，b属性应该为一个正则表达式，在克隆后为一个空对象，c属性对象的构造函数不再指向Animal, 而是指向Object，构造函数被丢失，导致原型链关系的断裂。

这时候我们可以写一个递归函数，来实现深层次的递归，来实现原始对象和克隆对象之间没有共享应用且没有丢失。

```javascript
function deepClone(obj, hash = new WeakMap()) {
    // 处理null、undefined、原始类型和函数（不克隆函数）
    if (obj === null || typeof obj !== 'object') {
        return obj;
    }

    // 处理循环引用
    if (hash.has(obj)) {
        return hash.get(obj);
    }

    // 处理Date对象
    if (obj instanceof Date) {
        return new Date(obj);
    }

    // 处理Array
    if (Array.isArray(obj)) {
        let clone = [];
        hash.set(obj, clone);
        for (let i = 0; i < obj.length; i++) {
            clone[i] = deepClone(obj[i], hash);
        }
        return clone;
    }

    // 处理RegExp对象（可选：可以选择不克隆RegExp）
    if (obj instanceof RegExp) {
        return new RegExp(obj);
    }

    // 处理其他对象类型（包括Map、Set等，需要额外处理）
    let clone = {};
    hash.set(obj, clone);
    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            clone[key] = deepClone(obj[key], hash);
        }
    }

    // 处理Map和Set（如果需要克隆这些集合类型）
    if (obj instanceof Map) {
        let mapClone = new Map();
        hash.set(obj, mapClone);
        obj.forEach((value, key) => {
            mapClone.set(deepClone(key, hash), deepClone(value, hash));
        });
        return mapClone;
    }

    if (obj instanceof Set) {
        let setClone = new Set();
        hash.set(obj, setClone);
        obj.forEach(value => {
            setClone.add(deepClone(value, hash));
        });
        return setClone;
    }

    // 对于其他类型的对象，如WeakMap和WeakSet，由于它们的键不能是原始值，
    // 因此通常不会进行深克隆（或者它们的使用场景不适合深克隆）。

    return clone;
}
```

### 原型对象、构造函数和实例之间的关系

每一个函数在创建时都会被赋予一个prototype属性。在默认情况下，所有的原型对象都会增加一个constructor属性，指向prototype属性所在的函数，即构造函数。
当我们通过new操作符调用构造函数创建一个实例时，实例具有一个__proto__属性，指向构造函数的原型对象。因此__proto__属性可以看作是一个连接实例与构造函数的原型对象的桥梁。
]

## html & jquery

### html

#### a 标签
  
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>a链接的使用教程</title>
	</head>
	<body>
		<a target="_blank" id='a01' title="123" href="01.html">baidu</a></br>
		<a class="c1" id="a02" href="1.zip">下载好资源</a>
		<a style="background: deeppink;color: white;" id="a03" href="mp3/1.mp3">下载音乐</a>
	</body>
</html>
```

#### table 标签

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>表格</title>
	</head>
	<body>
		<table width='800' align="center" border='1' cellspacing='0' cellpadding='10'>
			<tr><td colspan='7'></td></tr>
			<tr>
				<td>2</td>
				<td>3</td>
				<td><img src="images/IMG_8888.JPG"></td>
			</tr>
		</table>

	</body>
</html>
```

#### 表单标签

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>表单</title>
	</head>
	<body>
		<form action='login.php' method="GET">
			<table border="1" cellpadding='10' >
				<tr>
					<td>请输入用户名：</td>
					<td><input value="jack" type="text" name="username"></td>
				</tr>
				<tr>
					<td>请输入密码：</td>
					<td><input value="123" type="password" name="password"></td>
				</tr>
				<tr>
					<td>请输入个人介绍：</td>
					<td><textarea name='description' rows='10' clos='50'></textarea></td>
				</tr>
				<tr>
					<td>请输入您的爱好：</td>
					<td>
						<label>
							<input type="checkbox" name="hobby" value="finishing">钓鱼
						</label>
						<label>
							<input type="checkbox" name="hobby" value="lol">王者荣耀
						</label>
					</td>
				</tr>
				<tr>
					<td>请输入您的性别：</td>
					<td>
						<label>
							<input type="radio" name="gender" value="1"/>男
							<input type="radio" name="gender" value="2"/>女
							<input type="radio" name="gender" value="3"/>保密
						</label>
					</td>
				</tr>
				<tr>
					<td>
						请选择收货地址：
					</td>
					<td>
						<select name="province">
							<option>---请选择省份---</option>
							<option value="1">江苏省</option>
							<option value="2">河南省</option>
						</select>
						<br>
						<select name="city">
							<option>---请选择城市---</option>
							<option value="1">北京</option>
							<option value="2">上海</option>
							<option value="3">广州</option>
						</select>
						<br>
						<select name="area">
							<option>---请选择区---</option>
							<option value="1">大兴</option>
							<option value="2">海淀</option>
							<option value="3">昌平</option>
						</select>
						<br><br>
						具体街道和门牌号：
						<textarea name="address" rows="1" cols="50"></textarea>
					</td>
				</tr>
				<tr align="right">
					<td colspan="2">
						<input type="submit" value="保存">
					</td>
				</tr>
			</table>
		</form>

	</body>
</html>
```

#### css

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>css</title>
		<style>
			/* 在这里统一设置模式
			也可以将一下内容写入style.css
			然后替换此style然后引入<link rel="stylesheet" href="styles.css">
			*/
			.line {font-size: 20px; color: orange;}
			#title {color: blue; font-weight: 600;}
		</style>
	</head>
	<body>
		<h1 id="title">静夜思</h1>
		<p class="line">窗前明月光</p>
		<p class="line">疑是地上霜</p>
		<p class="line">举头望明月</p>
		<p class="line">低头思故乡</p>

	</body>
</html>
```

### jquery

#### 简介

jquery是一个快速、简洁的javascript框架。jqery的设计宗旨是"write less, do more"。jquery封装了javascript常用的功能代码，提供了简便的javascript api，优化了html文档操作、事件处理、动画设计和ajax交互。
为什么要用jquery呢？举例你用input画了一个按钮，当用户单击这个按钮需要发生交互。你要操作某一个html标签，在某一个时刻变化颜色。这些都需要编写javascript先获取这个元素，然后进行处理。
javascript获取元素代码如下：

```javascript
document.getElementById("id")
```

而使用jquery则为：

```jquery
$('#id')
```

jquery提供了大量的方法，可以非常方便的操作dom元素。jquery的选择机制构建于css的选择器，它提供了快速查询dom文档中元素的能力，而且大大强化了javascript中获取页面元素的方式。
而且，jquery还提供了一些展现动画效果的方法，比如淡入淡出，元素移除等特效。
在开发服务器时，jquery也有非常大的优势，比如ajax异步刷新技术，在jquery里面只需要调用一个又要的ajax方法即可。
原生javascript ajax:

```javascript
var Ajax = {
  get: function (url, fn) {
    // xmlhttprequest: 用于在后端与服务器交互
    var xhr = new XMLHttpRequest();
    xhr.open("GET", url, true);
    xhr.onreadystatechange = function () {
      // readyState == 4 说明请求已完成
      if ((xhr.readyState == 4 && xhr.status == 200) || xhr.status == 304) {
        // 从服务器获取数据
        fn.call(this, xhr.responseText);
      }
    };
    xhr.send();
  },

  // data 应为'a=a1&b=b1'这种字符串格式，在jquery里，如果data为对象，则会自动将对象转换为这种字符串格式
  post: function (url, data, fn) {
    var xhr = new XMLHttpRequest();
    xhr.open("POST", url, true);
    xhr.onreadystatechange = function () {
      // readyState == 4 说明请求已完成
      xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
      if ((xhr.readyState == 4 && xhr.status == 200) || xhr.status == 304) {
        // 从服务器获取数据
        fn.call(this, xhr.responseText);
      }
    };
    xhr.send(data);
  },
};
```

jquery的ajax：

```jquery
$.ajax({
    url:,
    type: '',
    data: {},
    success: function () { },
    error: function () { }
})

```

### css 选择器

css选择器有id选择器，类选择器，标签选择器，群组选择器，通配符选择器。

### 使用jquery操作dom

#### 查找元素

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Baidu</title>
		<!-- 引用jQuery库 -->
		<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
	</head>
	<body>
		<script>
		$(document).ready(function(){
			// var lis = $('ul').find('li');
			// var li = lis.eq(1);
			var li = $('ul li').eq(1)
			alert(li.text());
			alert($('ul li:last').attr('id'))
		});
		</script>
		<h2>法宝列表</h2>
		<ul>
			<li>天马流星拳</li>
			<li>阴阳指</li>
			<li id='3'>一指禅</li>
		</ul>
	</body>
</html>
```

#### 添加元素

```javascript
$("<li>新法宝</li>").appendTo($('ul'))
```

#### 删除元素

```javascript
$("#3").remove()
```

#### 隐藏元素

```javascript
$("#3").hide()
```

#### 显示隐藏元素

```javascript
$("#3").show()
```

#### 操作属性

```javascript
			$("#4").attr('name')
			$("#3").attr("id","4")
			$('#4').attr({'title':'testing'})
			$("#4").removeAttr('title')
```

#### 内容操作

```javascript
			console.log($("#3").html())
			console.log($("#3").text())
			$("#3").html("<img src='images/IMG_8888.JPG' style='width: 10px;height: 10px;'/>")
			$("#3").text(一指禅")
      $('select:eq(0)').val()
      $('select:eq(0)').val('02')
      $('#3').parent()
      $('#3').children()
      $('#3').siblings()
      $('#3').prev()
      $('#3').next()
```

## ES6

### 全新的变量定义

javascript是没有块级作用域的。而es6推荐使用let定义变量才有了块级作用域的概念。
除了let, es6还推荐const定义一个只读的变量。const提高了javascript的安全性。

### 解构赋值

变量的解构赋值主要分为数组的解构赋值和对象的解构赋值。

```javascript
let Person = {
  eat: function () {
    console.log("eat---");
  },
  sleep: function () {
    console.log("sleep---");
  },
};

// let eat = Person.eat;
// let sleep = Person.sleep;
// eat();
// sleep();

let { eat, sleep, name = "hi" } = Person;
console.log(name);
console.log(eat());
```

### 字符串升级

#### 允许字符串通过for循环遍历

```javascript
var a = "helloworld";
for (i of a) {
  console.log(i); // value
}
for (i in a) {
  console.log(i); // index
}
```

#### 允许用反引号进行一些简化的字符串定义

```javascript
var name = "cara";
var sayHi = `hello, ${name}`;
console.log(sayHi);
```

### proxy代理

在支持proxy的浏览器环境中，proxy是一个全局对象，它可以被直接使用。proxy的作用就是允许我们声明一个代理，对某个对象进行一些特殊的访问拦截。一个proxy对象有两个部分组成：target、handler。在通过proxy构造函数生成实例对象时，需要提供这两个参数。如下：

```javascript
let obj = {
  name: "keke",
  age: 28,
};

let objProxy = new Proxy(obj, {
  set(target, key, value) {
    if (key == "age" && typeof value != "number") {
      throw new Error(`invalid attempt to set ${key} to ${value}: not number`);
    }
    return (target[key] = value);
  },
  get(target, key, receiver) {
    return target[key];
  },
});
```

### 强化后的数组

#### 快速构建新数组

```javascript
let listData = {
  0: "hi",
  1: "morning",
  2: "noon",
  length: 3,
}; // 类数组：有index和length

console.log(Array.of(listData));
console.log(Array.from(listData)); // 将类数组转化为数组
```

#### 新的数组方法

find， findIndex， fill， copyWithin， entires， keys， values

```javascript
// find， findIndex， fill， copyWithin， entires， keys， values
var a = [1, 2, 3, 4, 5, 7, 6];
console.log(
  a.find(function (item) {
    if (item > 2) {
      return item;
    }
  })
); // 3

console.log(
  a.findIndex(function (item) {
    if (item > 2) {
      return item;
    }
  })
); // 2

// copy the elements from index 4 to index 5 and place them starting at index 0
console.log(a.copyWithin(0, 4, 5)); // [5,2,3,4,5,7,6]

let arr = ["a", "b", "c", "d"];

// Using the entries() method to get an iterator for the array
let iterator = arr.entries();

// Logging the array entries (key-value pairs) to the console
for (let [index, value] of iterator) {
  console.log(index, value);
}

let bKeys = arr.keys();
for (let key of bKeys) {
  console.log(key);
}

let bValues = arr.values();
for (let value of bValues) {
  console.log(value);
}

```

#### 数组复制

在以前的传统项目中，如果要复制一个数组，大多采用slice方法，现在可以用“...”的方法快速复制一个数组。

```javascript
var a = [1, 2, 3, 4, 5, 7, 6];
let b = [...a];
console.log(b);
```

### 强化后的函数

es6对函数做了许多强化/简化，尤其著名的就是箭头函数，而现在es6的语法允许省略function关键字，直接用一个箭头声明一个函数。

```javascript
let sayHi = function (name) {
  console.log(`hello, ${name}`);
};
sayHi("cara");

let sayGoodbye = (name) => {
  console.log(`goodbye, ${name}`);
};
sayGoodbye("cara");

sayGoodbye("cara");
let Person = {
  getName: () => {
    return "cara";
  },
};
console.log(Person.getName());
```

### 更加灵活多变的对象

允许简写。

```javascript
let name = "cara";
let obj = {
  name: name,
};
console.log(obj); // { name: 'cara' }

let age = 10;
let obj1 = {
  name,
  age,
};
console.log(obj1); // { name: 'cara', age: 10 }
```

### promise对象和async函数

#### promise对象

javaqscript会把任务放到一个任务队列中，通过事件循环机制--执行任务队列里的任务，从第一个执行到最后一个。有些执行任务可能事件会比较长，如果等待时间比较长的任务执行完成后在执行下一个任务就会影响用户体验，所以javascript在设计的时候就有同步和异步。异步任务不进入主线程，而进入任务队列中的任务，只有任务队列通知主线程，某个异步任务就可以执行了，这个任务才会进入主线程执行。

promise对象会有三种状态，分别是pending, resolved, rejec，如果代码中没有调取reslove和reject，那么就会返回一个pending状态的promise对象。

```javascript
let gift = null;
new Promise((resolve, reject) => {
  setTimeout((_) => {
    if (Math.random() < 0.2) {
      gift = "_one small gift";
      resolve(gift); // go to then
    } else {
      gift = "_empty";
      reject(gift); // go to catch
    }
  }, 2000);
})
  .then((gift) => {
    console.log("i got the gift:" + gift);
  })
  .catch((gift) => {
    console.log("i got the gift:" + gift);
  });
```

#### async函数

```javascript
let getGiftAsyn = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (Math.random() < 0.2) {
        let gift = "small gift";
        resolve(gift);
      } else {
        let gift = "empty";
        reject(gift);
      }
    }, 2000);
  });
};
// async 必须和 await 配套使用
// async 函数执行时，如果遇到await就会暂停执行，等到触发的
// 异步操作完成后，才会恢复async函数的执行并返回解析值
async function executeAsyncFunc() {
  let gift = await getGiftAsyn();
  console.log(gift);
}
executeAsyncFunc();
```

### symbol

我们在第一章介绍了五种基本数据类型+引用数据类型，es6中新增了一种数据类型symbol来表示唯一值。
每一个创建的symbol都是唯一的，这样在实际应用中可以创建一些唯一的属性以及定义私有变量。

```javascript
// 直接创建
let si = Symbol(); //不需要new运算符实例化
// 传入字符串创建
let si1 = Symbol("mySymbol");
let si2 = Symbol("mySymbol");
console.log(si1 === si2); // false
```

目前，前端项目都会采用模块化构建，可以通过symbol来定义属性名。在symbol出来之前会直接定义对象属性名如下,这里我们看到zhangsan被覆盖了。

```javascript
// a.js
let Obj = {
  name: "zhangsan",
  age: 20,
};
export default Obj;
// b.js
import Obj from "./a.js";
Obj.name = "lisi";
/*
create package.json and add the following to make
sure node knows js are modules.
{
  "type": "module"
}
*/
console.log(Obj); // { name: 'lisi', age: 20 }
```

如果我们不想zhangsan被覆盖，可以通过symbol来定义对象属性名。

```javascript
// a.js
const NAME = Symbol("name");

let Obj = {
  [NAME]: "zhangsan",
  age: 20,
};
export default Obj;
// b.js
import Obj from "./a.js";
const NAME = Symbol("name");
Obj[NAME] = "lisi";
console.log(Obj); // { age: 20, [Symbol(name)]: 'zhangsan', [Symbol(name)]: 'lisi' }
```

### 类

#### 类的基本语法

在es5标准中，通过构造函数来模拟类的功能，如下：

```javascript
function Person(name) {
  this.name = name;
  this.age = 20;
}
Person.prototype.sayName = function () {
  console.log(`my name is ${this.name} `);
};

let zhangsan = new Person("zhangsan");
zhangsan.sayName(); // zhangsan
let lisi = new Person("lisi");
lisi.sayName(); // lisi
```

在es6中，提供了class关键字，使写法更简单。

```javascript
class Person {
  constructor(name) {
    this.name = name;
    this.age = 20;
  }
  sayName() {
    console.log(`my name is ${this.name} `);
  }
}

let zhangsan = new Person("zhangsan");
zhangsan.sayName(); // zhangsan
let lisi = new Person("lisi");
lisi.sayName(); // lisi
```

#### 静态成员

静态成员只有通过类名访问，无法通过实例访问。

```javscript
class Counter {
  static count = 0;
  constructor() {
    Counter.count += 1;
  }
  static getCount() {
    console.log(Counter.count);
  }
}

console.log(Counter.count); // 0
Counter.getCount(); // 0
var a = new Counter();
// console.log(a.count); // will raise error: count is not defined.
Counter.getCount(); // 1
console.log(Counter.count); // 1
```

#### 类的继承

在es5中可以通过call、apply、bind来实现构造函数的继承。es6中提供了extends关键字来实现类的继承。

```javascript
class Dad {
  constructor(name) {
    this.name = name;
  }
  static fn() {
    console.log("fn....");
  }
}

class Son extends Dad {
  constructor(name) {
    super(name);
  }
  hobby() {
    console.log("hobby...");
  }
}

Dad.fn(); // fn....
Son.fn(); // fn....
var d = new Dad("wang");
var s = new Son("wangson");
console.log(d.name); // wang
console.log(s.name); // wangson
s.hobby(); // hobby
```

### 模块化module

要使用es6标准中的模块化工具，必须在script的标签里声明type="module"，然后才能使用es6标准中的导入导出关键字export和import。
```javascript
// index.js
console.log("i am module a");
let obj = {
  name: 'zhangsan',
  age: 20,
};
export let a = 10;
export default obj;
```

```html
	<head>
		<meta charset="utf-8">
		<title>check module</title>
		<script type="module">
		    import A, {a} from './index.js'
		    console.log(A, a)
		</script>
	</head>
```

### set和map集合

在es6中提供了新的数据解构来表示数据，那就是set和map。set集合是一组五重复元素的列表，而map集合是键值对的集合。

```javascript
let set = new Set();
set.add(1);
set.add(2);
set.add(1);
console.log(set); // Set(2) { 1, 2 }
console.log(set.has(2)); // true
console.log(set.has(4)); // false
console.log(set.delete(2)); // true
console.log(set); // Set(1) { 1 }
console.log(set.clear()); // undefined
console.log(set); // Set(0) {}

let arr = [1, 2, 3, 4, 3, 2];
let arrSet = new Set(arr);
console.log(arrSet); // Set(4) { 1, 2, 3, 4 }

let map = new Map();
map.set(1, 2);
map.set(1, 3);
map.set(2, 4);
console.log(map); // Map(2) { 1 => 3, 2 => 4 }
console.log(map.has("1")); // false
console.log(map.has(1)); // true
map.delete(1);
console.log(map); // Map(1) { 2 => 4 }
console.log(map.clear()); // undefined
console.log(map); // Map(0) {}
```

### ...

称为spread和rest运算符。

#### spread

```javascript
// 展开数组
var a = [1, 2, 3];
var b = [4, 5, ...a];
console.log(b); // [ 4, 5, 1, 2, 3 ]
var e = [...a, ...b];
console.log(e); // [1, 2, 3, 4, 5, 1, 2, 3]

// 展开对象
var c = { 1: 2, 3: 4 };
var d = { 5: 6, ...c };
console.log(d); // { '1': 2, '3': 4, '5': 6 }
f = { ...c, ...d };
console.log(f); // { '1': 2, '3': 4, '5': 6 }
```

#### rest

```javacript
// 收集参数为数组
function sum(...num) {
  return num.reduce((acc, currentValue) => acc + currentValue, 0);
}
var b = sum(1, 2, 3, 4, 5);
console.log(b); // 15

// 解构中的rest
// 对象解构
var a = { a: 1, b: 2, c: 3, d: 4 };
var { a, ...rest } = a;
console.log(a); // 1
console.log(rest); // { b: 2, c: 3, d: 4 }

// 数组解构
var c = [1, 2, 3, 4];
var [first, second, ...rest] = c;
console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4]
```