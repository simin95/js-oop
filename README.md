使用javascript，学习实践面向对象编程（Object Oriented Programming）

1. javascript里没有类的概念，类似的概念叫构造函数，是一个函数，用于构造一类对象

2. 继承允许一个对象得到另一个对象的属性和方法，继承有：经典继承 和 原型继承，但js里没有类这个概念，所以只有原型继承

3. 对象的 __proto__ 属性，指向 构造这个对象的构造函数 的原型

4. 每个对象的原型上都有一个constructor属性，指向创建这个对象的构造函数

5. 所有由一个构造函数构造出的对象，都拥有相同的原型

6. 所有属性都有自己的特征，调用Object.getOwnPropertyDescriptor(对象, 属性名) 来访问：
    value: 方法实现 ; 
    writable : 可重写 ; 
    enumerable : 不可遍历出来（迭代器，for-in）;
    configuraable : 表示属性是否能被删除，置为false后不能再置为true ;

7. js是动态编程语言，可以很方便的向已存在的对象里添加和修改属性，但是记得，不要修改不属于你的对象和属性，因为别人的库(library)也可能在修改，造成不兼容的问题(就像全局变量一样)

8. 在实现原型继承的过程中，如果你重设了原型属性(.protorype)，作为最佳实践，确保你也重设的构造器(constructor)