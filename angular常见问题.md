# Front-End
## 前端开发工程师面试宝典！   （本文部分有转载，不定期更新！）          [![AppVeyor](https://img.shields.io/badge/%E6%89%AB%E5%9C%B0-%E5%83%A7-green.svg?style=plastic)](https://weibo.com/237800789)   

## <a name='preface'>前言（README.md）</a>

```html
本仓库是我整理的前端常见面试题，大部分由我整理，其中个别部分参考网上其他资料，感谢！   
本资料仅供大家学习参考使用！欢迎大家Star和提交issues。
```
NO.1  [README](https://github.com/famensaodiseng/Front-End/edit/master/README.md)  
NO.2  [简历经验分享](https://github.com/famensaodiseng/Front-End/blob/master/%E7%AE%80%E5%8E%86%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB.md)    
NO.3  [angular常见问题](https://github.com/famensaodiseng/Front-End/blob/master/angular%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98.md)        
NO.4  [前端面试宝典第一版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%B8%80%E7%89%88.md)   
NO.5  [前端笔记版本第二版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%BA%8C%E7%89%88.md)   
NO.6  [前端笔记版本第三版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%B8%89%E7%89%88.md)    
NO.7  [前端笔记版本第四版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E5%9B%9B%E7%89%88.md) 	       
NO.8  [vue常见问题](https://github.com/famensaodiseng/Front-End/blob/master/vue%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98.md) 	 



# 欢迎大家一起交流提高	



### angularjs的几大特性是什么？

双向数据绑定、依赖注入、模板、指令、MVC/MVVM

### 列举几种常见的设计模式，写出没个代表的含义？

MVC ：model view controller
MVVM ：model view viewModel

### 请描述angularjs的运行过程？

angularjs编译所有的HTML元素标签，然后在里面查找angular程序的入口 ng-app 每个元素上的指令是把所有指令收集起来根据优先级依次编译

### ng-bind和ng-model的区别是什么？

ng-bind只能展示数据 ng-model可以操作数据

### 请描述$scope的特点还有其最大的父类？

随创建作用域创建的一个变量，就代表controller所代表的作用域，其持有的对象和方法可在当前及其子作用域生效

### 原生js的延迟或回调在angularjs里能完美运行吗？怎么解决？可以用例子？

不能 需要用$apply来进行传播

### {{ array | filter:{‘age’:23}:true }} 这个过滤里的true是什么意思？

是否用angular.equals进行比较后为真才返回

### 自定义过滤创建后返回的是一个什么对象？

返回一个函数对象 并且函数内要返回最后返回的对象

### ng-repeat循环[1,3,2,4,3,4]数组会报错吗？如果会怎么解决？

会因为有重复的内容 track by $index

### angular常用的服务中value和constant最大的区别是什么？

constant的创建要早于value 并且其可以在config配置中使用 value不行

### 常用服务中factory和service的最大区别是什么？

factory返回的对象当我们使用它的时候手动初始化并返回，而service是当我们第一次使用的时候angular帮我们初始化一次，然后以后使用的时候返回的都是这个对象，factory创建的服务是代表的是其后面函数的返回值，这个返回值可以是任意类型，service不用返回，直接操作的就是自己

### 怎么拦截服务？

在config配置里注入需要拦截的服务的名字+Provider来拦截

### decorator的作用是什么？和拦截服务的区别是什么？

装饰器不仅可以应用在我们自己的服务上，也可以对angularjs核心服务进行拦截、中断甚至替换功能的操作，事实上angularjs的很多测试就是借助$provide.decorator()建立的、请写一个配置路由的代码段（只需要写怎么声明一个路由和其常用属性的代码段）

### resolve的作用是什么？

如果设置了resolve属性，angularjs会将列表中的元素都注入到控制器中，列表对象可以是键(键值是会被注入到控制器中依赖的名字)，也可以是工厂(即可以是一个服务的名字)

### ngRoute默认查找的路由是什么？$routeProvider.otherwise(’/index’)是什么作用？

是/ 设置路由的意外指向到/index

###常使用的跨域方案就哪两种？分别描述其利用的原理？

jsonp; post请求设置请求头 ； jsonp利用的是script可以访问外部信息的原理发送请求并且利用jsonp协议进行数据交互 post设置请求头跳过预请求来实现跨域

### 请写出$http网络请求的几种写法，最少两种

$http.**(url).success(function(data){}).error(function(error){}) $http({ method:’**’, url:url }).success(function(data){
}).error(function(error){
}) $http({ method:’***’, url:url }).then(function success(data){
},function error(error){
})
var promise = $http({ method:’get’, url:url }); promise.then(function(data){
},function(error){
}) 或者 promise.success(function(data){
}); promise.error(function(error){
});

### ng-repeat迭代数组的时候，如果数组中有相同值，会有什么问题，如何解决？

会提示 Duplicates in a repeater are not allowed.加 track by $index

可解决。当然，也可以 trace by 任何一个普通的值，只要能唯一性标识数组中的每一项即可（建立 dom 和数据之间的关联）。

ng-click 中写的表达式，能使用 JS 原生对象上的方法吗？

不止是 ng-click 中的表达式，只要是在页面中，都不能直接调用原生的 JS 方法，因为这些并不存在于与页面对应的 Controller 的 $scope 中。

举个栗子：

{{parseInt(55.66)}}

会发现，什么也没有显示。
但如果在 $scope 中添加了这个函数：
$scope.parseInt = function(x){ return parseInt(x);}
这样自然是没什么问题了。

### 对于这种需求，使用一个 filter 或许是不错的选择：

{{13.14 | parseIntFilter}}

app.filter('parseIntFilter', function(){ return function(item){ return parseInt(item); }})

{{now | 'yyyy-MM-dd'}}

这种表达式里面，竖线和后面的参数通过什么方式可以自定义？

filter，格式化数据，接收一个输入，按某规则处理，返回处理结果。

内置 filter

ng 内置的 filter 有九种：

date（日期）

currency（货币）

limitTo（限制数组或字符串长度）

orderBy（排序）

lowercase（小写）

uppercase（大写）

number（格式化数字，加上千位分隔符，并接收参数限定小数点位数）

filter（处理一个数组，过滤出含有某个子串的元素）

json（格式化 json 对象）

filter 有两种使用方法，一种是直接在页面里：

{{now | date : 'yyyy-MM-dd'}}

另一种是在 js 里面用：
// $filter('过滤器名称')(需要过滤的对象, 参数1, 参数2,...)$filter('date')(now, 'yyyy-MM-dd hh:mm:ss');

### angular 应用常用哪些路由库，各自的区别是什么？

Angular1.x 中常用 ngRoute 和 ui.router，还有一种为 Angular2 设计的 [new router](https://angular.github.io/router/)（面向组件）。后面那个没在实际项目中用过，就不讲了。
无论是 ngRoute 还是 ui.router，作为框架额外的附加功能，都必须以 模块依赖 的形式被引入。
区别
ngRoute 模块是 Angular 自带的路由模块，而 ui.router 模块是基于 ngRoute模块开发的第三方模块。
ui.router 是基于 state （状态）的， ngRoute 是基于 url 的，ui.router模块具有更强大的功能，主要体现在视图的嵌套方面。
使用 ui.router 能够定义有明确父子关系的路由，并通过 ui-view 指令将子路由模版插入到父路由模板的

中去，从而实现视图嵌套。而在 ngRoute 中不能这样定义，如果同时在父子视图中 使用了

会陷入死循环。

## 如果通过angular的directive规划一套全组件化体系，可能遇到哪些挑战？

没有自己用 directive 做过一全套组件，讲不出。
能想到的一点是，组件如何与外界进行数据的交互，以及如何通过简单的配置就能使用吧。
分属不同团队进行开发的 angular 应用，如果要做整合，可能会遇到哪些问题，如何解决？
可能会遇到不同模块之间的冲突。
比如一个团队所有的开发在 moduleA 下进行，另一团队开发的代码在 moduleB 下
angular.module('myApp.moduleA', []) .factory('serviceA', function(){ ... }) angular.module('myApp.moduleB', []) .factory('serviceA', function(){ ... }) angular.module('myApp', ['myApp.moduleA', 'myApp.moduleB'])

会导致两个 module 下面的 serviceA 发生了覆盖。
貌似在 Angular1.x 中并没有很好的解决办法，所以最好在前期进行统一规划，做好约定，严格按照约定开发，每个开发人员只写特定区块代码。
angular 的缺点有哪些？
强约束
导致学习成本较高，对前端不友好。
但遵守 AngularJS 的约定时，生产力会很高，对 Java 程序员友好。
不利于 SEO
因为所有内容都是动态获取并渲染生成的，搜索引擎没法爬取。
一种解决办法是，对于正常用户的访问，服务器响应 AngularJS 应用的内容；对于搜索引擎的访问，则响应专门针对 SEO 的HTML页面。
性能问题
作为 MVVM 框架，因为实现了数据的双向绑定，对于大数组、复杂对象会存在性能问题。
可以用来 [优化 Angular 应用的性能](https://github.com/xufei/blog/issues/23) 的办法：
减少监控项（比如对不会变化的数据采用单向绑定）

主动设置索引（指定 track by
，简单类型默认用自身当索引，对象默认使用 $$hashKey
，比如改为 track by item.id
）

降低渲染数据量（比如分页，或者每次取一小部分数据，根据需要再取）

数据扁平化（比如对于树状结构，使用扁平化结构，构建一个 map 和树状数据，对树操作时，由于跟扁平数据同一引用，树状数据变更会同步到原始的扁平数据）

另外，对于Angular1.x ，存在 脏检查 和 模块机制 的问题。
移动端
可尝试 Ionic，但并不完善。

### 补充

对于一个 DI 容器，必须具备三个要素：依赖项的注册，依赖关系的声明和对象的获取。
在 AngularJS 中，module 和 $provide 都可以提供依赖项的注册；内置的 injector 可以获取对象（自动完成依赖注入）；依赖关系的声明，就是前面问题中提到的那样。
下面是个栗子
// 对于 module，传递参数不止一个，代表新建模块，空数组代表不依赖其他模块// 只有一个参数（模块名），代表获取模块// 定义 myApp，添加 myApp.services 为其依赖项angular.module('myApp', ['myApp.services']);// 定义一个 services module，将 services 都注册在这个 module 下面angular.module('myApp.services', [])// $provider 有 factory, service, provider, value, constant// 定义一个 HttpServiceangular.module('myApp.services').service('HttpService', ['$http', function($http){ ...}])

### 如何看待angular2

相比 Angular1.x，Angular2的改动很大，几乎算是一个全新的框架。
基于 TypeScript（可以使用 TypeScript 进行开发），在大型项目团队协作时，强语言类型更有利。
组件化，提升开发和维护的效率。
还有 module 支持动态加载，new router，promise的原生支持等等。
迎合未来标准，吸纳其他框架的优点，值得期待，不过同时要学习的东西也更多了（ES next、TS、Rx等）    


###		angularjs 是 mvc 还是 mvvm 框架?
首先阐述下你对mvc和mvvm的理解
首先为什么我们会需要MVC？因为随着代码规模越来越大，切分职责是大势所趋，还有为了后期维护方便，修改一块功能不影响其他功能。还有为了复用，因为很多逻辑是一样的。而MVC只是手段，终极目标是模块化和复用。
mvvm的优点:

低耦合：View可以独立于Model变化和修改，同一个ViewModel可以被多个View复用；并且可以做到View和Model的变化互不影响
可重用性：可以把一些视图的逻辑放在ViewModel，让多个View复用
独立开发：开发人员可以专注与业务逻辑和数据的开发（ViewModemvvmdi计人员可以专注于UI(View)的设计
可测试性：清晰的View分层，使得针对表现层业务逻辑的测试更容易，更简单
在angular中MVVM模式主要分为四部分：

View：它专注于界面的显示和渲染，在angular中则是包含一堆声明式Directive的视图模板。
ViewModel：它是View和Model的粘合体，负责View和Model的交互和协作，它负责给View提供显示的数据，以及提供了View中Command事件操作Model的途径；在angular中$scope对象充当了这个ViewModel的角色；
Model：它是与应用程序的业务逻辑相关的数据的封装载体，它是业务领域的对象，Model并不关心会被如何显示或操作，所以模型也不会包含任何界面显示相关的逻辑。在web页面中，大部分Model都是来自Ajax的服务端返回数据或者是全局的配置对象；而angular中的service则是封装和处理这些与Model相关的业务逻辑的场所，这类的业务服务是可以被多个Controller或者其他service复用的领域服务。
Controller：这并不是MVVM模式的核心元素，但它负责ViewModel对象的初始化，它将组合一个或者多个service来获取业务领域Model放在ViewModel对象上，使得应用界面在启动加载的时候达到一种可用的状态。

###		angular 核心？
AngularJS是为了克服HTML在构建应用上的不足而设计的。 AngularJS有着诸多特性，最为核心的是：

MVC
模块化
自动化双向数据绑定
语义化标签、依赖注入等等
factory 和 service，provider是什么关系？
factory 把 service 的方法和数据放在一个对象里，并返回这个对象；service 通过构造函数方式创建 service，返回一个实例化对象；provider 创建一个可通过 config 配置的 service。

从底层实现上来看，service 调用了 factory，返回其实例；factory 调用了 provider，将其定义的内容放在 $get 中返回。factory 和 service 功能类似，只不过 factory 是普通 function，可以返回任何东西（return 的都可以被访问，所以那些私有变量怎么写你懂的）；service 是构造器，可以不返回（绑定到 this 的都可以被访问）；provider 是加强版 factory，返回一个可配置的 factory。

###ng-if 跟 ng-show/hide的区别有哪些？
ng-if 在后面表达式为 true 的时候才创建这个 dom 节点，ng-show 是初始时就创建了，用 display:block 和 display:none 来控制显示和不显示。
ng-if 会（隐式地）产生新作用域，ng-switch 、 ng-include 等会动态创建一块界面的也是如此。

###		ng-repeat迭代数组的时候，如果数组中有相同值，会有什么问题，如何解决？
会提示 Duplicates in a repeater are not allowed. 加 track by $index 可解决。当然，也可以 trace by 任何一个普通的值，只要能唯一性标识数组中的每一项即可（建立 dom 和数据之间的关联）。

在写controlloer逻辑的时候 你需要注意什么？
简化代码（这个是所有开发人员都要具备的）
坚决不能操作dom节点 这个时候可能会问 为什么不能啊
你的回答是：DOM操作只能出现在指令（directive）中。最不应该出现的位置就是服务（service）中。Angular倡导以测试驱动开发，在service或者controller中出现了DOM操作，那么也就意味着的测试是无法通过的。当然，这只是一点，重要的是使用Angular的其中一个好处是啥，那就是双向数据绑定，这样就能专注于处理业务逻辑，无需关系一堆堆的DOM操作。如果在Angular的代码中还到处充斥着各种DOM操作，那为什么不直接使用jquery去开发呢。

### 测试驱动开发是什么呢？普及一下：

测试驱动开发，英文全称Test-Driven Development，简称TDD，是一种不同于传统软件开发流程的新型的开发方法。它要求在编写某个功能的代码之前先编写测试代码，然后只编写使测试通过的功能代码，通过测试来推动整个开发的进行。这有助于编写简洁可用和高质量的代码，并加速开发过程。

###	单页应用有哪些优缺点？
单页Web应用（single page web application，SPA），就是只有一张Web页面的应用。单页应用程序 (SPA) 是加载单个HTML 页面并在用户与应用程序交互时动态更新该页面的Web应用程序。 浏览器一开始会加载必需的HTML、CSS和JavaScript，所有的操作都在这张页面上完成，都由JavaScript来控制。因此，对单页应用来说模块化的开发和设计显得相当重要。

速度：更好的用户体验，让用户在web app感受native app的速度和流畅，
MVC：经典MVC开发模式，前后端各负其责。
ajax：重前端，业务逻辑全部在本地操作，数据都需要通过AJAX同步、提交。
路由：在URL中采用#号来作为当前视图的地址,改变#号后的参数，页面并不会重载。
单页Web应用（single page web application，SPA）是当今网站开发技术的弄潮儿，很多传统网站都在或者已经转型为单页Web应用，新的单页Web应用网站（包括移动平台上的）也如雨后春笋般涌现在人们的面前，如Gmail、Evernote、Trello等。如果你是一名Web开发人员，却还没开发过或者甚至是没有听说过单页应用，那你已经Out很久了。
单页Web应用和前端工程师们息息相关，因为主要的变革发生在浏览器端，用到的技术其实还是HTML+CSS+JavaScript，所有的浏览器都原生支持，当然有的浏览器因为具备一些高级特性，从而使得单页Web应用的用户体验更上一层楼。关于单页应用的优点和缺点，网上讲解的文章有很多，这里就不展开论述了。 单页Web应用，顾名思义，就是只有一张Web页面的应用。浏览器一开始会加载必需的HTML、CSS和JavaScript，之后所有的操作都在这张页面上完成，这一切都由JavaScript来控制。因此，单页Web应用会包含大量的JavaScript代码，复杂度可想而知，模块化开发和设计的重要性不言而喻。

优点：

分离前后端关注点，前端负责界面显示，后端负责数据存储和计算，各司其职，不会把前后端的逻辑混杂在一起；
减轻服务器压力，服务器只用出数据就可以，不用管展示逻辑和页面合成，吞吐能力会提高几倍；
同一套后端程序代码，不用修改就可以用于Web界面、手机、平板等多种客户端；
缺点：

SEO问题，现在可以通过Prerender等技术解决一部分；
前进、后退、地址栏等，需要程序进行管理；
书签，需要程序来提供支持；


###	angular 的数据绑定采用什么机制？详述原理
脏检查机制。

双向数据绑定是 AngularJS 的核心机制之一。当 view 中有任何数据变化时，会更新到 model ，当 model 中数据有变化时，view 也会同步更新，显然，这需要一个监控。

原理就是，Angular 在 scope 模型上设置了一个 监听队列，用来监听数据变化并更新 view 。每次绑定一个东西到 view 上时 AngularJS 就会往 $watch 队列里插入一条 $watch，用来检测它监视的 model 里是否有变化的东西。当浏览器接收到可以被 angular context 处理的事件时，$digest 循环就会触发，遍历所有的 $watch，最后更新 dom。
举个栗子
```
<button ng-click="val=val+1">increase 1</button>
click 时会产生一次更新的操作（至少触发两次 $digest 循环）
```
按下按钮

浏览器接收到一个事件，进入到 angular context
$digest 循环开始执行，查询每个 $watch 是否变化

由于监视 $scope.val 的 $watch 报告了变化，因此强制再执行一次 $digest 循环

新的 $digest 循环未检测到变化

浏览器拿回控制器，更新 $scope.val 新值对应的 dom

$digest 循环的上限是 10 次（超过 10次后抛出一个异常，防止无限循环）。


###		表达式 {{yourModel}}是如何工作的?

它依赖于 $interpolation服务，在初始化页面html后，它会找到这些表达式，并且进行标记，于是每遇见一个{{}}，则会设置一个$watch。而$interpolation会返回一个带有上下文参数的函数，最后该函数执行，则算是表达式$parse到那个作用域上。

###		angular 的缺点有哪些？
强约束
导致学习成本较高，对前端不友好。

但遵守 AngularJS 的约定时，生产力会很高，对 Java 程序员友好。

不利于 SEO
因为所有内容都是动态获取并渲染生成的，搜索引擎没法爬取。

一种解决办法是，对于正常用户的访问，服务器响应 AngularJS 应用的内容；对于搜索引擎的访问，则响应专门针对 SEO 的HTML页面。

性能问题
作为 MVVM 框架，因为实现了数据的双向绑定，对于大数组、复杂对象会存在性能问题。

可以用来 优化 Angular 应用的性能 的办法：

减少监控项（比如对不会变化的数据采用单向绑定）

主动设置索引（指定 track by，简单类型默认用自身当索引，对象默认使用 $$hashKey，比如改为 track by item.id）

降低渲染数据量（比如分页，或者每次取一小部分数据，根据需要再取）

数据扁平化（比如对于树状结构，使用扁平化结构，构建一个 map 和树状数据，对树操作时，由于跟扁平数据同一引用，树状数据变更会同步到原始的扁平数据）

另外，对于Angular1.x ，存在 脏检查 和 模块机制 的问题。

###		解释下什么是$rootScrope以及和$scope的区别？

通俗的说$rootScrope 页面所有$scope的父亲。

我们来看下如何产生$rootScope和$scope吧。

step1:Angular解析ng-app然后在内存中创建$rootScope。

step2:angular回继续解析，找到{{}}表达式，并解析成变量。

step3:接着会解析带有ng-controller的div然后指向到某个controller函数。 这个时候在这个controller函数变成一个$scope对象实例。


###		angular中的$http

$http 是 AngularJS 中的一个核心服务，用于读取远程服务器的数据。

我们可以使用内置的$http服务直接同外部进行通信。$http服务只是简单的封装了浏览器原生的XMLHttpRequest对象。

 

### ng-repeat迭代数组的时候，如果数组中有相同值，会有什么问题，如何解决？

会提示 Duplicates in a repeater are not allowed. 加 track by $index 可解决。当然，也可以 trace by 任何一个普通的值，只要能唯一性标识数组中的每一项即可（建立 dom 和数据之间的关联）

###  Observables和Promises的核心区别是什么？

从堆栈溢出就是一个区别： 

当异步操作完成或失败时，Promise会处理一个单个事件。

Observable类似于（在许多语言中的）Stream，当每个事件调用回调函数时，允许传递零个或多个事件。通常Observable比Promise更受欢迎，因为它不但提供了Promise特性，还提供了其它特性。使用Observable可以处理0,1或多个事件。你可以在每种情况下使用相同的API。Observable是可取消的，这相比于Promise也具有优势。如果服务器的HTTP请求结果或其它一些异步操作不再需要，则Observable的订阅者可以取消订阅，而Promise将最终调用成功或失败的回调，即使你不需要通知或其提供的结果。Observable提供像map，forEach，reduce之类的类似于数组的运算符，还有强大的运算符，如retry（）或replay（）等，使用起来是相当方便的。

Promises vs Observables

Promises：
返回单个值
不可取消
Observables：
可以使用多个值
可取消
支持map，filter，reduce和类似的操作符
ES 2016提议的功能
使用反应式扩展（RxJS）
根据时间的变化，数组成员可以异步获取
###		优化 Angular 应用的性能
减少监控项（比如对不会变化的数据采用单向绑定）
主动设置索引（指定 track by，简单类型默认用自身当索引，对象默认使用 $$hashKey，比如改为 track by item.id）
降低渲染数据量（比如分页，或者每次取一小部分数据，根据需要再取）
数据扁平化（比如对于树状结构，使用扁平化结构，构建一个 map 和树状数据，对树操作时，由于跟扁平数据同一引用，树状数据变更会同步到原始的扁平数据）


###	详述 angular 的 “依赖注入”
赖注入是一种软件设计模式，目的是处理代码之间的依赖关系，减少组件间的耦合。
原理：AngularJS是通过构造函数的参数名字来推断依赖服务名称的，通过 toString() 来找到这个定义的 function 对应的字符串，然后用正则解析出其中的参数（依赖项），再去依赖映射中取到对应的依赖，实例化之后传入。



**备注：**

```
前端的路上我们一起携手共进！如果转载，请标注本链接地址。
```

​[MIT](https://github.com/famensaodiseng/Front-End/blob/master/LICENSE)	©[杨方涛](https://github.com/famensaodiseng)   		

Email:58267980@qq.com

