#### eval()

作用：可将字符串转化成可执行js代码



​	eval规定是不允许定义别名的，但在非严格模式下，evel函数可以改变局部作用域的变量，直接调用eval时，代码会在其所在的作用域内的上下文进行执行；当eval被赋予了别名后，通过别名调用时，其执行的上下文是全局，并且无法访问局部变量；

​	严格模式下，eval被指定为保留字，不弄被赋值，并且变量名、函数名不能取名为eval;



缺点：

- 安全性：eval会执行所有传入的代码，容易引起跨站脚本攻击；
- 代码可读性差：字符串拼接使代码看起来杂乱，不好维护；
- 不利于调试：控制台无法给eval内的代码打断点；
- 性能：由于eval执行的代码无法预测，所以编译器无法对其就行性能优化；
- 可替代：由于Function对象也能实现eval类似的功能，所以eval不是必须要用的；

优点:

​	如果对于eval能够很好地了解并使用的话，对于某些功能来说，会很方便；