###二　数据绑定
#### 2.1Angularjs 中的数据绑定
1. 单向视图：在Rails等传统Web框架中，控制器将多个模型中的数据和模板组合在一起形成视图，并将其提供给用户，这个组合过程产生了一个单向视图．如果没有创建任何自定义的javascript组件，视图只会体现它渲染时模型暴露出的数据．
2. Angularjs　采用实时模板代替视图，而不是将数据合并进模板之后更新DOM.任何一个独立视图组件中的值都是动态替换的．Angularjs最重要的功能之一．
3. ng-app 属性声明所有被其包含的内容都属于AngularJS应用．这也是可以在Web应用中嵌套AngularJS应用的原因．
4. AngularJS会记录数据模型所包含的数据在任何特定时间点的值，而不是原始值．
5. ＂脏＂检查：AngularJS 跟踪和响应应用变化的方式．当AngularJS 认为某个值可能发生变化时，它会运行自己的事件循环检查这个值是否变＂脏＂．如果该值从上次事件循环运行之后发生了变化，则该值被认为是＂脏＂值．
> 注：  
> (1). 这个事件循环调用$digest().
> (2). "脏＂检查是检查数据模型变化的有效手段．
> (3). 当有潜在变化的时，AngularJS 会执行事件循环执行脏检查来保证数据一致性． 

#### 2.2简单的数据绑定
1. $scope 数据模型对象，简单的javascript对象，其属性可以被视图访问，也可以被所在的控制器访问.
2. 双向数据绑定：视图改变了数据模型的某个值，数据模型会执行＂脏＂检查，更新这个值．如果数据模型更新了某个值，视图也会重新渲染它．
3. 新指令：ng-model ng-app 对象：$timeout:　setTimeout 的引用

#### 2.3数据绑定的最佳实践
1. 由于javascript特点，以及在传值和引用的不同，通常认为：在视图中使用对象的属性而不是对象本身进行绑定，是最佳实践．

#### 2.4总结：
1. 概要：单向视图，Angularjs视图，＇脏＇检查，$scope 双向数据绑定，　数据绑定最佳实践
2. 问题：　$timeout 对象．javascript 传值和引用．


### 三 模块
1. 使用模块的好处：
> 保持全局命名空间的清洁．　
> 编写测试代码更容易，保持其清洁，以便更容易找到互相隔离的功能．  
> 易于在不同引用直接复用代码
> 使应用能够任意加载代码的各个部分
2. 声明应用  
        /**
		*@params: String (模块名), Arrays (模块依赖)
		*/
		angular.module('myapp',[])
		
		angular.module('myapp') //引用
		