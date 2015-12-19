## 字符串
### 1. 表示
    "内容"
	'单字符'
	'' //空字符串

> 单双银行一样

### 2.str.length 
> 获取字符串的长度

### 3. str.charAt(index)
> 访问某个 元素位置    
> 访问起始值： 0


### 4. str.indexOf(searchValue[,fromeIndex])
> 查询某个字符串的位置（第一次出现）

### 5. str.search(regexp)
> 搜索匹配的正则表达式

    'mmm123'.search(/[0-9]/)
	'mmm123'.search(/a/) // -1

### 6. str.match(regexp)
> 返回匹配的数组

    ‘mmm1232’.match([/[0-9]/]) //['1']
	'mm123'.match([/[0-9]/g])  // ['','',]
	'mm123'.match(/[A-Z]/)   //null

### 7. str.replace(regexp|substr, newSubstr|function)
> 替换

### 8. str.substring(indexA[, indexB])
> 

### 9. str.slice(beginSlice[, endSlice])
> 与 substring 区别 （负值）

### 10 str.substr(start[, length])

> 注意 substring, slice, substr 区别


### 11 str.split([separator][,limit])

### 12 toLowerCase(), toUpperCase()

### 13 链接：＋

### 14 String() :转成字符串
> String(133)

### 15 转移字符


##JAVACRIPT 对象

### 1. 基本概念（取自java,与 javascript中的对象是有区别的，加深理解）
####对象
>OOP旨在将现实世界中的概念模拟到计算机程序中，它将现实世界中的所有事物视为对象。OOP思想的核心是对象，对象具有属性和行为。
>每个对象都有各自的属性和行为，描述它是什么样或执行什么任务。对象是存在的具体实体，具有明确定义的状态和行为。

####类
>个对象所共有的属性和操作需要组合成一个单元，称为“类”。如果将对象比作房子，那和类就是房子的设计图纸。类是具有相同属性和共同行为的一
>组对象的集合。类确定对象将会拥有的特征（属性）和行为（方法），它定义了一种对象所能拥有的数据和能完成的操作。在而向对象的程序设计中，
>类是程序的基本单元。程序中的对象是类的一个实例，是一个软件单元，它由一组结构化的数据和在其上操作构成.  

##### (1)类的属性  
>对象的特征在类中表示为成员变量，称为类的属性。例如，每个员工对象都有姓名，年龄和体重，它们是类中所有员工共享的共公属性。
>对象或实体拥有的特征在类中表示时称属性。每个对象的每个属性都有拥有其特有的值，但是属性名称由类的所有实例共享。

##### (2)类的方法
>方法是对象执行操作的一种规范。方法指定以何种方式操作对象的数据，是操作的实际实现。对象执行的操作称为方法。

####类和对象的区别
>类和对象之间具有本质的区别。类是用来描述实体的“模板”或“原型”，而对象是实际的实体，每一个对象都是类的一个实例。
>所以通常“为类创建一个对象”也叫作“为类创建一个实例”。对象是实体，而类是概念模型，用来定义对象的所有特性和需操作。
>同一类的所有对象都拥有相同的特性和操作。类是对象的“原型”，它为特定的类型的对象指定了允许的操作和必需的特性。

####封装
>对于OOP而言，封装是将方法和属性一起包装到一个程序单元中。这些单元以类的形式实现。在OOP中，每当定义/对象时，
>往往将相互关联的数据和功能绑定在一起。就像将药用胶囊中的化学药品包装起来一样，这种做法称为封装。隐藏卫生员性，方法或实现的详细的处理方式称为封装。封装的好处之一就是隐藏信息。

####抽象
>由封存装引出的另一个OOP的重要概念是抽象，抽象是处理对象复杂性的一种技术。它是指只关注对象的重要细节，
>而忽略对象的次要细节。通过抽象简化软件的复杂性。这种忽略将要的业务细节和信息而只关注重要数据的概念就叫抽象。
>又分数据抽象和过程抽象。


### 2. javascript 创建对象
> 只有以下两种方式定义对象

    var car = new Object();
	var car = {};           //直接量
	
### 3. 属性和方法
> 定义属性和方法。（例子） key:value形式  
> 注： 最后不能有逗号，否则会报错

    var car = {
		color : 'red',
		run ; function(){}
	};

> 属性方法的访问：2种方式(.,[])  
> []访问形式：可以通过变量获取对象的属性，动态访问

	car.color
	car.run();
	car["color"]
	car['run']()

### 4. 增加属性和方法
> 直接通过 “."运算符进行追加

    var car = {
		color: 'red',
		run : function(){}
	}
	
	car.type = 'suv';
	car.stop = function(){} 

### 5. 修改属性和方法

    car.type = 'qq';
	
### 6. 删除对象属性
> delete 

     delete car.type
	 
### 7 obj.constructor
> 对象是由什么构建出来的？ 

    car.consructor //Object
	var num = new Number(1233);
	num.constructor; //Number 获得number构造函数

### 8.obj.toString()
> 把对象转换成 字符串

    num.toString()

### 9. obj.valueOf
> 获取对象的原始值  

    num.valueOf()
	
### 10. obj.hasOwnProperty()
> 检查对象是否由这个属性   
> 检查继承（后续）

    car.hasOwnProperty('color')  //true
	car.hasOwnProperty('logo')   //false


## 数组
### 1. 创建数组

	var array = new Array();
	var array = [];//直接量
	var array = [1,2,5], //赋值
	var array = [
		153,
		"dsf"
		{},
		[],
		true
	]

### 2. arr.length
> 数组的长度

 var students = [
	 {id:1,score:89},
	 {id:2,score:9},
	 {}
 ]
 
### 3.获取数组元素

    students[0]
	
### 4.修改数组元素

	students[0] = {id:3,score:20}
	
> 注意： 比较 数组与字符串的 length,修改元素，访问元素的区别和不同
	
### 5. arr.indexOf(searchElement [, fromeIndex])
	var telephones = [110, 120, 114];
	telephones.indexOf(120); 1
	telephones.indexOf(1);  -1

### 6. arr.forEach(callback[,thisArg])
> 遍历数组的元素，执行callback属性
> callback(item, index, array) 三个参数

    var editScore = function(item, index, array){
		item.score += 5;
	};
	students.forEach(editScore);
	
### 7. arr.reverse()
> 把数组的元素倒叙

    students.reverse()

### 8. arr.sort([compareFunction])
> 排序
> 修改了原始数组

	//倒xu
    var byScore = function(a, b) {
		return b.score - a.score;
	}
	//正序
	var byScore2 = function(a,b){
		return a.score - b.score;
	}
	students.sort(byScore)
	
> 不传回调

     var m = ['a', 'b', 'c']
	 m.sort()
	 
### 9. arr.push(elem1, elem2, elem3)
> 最后插入

### 10. arr.unshift(elem1, elem2, elem3)
> 前面插入

### 11 arr.shift()
> 返回 数组第一个元素，并删除

### 12。 arr.pop()
> 返回 最后一个 元素， 并删除


### 13 arr.splice(index, howMany[,ele1[,...[,eleN]]])
> 可插入某个元素 
> 可删除某个元素 
> 可删除某些元素，并插入

    students.splice(1,1) //第一个位置删除一个元素
	students.splice(1,0, {}) //第一个位置插入一个元素
	students.splice(1,1,{})  //删除，并插入
	
### 14. 注意
> push(), pop() 组成 栈  
> unshift(), shift() 组成队列     
> reverse,sort,push,unshift,shift,pop,splice :都改变了原数组


### 15. arr.slice(begin[,end])
> 截取数组的 begin 到 end-1    
> 复制一份出来，为改变原来的数组  
> end 不写 到末尾

    var newStudents = students.slice(0,2)

> 思考：（区别）   

    var newStudents1 = students; 
	var newStudents2 = students.slice(0)


### 16. arr.concat(val1,...,valN)
> 链接多个数组，

    var st1 = []
	var st2 = []
	var st3 = []
	var st = st1.concat(st2,st3)

### arr.join([separator])
> 链接多个元素    
> 不写separator 则默认 ‘，’

    var emails = ['a@163.com', 'b@11.com']
	emails.join(,)
	
	str.split(',')
	
### 18 arr.map(callback[,thisArg])
> 返回一个新的数组，所有元素通过回调返回的值

    var scores = [1, 2, 3, 4]
	
	var newScores = scores.map(function(item,index, array){
		return item + 2;
	}) //[]

### 19 arr.reduce(callback, [initialValue])
> 1+2+3+4 连加场景

    var sum = function(previsousResult, item, index, array){
		return previousResult + item.score;
	};
	
	students.reduce(sum,0)
	
### 20 注意：
> slice, concat, join, map, reduce 都没有改变原来的值，
> 而是复制一份新的
	
### 21. 思考
> 对于一个数值型的数组，求和都由几种方法？