# Front-End
### 前端开发工程师面试宝典！           [![AppVeyor](https://img.shields.io/badge/%E6%89%AB%E5%9C%B0-%E5%83%A7-green.svg?style=plastic)](https://weibo.com/237800789)   

### <a name='preface'>前言（README.md）</a>

```html
本仓库是我整理的前端常见面试题，大部分由我整理，其中个别部分参考网上其他资料，感谢！ 
当然，本仓库的内容由于个人技术所限，和时间关系，有些知识点难免发生错误和遗漏，
还望大家批评指正。探索前端的路上我们应该永远保持谦卑和热情，循序渐进，打好基础，
不可只背“面试题”混进公司，根深才稳健。欢迎大家Star和提交issues。
本资料仅供大家学习参考使用！
```

NO.1 	[README](https://github.com/famensaodiseng/Front-End/edit/master/README.md)				
NO.2 	[前端面试宝典第一版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%B8%80%E7%89%88.md)				
NO.3  	[前端笔记版本第二版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%BA%8C%E7%89%88.md)			
NO.4       [前端笔记版本第三版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E4%B8%89%E7%89%88.md)			
NO.5	[前端笔记版本第四版](https://github.com/famensaodiseng/Front-End/blob/master/%E5%89%8D%E7%AB%AF%E9%9D%A2%E8%AF%95%E5%AE%9D%E5%85%B8%E7%AC%AC%E5%9B%9B%E7%89%88.md) 	 			
NO.6 	[vue常见问题](https://github.com/famensaodiseng/Front-End/blob/master/vue%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98.md)   
NO.7 	[react常见问题](https://github.com/famensaodiseng/Front-End/blob/master/react%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98.md)    
NO.8  	[angular常见问题](https://github.com/famensaodiseng/Front-End/blob/master/angular%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98.md)   
NO.9 	[简历经验分享](https://github.com/famensaodiseng/Front-End/blob/master/%E7%AE%80%E5%8E%86%E7%BB%8F%E9%AA%8C%E5%88%86%E4%BA%AB.md)     
NO.10     [人事常见面试题](https://github.com/famensaodiseng/Front-End/blob/master/%E4%BA%BA%E4%BA%8B%E5%B8%B8%E8%A7%81%E9%9D%A2%E8%AF%95%E9%A2%98.pdf) 

### 欢迎大家一起交流提高        
	

###	redux中间件

中间件提供第三方插件的模式，自定义拦截 action -> reducer 的过程。变为 action -> middlewares -> reducer 。这种机制可以让我们改变数据流，实现如异步 action ，action 过滤，日志输出，异常报告等功能。

常见的中间件：

redux-logger：提供日志输出

redux-thunk：处理异步操作

redux-promise：处理异步操作，actionCreator的返回值是promise

###	React 的工作原理
React 会创建一个虚拟 DOM(virtual DOM)。当一个组件中的状态改变时，React 首先会通过 "diffing" 算法来标记虚拟 DOM 中的改变，第二步是调节(reconciliation)，会用 diff 的结果来更新 DOM。

###	使用 React 有何优点
只需查看 render 函数就会很容易知道一个组件是如何被渲染的
JSX 的引入，使得组件的代码更加可读，也更容易看懂组件的布局，或者组件之间是如何互相引用的
支持服务端渲染，这可以改进 SEO 和性能
易于测试
React 只关注 View 层，所以可以和其它任何框架(如Backbone.js, Angular.js)一起使用
###	使用箭头函数(arrow functions)的优点是什么
作用域安全：在箭头函数之前，每一个新创建的函数都有定义自身的 this 值(在构造函数中是新对象；在严格模式下，函数调用中的 this 是未定义的；如果函数被称为“对象方法”，则为基础对象等)，但箭头函数不会，它会使用封闭执行上下文的 this 值。
简单：箭头函数易于阅读和书写
清晰：当一切都是一个箭头函数，任何常规函数都可以立即用于定义作用域。开发者总是可以查找 next-higher 函数语句，以查看 this 的值
###	为什么建议传递给 setState 的参数是一个 callback 而不是一个对象
因为 this.props 和 this.state 的更新可能是异步的，不能依赖它们的值去计算下一个 state。

除了在构造函数中绑定 this，还有其它方式吗
你可以使用属性初始值设定项(property initializers)来正确绑定回调，create-react-app 也是默认支持的。在回调中你可以使用箭头函数，但问题是每次组件渲染时都会创建一个新的回调。

###	怎么阻止组件的渲染
在组件的 render 方法中返回 null 并不会影响触发组件的生命周期方法


###	何为 JSX
JSX 是 JavaScript 语法的一种语法扩展，并拥有 JavaScript 的全部功能。JSX 生产 React "元素"，你可以将任何的 JavaScript 表达式封装在花括号里，然后将其嵌入到 JSX 中。在编译完成之后，JSX 表达式就变成了常规的 JavaScript 对象，这意味着你可以在 if 语句和 for 循环内部使用 JSX，将它赋值给变量，接受它作为参数，并从函数中返回它。


###	redux有什么缺点

1.一个组件所需要的数据，必须由父组件传过来，而不能像flux中直接从store取。

2.当一个组件相关数据更新时，即使父组件不需要用到这个组件，父组件还是会重新render，可能会有效率影响，或者需要写复杂的shouldComponentUpdate进行判断。

 

###	react组件的划分业务组件技术组件？

根据组件的职责通常把组件分为UI组件和容器组件。

UI 组件负责 UI 的呈现，容器组件负责管理数据和逻辑。

两者通过React-Redux 提供connect方法联系起来。
 

###	react生命周期函数

这个问题要考察的是组件的生命周期

**一、初始化阶段：**

getDefaultProps:获取实例的默认属性

getInitialState:获取每个实例的初始化状态

componentWillMount：组件即将被装载、渲染到页面上

render:组件在这里生成虚拟的DOM节点

componentDidMount:组件真正在被装载之后

**二、运行中状态：**

componentWillReceiveProps:组件将要接收到属性的时候调用

shouldComponentUpdate:组件接受到新属性或者新状态的时候（可以返回false，接收数据后不更新，阻止render调用，后面的函数不会被继续执行了）

componentWillUpdate:组件即将更新不能修改属性和状态

render:组件重新描绘

componentDidUpdate:组件已经更新

**三、销毁阶段：**

componentWillUnmount:组件即将销毁

 

###	react性能优化是哪个周期函数？

shouldComponentUpdate 这个方法用来判断是否需要调用render方法重新描绘dom。因为dom的描绘非常消耗性能，如果我们能在shouldComponentUpdate方法中能够写出更优化的dom diff算法，可以极大的提高性能。 

###	为什么虚拟dom会提高性能?

虚拟dom相当于在js和真实dom中间加了一个缓存，利用dom diff算法避免了没有必要的dom操作，从而提高性能。

具体实现步骤如下：

用 JavaScript 对象结构表示 DOM 树的结构；然后用这个树构建一个真正的 DOM 树，插到文档当中

当状态变更的时候，重新构造一棵新的对象树。然后用新的树和旧的树进行比较，记录两棵树差异

把2所记录的差异应用到步骤1所构建的真正的DOM树上，视图就更新了。


###	diff算法?

把树形结构按照层级分解，只比较同级元素。

给列表结构的每个单元添加唯一的key属性，方便比较。

React 只会匹配相同 class 的 component（这里面的class指的是组件的名字）

合并操作，调用 component 的 setState 方法的时候, React 将其标记为 dirty.到每一个事件循环结束, React 检查所有标记 dirty 的 component 重新绘制.

选择性子树渲染。开发人员可以重写shouldComponentUpdate提高diff的性能。

###	react性能优化方案

（1）重写shouldComponentUpdate来避免不必要的dom操作。

（2）使用 production 版本的react.js。

（3）使用key来帮助React识别列表中所有子组件的最小变化。 

###	简述flux 思想

Flux 的最大特点，就是数据的"单向流动"。

1.用户访问 View

2.View 发出用户的 Action

3.Dispatcher 收到 Action，要求 Store 进行相应的更新

4.Store 更新后，发出一个"change"事件

5.View 收到"change"事件后，更新页面


###	React项目用过什么脚手架？Mern? Yeoman?

Mern：MERN是脚手架的工具，它可以很容易地使用Mongo, Express, React and NodeJS生成同构JS应用。它最大限度地减少安装时间，并得到您使用的成熟技术来加速开发。


###	描述对react理解？
react是一个用于构建用户界面的JS库。

react主要用于构建UI。很多人认为 React 是 MVC 中的 V（视图）。

react起源于：Facebook的内部项目，用来架设instagram网站，于2013年5月。

###	react特点？
生命式设计：react采用声明范式。

高效：react通过对DOM的模拟，最大限度减少DOM交互。

灵活：react可与已知的库和框架很好的配合。

JSX：JSX 是一个看起来很像 XML 的 JavaScript 语法扩展。

组件：通过react构建组件，使得代码更加容易得到复用，能够很好应用在大项目开发中。

单向页面的数据流：react实现了单向响应的数据流，从而减少了重复代码，这也是它为什么比传统数据绑定更简单。

###	React中如何定义初始状态 ？
State和Props

      State主要用于更新界面，组件的State属性在生命周期函数 getInitialState中初始化，当调用组件的this.setState改变state的时候，组件会重新渲染刷新。
Props主要用于组件之间传递数据，也就是标签的属性 这里的pname属性就可以在MyText中通过this.props.pname得到

###	JSX的有什么优点？
JSX 执行更快，因为它在编译为 JavaScript 代码后进行了优化。

它是类型安全的，在编译过程中就能发现错误。

使用 JSX 编写模板更加简单快速。

###	如何创建虚拟DOM、组件?
Var  Com=React.createClass({render(){return ()}})

###	数组如何渲染到页面？
ReactDOM.render(

组件，

Domcoment.getElementById()

)

###	构建view视图用哪个函数？
render: function () {}

###	什么是组件?
通过React.creatClass({})定义一个组件的

可以通过this.props对象传递数据

###	通过什么方法定义一个组件？
Let  Hello = react.createClass({

})

  ReactDOM.render(Hello,document.getElementById(“app”)

###	class是js中的保留字，所以用什么方法创建一个类名？
  class App extends Component{

}

export default App;

###	render函数中，如果多个元素嵌套时需要注意什么？
代码中嵌套多个HTML标签 ，需要使用一个标签元素包裹她

###	写事件是需要注意哪些问题？
  map函数渲染的子元素绑定

          事件冒泡的问题

          页面传递参数问题

          获取页面参数问题

###	什么是state？
是一个状态机，根据数据的改变更新视图

###	state怎么设置默认值？
getInitialState(){}

###	在哪个函数中修改状态？
  setState((state)=>{})

###	props和state区别是什么？
Props是一个属性值，里面数据是不能改变的  
State是一个状态机，根据数据的改变更改视图

###	怎么获取组件中定义的属性？
this.state 

###	props验证器？
propTypes{

                    number：React.PropTypes.number.isRequired 判断是数字类型

                    arr:React.PropTypes.array.isRequired    判断是数组类型

                    function:React.PropTypes.func.isRequired  判断是function类型

                    bool:React.PropTypes.bool.isRequired    判断是布尔类型

                    object:React.PropTypes.object.isRequired  判断是对象类型

｝

###	简述一下ref属性？
  是一个非常特殊的属性，可以用来绑定到render（）输出的任何组件上，允许引用render（）返回的相应的支撑案例，用来确保任何时间总是拿到正确的实例；

###	Ref属性有什么优点？
  可以用来绑定render输出的任何组件

###	Ref怎么获取支撑实例？
    通过this.refs获取属性

###	组件的生命周期钩子函数？
ComponentWillMount 编译前。渲染前调用

componentDidMount 编译完成，渲染后调用

componentWillUpdate 组件state调用后 将要更新时，但还没有render调用

componentDidUpdate 在组件完成更新后立即被调用

componentWillUnmount 在组件从DOM中移除的时候被调用

componentWillReceiveProps 组件接受props之前

shouldComponentUpdate 组件state被调用  必须返回一个布尔值，true false

###	组件中的七个方法？？
SetState 设置状态

ReplaceState 替换状态

setProps设置属性

replacerProps替换属性

forceUpdate  强制更新

findDOMNode获取DOM节点

isMounted 判断组件挂载状态

###	构建view视图用哪个函数？
render(){

function(){

}

}

25、怎么创建一个组建？
var Com=React.createClass{

、render(){

return()

}

}

###	redux中间件
中间件提供第三方插件的模式，自定义拦截 action -> reducer 的过程。变为 action -> middlewares -> reducer 。这种机制可以让我们改变数据流，实现如异步 action ，action 过滤，日志输出，异常报告等功能。
常见的中间件：
redux-logger：提供日志输出
redux-thunk：处理异步操作
redux-promise：处理异步操作，actionCreator的返回值是promise

###	redux有什么缺点
1.一个组件所需要的数据，必须由父组件传过来，而不能像flux中直接从store取。
2.当一个组件相关数据更新时，即使父组件不需要用到这个组件，父组件还是会重新render，可能会有效率影响，或者需要写复杂的shouldComponentUpdate进行判断。

###	react组件的划分业务组件技术组件？
根据组件的职责通常把组件分为UI组件和容器组件。
UI 组件负责 UI 的呈现，容器组件负责管理数据和逻辑。
两者通过React-Redux 提供connect方法联系起来。

###	在生命周期中的哪一步你应该发起 AJAX 请求？

我们应当将AJAX 请求放到 componentDidMount 函数中执行，主要原因有下：
React 下一代调和算法 Fiber 会通过开始或停止渲染的方式优化应用性能，其会影响到 componentWillMount 的触发次数。对于 componentWillMount 这个生命周期函数的调用次数会变得不确定，React 可能会多次频繁调用 componentWillMount。如果我们将 AJAX 请求放到 componentWillMount 函数中，那么显而易见其会被触发多次，自然也就不是好的选择。

如果我们将 AJAX 请求放置在生命周期的其他函数中，我们并不能保证请求仅在组件挂载完毕后才会要求响应。如果我们的数据请求在组件挂载之前就完成，并且调用了setState函数将数据添加到组件状态中，对于未挂载的组件则会报错。而在 componentDidMount 函数中进行 AJAX 请求则能有效避免这个问题。

###	createElement 与 cloneElement 的区别是什么？
createElement 函数是 JSX 编译之后使用的创建 React Element 的函数，而 cloneElement 则是用于复制某个元素并传入新的 Props。

简单地说，一个 React element 描述了你想在屏幕上看到什么。
换个说法就是，一个 React element 是一些 UI 的对象表示。
一个 React Component 是一个函数或一个类，
它可以接受输入并返回一个 React element
(通常是通过 JSX ，它被转化成一个 createElement 调用）。

###	当你调用setState的时候，发生了什么事？
当调用 setState 时，React会做的第一件事情是将传递给 setState 的对象合并到组件的当前状态。这将启动一个称为和解（reconciliation）的过程。和解（reconciliation）的最终目标是以最有效的方式，根据这个新的状态来更新UI。 为此，React将构建一个新的 React 元素树（您可以将其视为 UI 的对象表示）。

一旦有了这个树，为了弄清 UI 如何响应新的状态而改变，React 会将这个新树与上一个元素树相比较（ diff ）。

通过这样做， React 将会知道发生的确切变化，并且通过了解发生什么变化，只需在绝对必要的情况下进行更新即可最小化 UI 的占用空间。

###		在 React 当中 Element 和 Component 有何区别？
简单地说，一个 React element 描述了你想在屏幕上看到什么。换个说法就是，一个 React element 是一些 UI 的对象表示。

一个 React Component 是一个函数或一个类，它可以接受输入并返回一个 React element t（通常是通过 JSX ，它被转化成一个 createElement 调用）。

###		受控组件( controlled component )与不受控制的组件( uncontrolled component )有什么区别？
React 的很大一部分是这样的想法，即组件负责控制和管理自己的状态。

当我们将 native HTML 表单元素（ input, select, textarea 等）投入到组合中时会发生什么？我们是否应该使用 React 作为“单一的真理来源”，就像我们习惯使用React一样？ 或者我们是否允许表单数据存在 DOM 中，就像我们习惯使用HTML表单元素一样？ 这两个问题是受控（controlled） VS 不受控制（uncontrolled）组件的核心。

受控组件是React控制的组件，也是表单数据的唯一真理来源。	
不受控制( uncontrolled component )的组件是您的表单数据由 DOM 处理，而不是您的 React 组件。

虽然不受控制的组件通常更容易实现，因为您只需使用引用从DOM获取值，但是通常建议您通过不受控制的组件来支持受控组件。

主要原因是受控组件 支持即时字段验证 ，允许您有条件地禁用/启用按钮，强制输入格式，并且更多的是 『the React way』。

###		描述事件在React中的处理方式。
为了解决跨浏览器兼容性问题，您的 React 中的事件处理程序将传递 SyntheticEvent 的实例，它是 React 的浏览器本机事件的跨浏览器包装器。

这些 SyntheticEvent 与您习惯的原生事件具有相同的接口，除了它们在所有浏览器中都兼容。有趣的是，React 实际上并没有将事件附加到子节点本身。React 将使用单个事件监听器监听顶层的所有事件。这对于性能是有好处的，这也意味着在更新DOM时，React 不需要担心跟踪事件监听器。

###		13、React 中 keys 的作用是什么？
Keys 是 React 用于追踪哪些列表中元素被修改、被添加或者被移除的辅助标识。在开发过程中，我们需要保证某个元素的 key 在其同级元素中具有唯一性。在 React Diff 算法中 React 会借助元素的 Key 值来判断该元素是新近创建的还是被移动而来的元素，从而减少不必要的元素重渲染。此外，React 还需要借助 Key 值来判断元素与本地状态的关联关系，因此我们绝不可忽视转换函数中 Key 的重要性。

###	vue vs React
1. 相似之处：都是javascript框架，有路由、状态管理、构建工具等、组件式开发。都用到了Virtual DOM。

Virtual DOM是一个映射真实DOM的javascript对象，如果需要改变任何元素的状态，则先在virtual DOM上改变，而不是直接改变真实的DOM。当有变化产生时，一个新的虚拟节点便会被创建，同时计算新旧虚拟结点之间的差别，最后映射真实的dom节点。

2. 不同之处：

 		**Vue**			VS			**React**

| 框架类型	|	mvvm			|	mvc	
| --------   | -----:   | :----: |
| 构建工具	|	vue-cli		|	flux	
| 编写方式	|模板				|	JSX		
| 状态管理	|vuex				|	redux	
|移动端		|	Weex			|	React Native
--------------------- 
###		传入 setState 函数的第二个参数的作用是什么？
该函数会在setState函数调用完成并且组件开始重渲染的时候被调用，我们可以用该函数来监听渲染是否完成：

```this.setState(
  { username: 'tylermcginnis33' },
  () => console.log('setState has finished and the component has re-rendered.')
)
```
###	何为 Children
在JSX表达式中，一个开始标签(比如<a>)和一个关闭标签(比如</a>)之间的内容会作为一个特殊的属性props.children被自动传递给包含着它的组件。

这个属性有许多可用的方法，包括 React.Children.map，React.Children.forEach， React.Children.count， React.Children.only，React.Children.toArray。

###	在 React 中，何为 state
State 和 props 类似，但它是私有的，并且完全由组件自身控制。State 本质上是一个持有数据，并决定组件如何渲染的对象。


###	何为 action
Actions 是一个纯 javascript 对象，它们必须有一个 type 属性表明正在执行的 action 的类型。实质上，action 是将数据从应用程序发送到 store 的有效载荷。

何为 reducer
一个 reducer 是一个纯函数，该函数以先前的 state 和一个 action 作为参数，并返回下一个 state。

###	Redux Thunk 的作用是什么
Redux thunk 是一个允许你编写返回一个函数而不是一个 action 的 actions creators 的中间件。如果满足某个条件，thunk 则可以用来延迟 action 的派发(dispatch)，这可以处理异步 action 的派发(dispatch)。

###	何为纯函数(pure function)
一个纯函数是一个不依赖于且不改变其作用域之外的变量状态的函数，这也意味着一个纯函数对于同样的参数总是返回同样的结果。


###	React Native相对于原生的ios和Android有哪些优势？
1.性能媲美原生APP
2.使用JavaScript编码，只要学习这一种语言
3.绝大部分代码安卓和IOS都能共用
4.组件式开发，代码重用性很高
5.跟编写网页一般，修改代码后即可自动刷新，不需要慢慢编译，节省很多编译等待时间
6.支持APP热更新，更新无需重新安装APP

缺点：
内存占用相对较高
版本还不稳定，一直在更新，现在还没有推出稳定的1.0版本

**备注：**

```
前端的路上我们一起携手共进！如果转载，请标注本链接地址。
```

​[MIT](https://github.com/famensaodiseng/Front-End/blob/master/LICENSE)	©[杨方涛](https://github.com/famensaodiseng)   		

Email:58267980@qq.com



