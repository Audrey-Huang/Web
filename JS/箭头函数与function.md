### 箭头函数与function

#### 1、语法更加简洁、清晰

从上面的基本语法示例中可以看出，箭头函数的定义要比普通函数定义简洁、清晰得多，很快捷。

#### 2、箭头函数不会创建自己的this（重要！！深入理解！！）

箭头函数没有自己的`this`，它会捕获自己在**定义时**（注意，是定义时，不是调用时）所处的**外层执行环境的`this`**，并继承这个`this`值。所以，箭头函数中`this`的指向在它被定义的时候就已经确定了，之后永远不会改变。

#### 4、.call()/.apply()/.bind()无法改变箭头函数中this的指向

`.call()`/`.apply()`/`.bind()`方法可以用来动态修改函数执行时`this`的指向，但由于箭头函数的`this`定义时就已经确定且永远不会改变。所以使用这些方法永远也改变不了箭头函数`this`的指向，虽然这么做代码不会报错。

#### 5、箭头函数不能作为构造函数使用

但是！！因为箭头函数没有自己的`this`，它的`this`其实是继承了外层执行环境中的`this`，且`this`指向永远不会随在哪里调用、被谁调用而改变，所以箭头函数不能作为构造函数使用，或者说构造函数不能定义成箭头函数，否则用`new`调用时会报错！

#### 6、箭头函数没有自己的arguments

#### 7、箭头函数没有原型prototype

#### 8、箭头函数不能用作Generator函数，不能使用yeild关键字