| 简单数据类型    | 说明                                           | 默认值    |
| --------------- | ---------------------------------------------- | --------- |
| Number          | 数字型，包括整型值和浮点型值，如21/0.21        | 0         |
| Boolean         | 布尔类型，如true、false，等价于1和0            | false     |
| String          | 字符串类型，带引号                             | “”        |
| Undefined       | `var a;`声明变量a但没有给值，此时是undefined。 | undefined |
| Null            | `var a = null;`声明了变量a为空值               | null      |
| symbol(es6新增) | let sym=Symbol()，不能使用new的方式构造        |           |

```javascript
var und = undefined;
console.log(und + 1); // NaN
var nul = null;
console.log(nul + 1); // 1
```

#### 获取数据类型

`typeof`用于检测数据变量的类型。

```javascript
var timer = null;
typeof timer; // object
```

null表示一个空对象引用，可以用来清空对象

```javascript
var person = null; // 值为null，但类型为对象
var person = undefined; // 值为undefined， 类型为undefined
```

##### undefined和null的区别

```javascript
typeof null					// object
typeof undefined			// undefined
null == undefined			// false
undefined == undefined		// true
```

#### 数据类型转换

转化为字符串

* num.toString()
* String(num)
* **加号拼接**： num+""

转化为数字

* parseInt(str) 	floor取整

  ```javascript
  parseInt('120px')	// 120
  parseInt('rem120px')	// NaN
  ```

* parseFloat(str)

* Number(str)

  ```javascript
  Number('120px')	// NaN
  ```

* 算术运算隐式转换

  ```javascript
  '12' - 0;	// 12
  '1' * 1;	// 1
  ```

#### 转换为Boolean

* Boolean()

  转换为false

  * ‘ ’
  * 0
  * NaN
  * null
  * undefined

#### 比较

== 表示值相等，默认数据类型转换，会把字符串转换为数字型

而 === 表示值和数据类型相等

```javascript
18 == '18'	// true
18 === '18' 	// false
```

#### 逻辑运算

逻辑与

如果表达式1为真，返回表达式2

```javascript
123 && 456; 	// 456
0 && 456; 		// 0
0 && 1 + 2 && 456 * 7890; 	// 0
```



#### 引用类型

object储存的是一个指向对象真实内存地址的指针，对象包括Array，Object，Function,RegExp，Math等