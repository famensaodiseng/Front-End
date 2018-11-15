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


###	active-class是哪个组件的属性？嵌套路由怎么定义？   
 答：vue-router模块的router-link组件。  
### 	怎么定义vue-router的动态路由？怎么获取传过来的动态参数？ 
 答：在router目录下的index.js文件中，对path属性加上/:id。  使用router对象的params.id  
###	vue-router有哪几种导航钩子？    
 答：三种，一种是全局导航钩子：router.beforeEach(to,from,next)，作用：跳转前进行判断拦截。第二种：组件内的钩子；第三种：单独路由独享组件  
###	scss是什么？安装使用的步骤是？有哪几大特性？
 答：预处理css，把css当前函数编写，定义变量,嵌套。 先装css-loader、node-loader、sass-loader等加载器模块，在webpack-base.config.js配置文件中加多一个拓展:extenstion，再加多一个模块：module里面test、loader
### 	scss是什么？在vue.cli中的安装使用步骤是？有哪几大特性？ 答：css的预编译。
使用步骤：				
第一步：用npm 下三个loader（sass-loader、css-loader、node-sass）			
第二步：在build目录找到webpack.base.config.js，在那个extends属性中加一个拓展.scss			
第三步：还是在同一个文件，配置一个module属性			
第四步：然后在组件的style标签加上lang属性 ，例如：lang=”scss”		
**有哪几大特性:**				
1、可以用变量，例如（$变量名称=值）；			
2、可以用混合器，例如（）			
3、可以嵌套				  
###		mint-ui是什么？怎么使用？说出至少三个组件使用方法？

答：基于vue的前端组件库。npm安装，然后import样式和js，vue.use（mintUi）全局引入。在单个组件局部引入：import {Toast} from ‘mint-ui’。组件一：Toast(‘登录成功’)；组件二：mint-header；组件三：mint-swiper  
###		v-model是什么？怎么使用？ vue中标签怎么绑定事件？
答：可以实现双向绑定，指令（v-class、v-for、v-if、v-show、v-on）。vue的model层的data属性。绑定事件：<input @click=doLog() />  
###		axios是什么？怎么使用？描述使用它实现登录功能的流程？
答：请求后台资源的模块。npm install axios -S装好，然后发送的是跨域，需在配置文件中config/index.js进行设置。后台如果是Tp5则定义一个资源路由。js中使用import进来，然后.get或.post。返回在.then函数中如果成功，失败则是在.catch函数中

###		axios+tp5进阶中，调用axios.post(‘api/user’)是进行的什么操作？axios.put(‘api/user/8′)呢？
答：跨域，添加用户操作，更新操作。  
###		什么是RESTful API？怎么使用?
答：是一个api的标准，无状态请求。请求的路由地址是固定的，如果是tp5则先路由配置中把资源路由配置好。标准有：.post .put .delete  
###		vuex是什么？怎么使用？哪种功能场景使用它？
答：vue框架中状态管理。在main.js引入store，注入。新建了一个目录store，….. export 。场景有：单页应用中，组件之间的状态。音乐播放、登录状态、加入购物车  
###		mvvm框架是什么？它和其它框架（jquery）的区别是什么？哪些场景适合？
答：一个model+view+viewModel框架，数据模型model，viewModel连接两个
区别：vue数据驱动，通过数据来显示视图层而不是节点操作。
场景：数据操作比较多的场景，更加便捷  
###		自定义指令（v-check、v-focus）的方法有哪些？它有哪些钩子函数？还有哪些钩子函数参数？
答：全局定义指令：在vue对象的directive方法里面有两个参数，一个是指令名称，另外一个是函数。组件内定义指令：directives
钩子函数：bind（绑定事件触发）、inserted(节点插入的时候触发)、update（组件内相关更新）
钩子函数参数：el、binding  
###		说出至少4种vue当中的指令和它的用法？
答：v-if：判断是否隐藏；v-for：数据循环出来；v-bind:class：绑定一个属性；v-model：实现双向绑定  
###		vue-router是什么？它有哪些组件？
答：vue用来写路由一个插件。router-link、router-view  
###		导航钩子有哪些？它们有哪些参数？
答：导航钩子有：a/全局钩子和组件内独享的钩子。b/beforeRouteEnter、afterEnter、beforeRouterUpdate、beforeRouteLeave
参数：有to（去的那个路由）、from（离开的路由）、next（一定要用这个函数才能去到下一个路由，如果不用就拦截）最常用就这几种  
###		Vue的双向数据绑定原理是什么？
答：vue.js 是采用数据劫持结合发布者-订阅者模式的方式，通过Object.defineProperty()来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。		
**具体步骤:**			
第一步：需要observe的数据对象进行递归遍历，包括子属性对象的属性，都加上 setter和getter这样的话，给这个对象的某个值赋值，就会触发setter，那么就能监听到了数据变化		
第二步：compile解析模板指令，将模板中的变量替换成数据，然后初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者，一旦数据有变动，收到通知，更新视图				
第三步：Watcher订阅者是Observer和Compile之间通信的桥梁，主要做的事情是:			 1、在自身实例化时往属性订阅器(dep)里面添加自己			 2、自身必须有一个update()方法				 3、待属性变动dep.notice()通知时，能调用自身的update()方法，并触发Compile中绑定的回调，则功成身退。		

第四步：MVVM作为数据绑定的入口，整合Observer、Compile和Watcher三者，通过Observer来监听自己的model数据变化，通过Compile来解析编译模板指令，最终利用Watcher搭起Observer和Compile之间的通信桥梁，达到数据变化 -> 视图更新；视图交互变化(input) -> 数据model变更的双向绑定效果。
ps：16题答案同样适合”vue data是怎么实现的？”此面试题。   
###		请详细说下你对vue生命周期的理解？
答：总共分为8个阶段创建前/后，载入前/后，更新前/后，销毁前/后。
创建前/后： 在beforeCreated阶段，vue实例的挂载元素$el和数据对象data都为undefined，还未初始化。在created阶段，vue实例的数据对象data有了，$el还没有。
载入前/后：在beforeMount阶段，vue实例的$el和data都初始化了，但还是挂载之前为虚拟的dom节点，data.message还未替换。在mounted阶段，vue实例挂载完成，data.message成功渲染。
更新前/后：当data变化时，会触发beforeUpdate和updated方法。
销毁前/后：在执行destroy方法后，对data的改变不会再触发周期函数，说明此时vue实例已经解除了事件监听以及和dom的绑定，但是dom结构依然存在  
###	请说下封装 vue 组件的过程？
答：首先，组件可以提升整个项目的开发效率。能够把页面抽象成多个相对独立的模块，解决了我们传统项目开发：效率低、难维护、复用性等问题。
然后，使用Vue.extend方法创建一个组件，然后使用Vue.component方法注册组件。子组件需要数据，可以在props中接受定义。而子组件修改好数据后，想把数据传递给父组件。可以采用emit方法。  
###	你是怎么认识vuex的？
答：vuex可以理解为一种开发模式或框架。比如PHP有thinkphp，java有spring等。 通过状态（数据源）集中管理驱动组件的变化（好比spring的IOC容器对bean进行集中管理）。
应用级的状态集中放在store中； 改变状态的方式是提交mutations，这是个同步的事物； 异步逻辑应该封装在action中。  
###	vue-loader是什么？使用它的用途有哪些？
答：解析.vue文件的一个加载器，跟template/js/style转换成js模块。
用途：js可以写es6、style样式可以scss或less、template可以加jade等  
###	请说出vue.cli项目中src目录每个文件夹和文件的用法？
答：assets文件夹是放静态资源；components是放组件；router是定义路由相关的配置;view视图；app.vue是一个应用主组件；main.js是入口文件  
###	vue.cli中怎样使用自定义的组件？有遇到过哪些问题吗？
答：第一步：在components目录新建你的组件文件（smithButton.vue），script一定要export default {
第二步：在需要用的页面（组件）中导入：import smithButton from ‘../components/smithButton.vue’
第三步：注入到vue的子组件的components属性上面,components:{smithButton}
第四步：在template视图view中使用，<smith-button>  </smith-button> 问题有：smithButton命名，使用的时候则smith-button。  
###	聊聊你对Vue.js的template编译的理解？
答：简而言之，就是先转化成AST树，再得到的render函数返回VNode（Vue的虚拟DOM节点）				
**详情步骤：**						
首先，通过compile编译器把template编译成AST语法树（abstract syntax tree 即 源代码的抽象语法结构的树状表现形式），compile是createCompiler的返回值，createCompiler是用以创建编译器的。另外compile还负责合并option。
然后，AST会经过generate（将AST语法树转化成render funtion字符串的过程）得到render函数，render的返回值是VNode，VNode是Vue的虚拟DOM节点，里面有（标签名、子节点、文本等等）

  **挑战一下**：

 1、vue响应式原理？

 2、vue-router实现原理？

 3、为什么要选vue？与其它框架对比的优势和劣势？

 4、vue如何实现父子组件通信，以及非父子组件通信？ 

5、vuejs与angularjs以及react的区别？ 

6、vuex是用来做什么的？

 7、vue源码结构

### vue的虚拟dom？

虚拟的DOM的核心思想是：对复杂的文档DOM结构，提供一种方便的工具，进行最小化地DOM操作。

### 如何理解vue中MVVM模式？

MVVM全称是Model-View-ViewModel；vue是以数据为驱动的，一旦创建dom和数据就保持同步，每当数据发生变化时，dom也会变化。DOMListeners和DataBindings是实现双向绑定的关键。DOMListeners监听页面所有View层DOM元素的变化，当发生变化，Model层的数据随之变化；DataBindings监听Model层的数据，当数据发生变化，View层的DOM元素随之变化。

### vue中<keep-alive>的作用？

把切换出去的组件保留在缓存中，可以保留组件的状态或者避免重新渲染。

### vue生命周期的理解？

总共分为8个阶段：

beforeCreate----创建前       组件实例更被创建，组件属性计算之前，数据对象data都为undefined，未初始化。

created----创建后  组件实例创建完成，属性已经绑定，数据对象data已存在，但dom未生成，$el未存在

beforeMount---挂载前 vue实例的$el和data都已初始化，挂载之前为虚拟的dom节点，data.message未替换

mounted-----挂载后    vue实例挂载完成，data.message成功渲染。

beforeUpdate----更新前     当data变化时，会触发beforeUpdate方法

updated----更新后 当data变化时，会触发updated方法

beforeDestory---销毁前      组件销毁之前调用

destoryed---销毁后       组件销毁之后调用，对data的改变不会再触发周期函数，vue实例已解除事件监听和dom绑定，但dom结构依然存在 

### 组件之间的传值通信？

  父组件向子组件传值：

​    1）子组件在props中创建一个属性，用来接收父组件传过来的值；

​    2）在父组件中注册子组件；

​    3）在子组件标签中添加子组件props中创建的属性；

​    4）把需要传给子组件的值赋给该属性

  子组件向父组件传值：

​    1）子组件中需要以某种方式（如点击事件）的方法来触发一个自定义的事件；

​    2）将需要传的值作为$emit的第二个参数，该值将作为实参传给响应事件的方法；

​    3）在父组件中注册子组件并在子组件标签上绑定自定义事件的监听。

\--------------------- 

### 什么是mvvm？

MVVM是Model-View-ViewModel的缩写。mvvm是一种设计思想。Model 层代表数据模型，也可以在Model中定义数据修改和操作的业务逻辑；View 代表UI 组件，它负责将数据模型转化成UI 展现出来，ViewModel 是一个同步View 和 Model的对象。

在MVVM架构下，View 和 Model 之间并没有直接的联系，而是通过ViewModel进行交互，Model 和 ViewModel 之间的交互是双向的， 因此View 数据的变化会同步到Model中，而Model 数据的变化也会立即反应到View 上。

ViewModel 通过双向数据绑定把 View 层和 Model 层连接了起来，而View 和 Model 之间的同步工作完全是自动的，无需人为干涉，因此开发者只需关注业务逻辑，不需要手动操作DOM, 不需要关注数据状态的同步问题，复杂的数据状态维护完全由 MVVM 来统一管理。

### mvvm和mvc区别

mvc和mvvm其实区别并不大。都是一种设计思想。主要就是mvc中Controller演变成mvvm中的viewModel。mvvm主要解决了mvc中大量的DOM 操作使页面渲染性能降低，加载速度变慢，影响用户体验。和当 Model 频繁发生变化，开发者需要主动更新到View 。

### vue的优点是什么？

低耦合。视图（View）可以独立于Model变化和修改，一个ViewModel可以绑定到不同的"View"上，当View变化的时候Model可以不变，当Model变化的时候View也可以不变。

可重用性。你可以把一些视图逻辑放在一个ViewModel里面，让很多view重用这段视图逻辑。

独立开发。开发人员可以专注于业务逻辑和数据的开发（ViewModel），设计人员可以专注于页面设计，使用Expression Blend可以很容易设计界面并生成xml代码。

可测试。界面素来是比较难于测试的，而现在测试可以针对ViewModel来写。

### 说说你对vue生命周期的理解？

答：总共分为8个阶段创建前/后，载入前/后，更新前/后，销毁前/后。

创建前/后： 在beforeCreate阶段，vue实例的挂载元素el和数据对象data都为undefined，还未初始化。在created阶段，vue实例的数据对象data有了，el还没有。

载入前/后：在beforeMount阶段，vue实例的$el和data都初始化了，但还是挂载之前为虚拟的dom节点，data.message还未替换。在mounted阶段，vue实例挂载完成，data.message成功渲染。

更新前/后：当data变化时，会触发beforeUpdate和updated方法。

销毁前/后：在执行destroy方法后，对data的改变不会再触发周期函数，说明此时vue实例已经解除了事件监听以及和dom的绑定，但是dom结构依然存在

### vue如何实现按需加载配合webpack设置？

webpack中提供了require.ensure()来实现按需加载。以前引入路由是通过import 这样的方式引入，改为const定义的方式进行引入。
 不进行页面按需加载引入方式：import home from '../../common/home.vue'
 进行页面按需加载的引入方式：const home = r => require.ensure( [], () => r (require('../../common/home.vue')))

### vuex是什么？怎么使用？哪种功能场景使用它？

vue框架中状态管理。在main.js引入store，注入。新建了一个目录store，….. export 。场景有：单页应用中，组件之间的状态。音乐播放、登录状态、加入购物车

### 请简述下Vuex的原理和使用方法

**数据单向流动**

一个应用可以看作是由上面三部分组成: **View, Actions,State**,数据的流动也是从View => Actions => State =>View 以此达到数据的单向流动.但是项目较大的, 组件嵌套过多的时候, 多组件共享同一个State会在数据传递时出现很多问题.Vuex就是为了解决这些问题而产生的.

Vuex可以被看作项目中所有组件的数据中心,我们将所有组件中共享的State抽离出来,任何组件都可以访问和操作我们的数据中心.

**Vuex**原理

上图可以很好的说明Vuex的组成,一个实例化的Vuex.Store由state, mutations和actions三个属性组成:

- state中保存着共有数据
- 改变state中的数据有且只有通过mutations中的方法,且mutations中的方法必须是同步的
- 如果要写异步的方法,需要些在actions中, 并通过commit到mutations中进行state中数据的更改.

### 请列举出3个Vue中常用的生命周期钩子函数?

1. **created:** 实例已经创建完成之后调用,在这一步,实例已经完成数据观测, 属性和方法的运算, watch/event事件回调. 然而, 挂载阶段还没有开始, $el属性目前还不可见

2. **mounted:** el被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm.$el 也在文档内。

3. **activated:**:keep-alive组件激活时调用 

#### 1、什么是VUE生命周期？

答： Vue 实例从创建到销毁的过程，就是生命周期。从开始创建、初始化数据、编译模板、挂载Dom→渲染、更新→渲染、销毁等一系列过程，称之为 Vue 的生命周期。

#### 2、VUE生命周期的作用是什么？

答：它的生命周期中有多个事件钩子，让我们在控制整个Vue实例的过程时更容易形成好的逻辑。

#### 3、VUE生命周期总共有几个阶段？

答：它可以总共分为8个阶段：创建前/后、载入前/后、更新前/后、销毁前/销毁后。

#### 4、第一次页面加载会触发哪几个钩子？

答：会触发下面这几个beforeCreate、created、beforeMount、mounted 。

#### 5、DOM 渲染在哪个周期中就已经完成？

答：DOM 渲染在 `mounted` 中就已经完成了。

####  VUE实现数据双向绑定的原理：OBJECT.DEFINEPROPERTY()

vue实现数据双向绑定主要是：采 **用数据劫持结合发布者-****订阅者模式** 的方式，通过 `Object.defineProperty()` 来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应监听回调。当把一个普通 Javascript 对象传给 Vue 实例来作为它的 data 选项时，Vue 将遍历它的属性，用 `Object.defineProperty()` 将它们转为 `getter/setter` 。用户看不到 `getter/setter` ，但是在内部它们让 Vue 追踪依赖，在属性被访问和修改时通知变化。

vue的数据双向绑定 将MVVM作为数据绑定的入口，整合Observer，Compile和Watcher三者，通过Observer来监听自己的model的数据变化，通过Compile来解析编译模板指令（vue中是用来解析 `{{}}` ），最终利用watcher搭起observer和Compile之间的通信桥梁，达到数据变化 —>视图更新；视图交互变化（input）—>数据model变更双向绑定效果。

js实现简单的双向绑定：

#### 四、VUE组件间的参数传递

#### 父组件与子组件传值

父组件传给子组件：子组件通过props方法接受数据；

子组件传给父组件： `$emit` 方法传递参数

#### 非父子组件间的数据传递，兄弟组件传值

eventBus，就是创建一个事件中心，相当于中转站，可以用它来传递事件和接收事件。项目比较小时，用这个比较合适（虽然也有不少人推荐直接用VUEX，具体来说看需求咯。技术只是手段，目的达到才是王道）。

#### VUE的路由实现：HASH模式 和 HISTORY模式

hash模式：在浏览器中符号“#”，#以及#后面的字符称之为hash，用 `window.location.hash` 读取。特点：hash虽然在URL中，但不被包括在HTTP请求中；用来指导浏览器动作，对服务端安全无用，hash不会重加载页面。

history模式：history采用HTML5的新特性；且提供了两个新方法： `pushState()` ， `replaceState()` 可以对浏览器历史记录栈进行修改，以及popState事件的监听到状态变更。

#### VUE与ANGULAR以及REACT的区别？

版本在不断更新，以下的区别有可能不是很正确。我工作中只用到vue，对angular和react不怎么熟。

#### 1、与ANGULARJS的区别

相同点：都支持指令：内置指令和自定义指令；都支持过滤器：内置过滤器和自定义过滤器；都支持双向数据绑定；都不支持低端浏览器。

不同点：AngularJS的学习成本高，比如增加了Dependency Injection特性，而Vue.js本身提供的API都比较简单、直观；在性能上，AngularJS依赖对数据做脏检查，所以Watcher越多越慢；Vue.js使用基于依赖追踪的观察并且使用异步队列更新，所有的数据都是独立触发的。

#### 2、与REACT的区别

相同点：React采用特殊的JSX语法，Vue.js在组件开发中也推崇编写.vue特殊文件格式，对文件内容都有一些约定，两者都需要编译后使用；中心思想相同：一切都是组件，组件实例之间可以嵌套；都提供合理的钩子函数，可以让开发者定制化地去处理需求；都不内置列数AJAX，Route等功能到核心包，而是以插件的方式加载；在组件开发中都支持mixins的特性。

不同点：React采用的Virtual DOM会对渲染出来的结果做脏检查；Vue.js在模板中提供了指令，过滤器等，可以非常方便，快捷地操作Virtual DOM。

#### VUE路由的钩子函数

首页可以控制导航跳转，beforeEach，afterEach等，一般用于页面title的修改。一些需要登录才能调整页面的重定向功能。

- beforeEach主要有3个参数to，from，next。
- to：route即将进入的目标路由对象。
- from：route当前导航正要离开的路由。
- next：function一定要调用该方法resolve这个钩子。执行效果依赖next方法的调用参数。可以控制网页的跳转。

#### VUEX是什么？怎么使用？哪种功能场景使用它？

只用来读取的状态集中放在store中； 改变状态的方式是提交mutations，这是个同步的事物； 异步逻辑应该封装在action中。

在main.js引入store，注入。新建了一个目录store，… export 。

场景有：单页应用中，组件之间的状态、音乐播放、登录状态、加入购物车

state：Vuex 使用单一状态树,即每个应用将仅仅包含一个store 实例，但单一状态树和模块化并不冲突。存放的数据状态，不可以直接修改里面的数据。

mutations：mutations定义的方法动态修改Vuex 的 store 中的状态或数据。

getters：类似vue的计算属性，主要用来过滤一些数据。

action：actions可以理解为通过将mutations里面处里数据的方法变成可异步的处理数据的方法，简单的说就是异步操作数据。view 层通过 `store.dispath` 来分发 action。

modules：项目特别复杂的时候，可以让每一个模块拥有自己的state、mutation、action、getters，使得结构非常清晰，方便管理。

#### 其它小知识点

#### 1、CSS只在当前组件起作用

答：在style标签中写入 **scoped** 即可 例如： `<stylescoped>`

#### 2、V-IF 和 V-SHOW 区别

答：v-if按照条件是否渲染，v-show是display的block或none；

#### 3、$ROUTE和$ROUTER的区别

答：$route是“路由信息对象”，包括path，params，hash，query，fullPath，matched，name等路由信息参数。而$router是“路由实例”对象包括了路由的跳转方法，钩子函数等。

PS：缺少的案例代码，这几天再补上去。有些地方可能描述的不够清楚，如果有歧义，可能是我理解错了。

####  css只在当前组件起作用

在style标签中写入**scoped**即可 例如：

#### 2. v-if和v-show区别

v-if按照条件是否渲染，v-show是display的block或none；

#### 3. $route和$router的区别

$route是“路由信息对象”，包括path，params，hash，query，fullPath，matched，name等路由信息参数。而$router是“路由实例”对象包括了路由的跳转方法，钩子函数等。

#### 4. vue.js的两个核心是什么？

·       数据驱动

·       组件系统

#### 5. vue几种常用的指令

v-for 、 v-if 、v-bind、v-on、v-show、v-else

#### 6. vue常用的修饰符？

.prevent: 提交事件不再重载页面；.stop: 阻止单击事件冒泡；.self: 当事件发生在该元素本身而不是子元素的时候会触发；.capture: 事件侦听，事件发生的时候会调用

#### 7. v-on可以绑定多个方法吗？

可以

#### 8. vue中key值的作用？

当 Vue.js 用 v-for 正在更新已渲染过的元素列表时，它默认用“就地复用”策略。如果数据项的顺序被改变，Vue 将不会移动 DOM 元素来匹配数据项的顺序， 而是简单复用此处每个元素，并且确保它在特定索引下显示已被渲染过的每个元素。key的作用主要是为了高效的更新虚拟DOM。

#### 9. 什么是vue的计算属性？

在模板中放入太多的逻辑会让模板过重且难以维护，在需要对数据进行复杂处理，且可能多次使用的情况下，尽量采取计算属性的方式。好处：①使得数据处理结构清晰；②依赖于数据，数据更新，处理结果自动更新；③计算属性内部this指向vm实例；④在template调用时，直接写计算属性名即可；⑤常用的是getter方法，获取数据，也可以使用set方法改变数据；⑥相较于methods，不管依赖的数据变不变，methods都会重新计算，但是依赖数据不变的时候computed从缓存中获取，不会重新计算。

#### 10. vue等单页面应用及其优缺点

**优点：** Vue的目标是通过尽可能简单的 API实现响应的数据绑定和组合的视图组件，核心是一个响应的数据绑定系统。MVVM、数据驱动、组件化、轻量、简洁、高效、快速、模块友好。

**缺点：** 不支持低版本的浏览器，最低只支持到IE9；不利于SEO的优化（如果要支持SEO，建议通过服务端来进行渲染组件）；第一次加载首页耗时相对长一些；不可以使用浏览器的导航按钮需要自行实现前进、后退。



## 6:vue如何实现按需加载配合webpack设置?

```
1.  webpack中提供了require.ensure()来实现按需加载。以前引入路由是通过import 这样的方式引入，改为const定义的方式进行引入。
2.  不进行页面按需加载引入方式：import  home   from '../../common/home.vue'
3.  进行页面按需加载的引入方式：const  home = r => require.ensure( [], () => r (require('../../common/home.vue')))
```

## 7:vuex是什么？怎么使用？哪种功能场景使用它？

vue框架中状态管理。在main.js引入store，注入。新建了一个目录store，….. export 。场景有：单页应用中，组件之间的状态。音乐播放、登录状态、加入购物车

### 请说下封装 **vue** 组件的过程

答：首先，组件可以提升整个项目的开发效率。能够把页面抽象成多个相对独立的模块，解决了我们传统项目开发：**效率低**、**难维护**、**复用性**等问题。

然后，使用Vue.extend方法创建一个组件，然后使用Vue.component方法注册组件。子组件需要数据，可以在props中接受定义。而子组件修改好数据后，想把数据传递给父组件。可以采用emit方法。


### 你是怎么认识vuex的？

答：vuex可以理解为一种开发模式或框架。比如PHP有thinkphp，java有spring等。
 通过状态（数据源）集中管理驱动组件的变化（好比spring的IOC容器对bean进行集中管理）。

应用级的状态集中放在store中； 改变状态的方式是提交mutations，这是个同步的事物； 异步逻辑应该封装在action中。

### 请说出vue.cli项目中src目录每个文件夹和文件的用法？

答：assets文件夹是放静态资源；components是放组件；router是定义路由相关的配置;view视图；app.vue是一个应用主组件；main.js是入口文件


### vue.cli中怎样使用自定义的组件？有遇到过哪些问题吗？

答：第一步：在components目录新建你的组件文件（smithButton.vue），script一定要export default {

第二步：在需要用的页面（组件）中导入：import smithButton from ‘../components/smithButton.vue’

第三步：注入到vue的子组件的components属性上面,components:{smithButton}

第四步：在template视图view中使用，<smith-button>  </smith-button>
 问题有：smithButton命名，使用的时候则smith-button。


### 聊聊你对Vue.js的template编译的理解？

答：简而言之，就是先转化成AST树，再得到的render函数返回VNode（Vue的虚拟DOM节点）

详情步骤：

首先，通过compile编译器把template编译成AST语法树（abstract syntax tree 抽象语法树  即 源代码的抽象语法结构的树状表现形式），compile是createCompiler的返回值，createCompiler是用以创建编译器的。另外compile还负责合并option。

然后，AST会经过generate（将AST语法树转化成render funtion字符串的过程）得到render函数，render的返回值是VNode，VNode是Vue的虚拟DOM节点，里面有（标签名、子节点、文本等等）

16、Vue的双向数据绑定原理是什么？

```
答：vue.js 是采用数据劫持结合发布者-订阅者模式的方式，通过Object.defineProperty()来劫持各个属性的setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调。
具体步骤：
第一步：需要observe的数据对象进行递归遍历，包括子属性对象的属性，都加上 setter和getter
这样的话，给这个对象的某个值赋值，就会触发setter，那么就能监听到了数据变化
第二步：compile解析模板指令，将模板中的变量替换成数据，然后初始化渲染页面视图，并将每个指令对应的节点绑定更新函数，添加监听数据的订阅者，一旦数据有变动，收到通知，更新视图
第三步：Watcher订阅者是Observer和Compile之间通信的桥梁，主要做的事情是:
1、在自身实例化时往属性订阅器(dep)里面添加自己
2、自身必须有一个update()方法
3、待属性变动dep.notice()通知时，能调用自身的update()方法，并触发Compile中绑定的回调，则功成身退。
第四步：MVVM作为数据绑定的入口，整合Observer、Compile和Watcher三者，通过Observer来监听自己的model数据变化，通过Compile来解析编译模板指令，最终利用Watcher搭起Observer和Compile之间的通信桥梁，达到数据变化 -> 视图更新；视图交互变化(input) -> 数据model变更的双向绑定效果。
ps：16题答案同样适合”vue data是怎么实现的？”此面试题。
```

17、请详细说下你对vue生命周期的理解？

```
答：总共分为8个阶段创建前/后，载入前/后，更新前/后，销毁前/后。
创建前/后： 在beforeCreated阶段，vue实例的挂载元素$el和数据对象data都为undefined，还未初始化。在created阶段，vue实例的数据对象data有了，$el还没有。
载入前/后：在beforeMount阶段，vue实例的$el和data都初始化了，但还是挂载之前为虚拟的dom节点，data.message还未替换。在mounted阶段，vue实例挂载完成，data.message成功渲染。
更新前/后：当data变化时，会触发beforeUpdate和updated方法。
销毁前/后：在执行destroy方法后，对data的改变不会再触发周期函数，说明此时vue实例已经解除了事件监听以及和dom的绑定，但是dom结构依然存在
```

18、请说下封装 vue 组件的过程？

```
答：首先，组件可以提升整个项目的开发效率。能够把页面抽象成多个相对独立的模块，解决了我们传统项目开发：效率低、难维护、复用性等问题。
然后，使用Vue.extend方法创建一个组件，然后使用Vue.component方法注册组件。子组件需要数据，可以在props中接受定义。而子组件修改好数据后，想把数据传递给父组件。可以采用emit方法。
```

19、你是怎么认识vuex的？

```
答：vuex可以理解为一种开发模式或框架。比如PHP有thinkphp，java有spring等。
通过状态（数据源）集中管理驱动组件的变化（好比spring的IOC容器对bean进行集中管理）。
应用级的状态集中放在store中； 改变状态的方式是提交mutations，这是个同步的事物； 异步逻辑应该封装在action中。
```

20、vue-loader是什么？使用它的用途有哪些？

```
答：解析.vue文件的一个加载器，跟template/js/style转换成js模块。
用途：js可以写es6、style样式可以scss或less、template可以加jade等
```

21、请说出vue.cli项目中src目录每个文件夹和文件的用法？

```
答：assets文件夹是放静态资源；components是放组件；router是定义路由相关的配置;view视图；app.vue是一个应用主组件；main.js是入口文件
```

22、vue.cli中怎样使用自定义的组件？有遇到过哪些问题吗？

```
答：第一步：在components目录新建你的组件文件（smithButton.vue），script一定要export default {
第二步：在需要用的页面（组件）中导入：import smithButton from ‘../components/smithButton.vue’
第三步：注入到vue的子组件的components属性上面,components:{smithButton}
第四步：在template视图view中使用，<smith-button>  </smith-button>
问题有：smithButton命名，使用的时候则smith-button。
```

23、聊聊你对Vue.js的template编译的理解？

```
答：简而言之，就是先转化成AST树，再得到的render函数返回VNode（Vue的虚拟DOM节点）
详情步骤：
首先，通过compile编译器把template编译成AST语法树（abstract syntax tree 即 源代码的抽象语法结构的树状表现形式），compile是createCompiler的返回值，createCompiler是用以创建编译器的。另外compile还负责合并option。
然后，AST会经过generate（将AST语法树转化成render funtion字符串的过程）得到render函数，render的返回值是VNode，VNode是Vue的虚拟DOM节点，里面有（标签名、子节点、文本等等）
```

24、vue的组件是怎么定义的？父组件怎么给子组件传值？

```
答：首先注册vue.components，第一个参数是组件名称，第二个参数是选项。
直接绑定一个属性，然后在子组件props里面接收
```

25、使用过element.ui吗？说下它其中两个组件的使用方法？

```
答：使用过用过一个布局的，它是由24份，它的写法是:span后面带的数字它占24份里面的宽度。:offset是它
的间距，后面也是跟数字，也是从24份里面取的。
input按钮，标签是el-input，后面type跟上一个属性就是显示不同按钮的类型，有默认的default
（默认的）、success（成功的）、warning（警告）、danger（危险）、info（）、primary（）
```

26、说下你对mvvm的理解？双向绑定的理解?

```
答：mvvm就是vm框架视图、m模型就是用来定义驱动的数据、v经过数据改变后的html、vm就是用来实现双向绑定
    双向绑定:一个变了另外一个跟着变了，例如：视图一个绑定了模型的节点有变化，模型对应的值会跟着变
```

27、说出你所使用过的vue指令

```
答：v-on（监听事件、@change、@click）、v-if（判断的）、v-show（显示/隐藏）、v-bind（绑定属性、:disabled、:src）
```

28、你觉得怎样的自定义组件是完善的？至少说出4点

```
答：第一点、可以通用
第二点、代码尽量简洁
第三点、容易修改
第四点、功能要多一点 
```

一、请说下具体使用vue的理解？

```
答：1、使用vue不必担心布局更改和类名重复导致的js重写，因为它是靠数据驱动双向绑定，底层是通过Object.defineProperty() 定义的数据 set、get 函数原理实现。
2、组件化开发，让项目的可拓展性、移植性更好，代码重用性更高，就好像农民工建房子，拿起自己的工具包就可以开工。项目经理坐等收楼就好。
3、单页应用的体验零距离接触安卓原生应用，局部组件更新界面，让用户体验更快速省时。
4、js的代码无形的规范，团队合作开发代码可阅读性更高。
```

二、你觉得哪些项目适合vue框架？

```html
答：1、数据信息量比较多的，反之类似企业网站就无需此框架了。
2、手机web和app应用多端共用一套界面的项目，因为使用vue.cli+webpack后的前端目录，非常有利于项目的跨平台部署。
```

三、怎么理解MVVM模式的这些框架？

```
答：1、M就是Model模型层，存的一个数据对象。
2、V就是View视图层，所有的html节点在这一层。
3、VM就是ViewModel，它通过data属性连接Model模型层，通过el属性连接View视图层。
```

四、PC端项目你会在哪些场景使用Vue框架？

```
答：上万级数据需要瀑布流更新和搜索的时候，因为数据庞大的时候，用原生的dom操作js和html都会有列表的html布局，迭代很困难。再一个dom节点的大面积添加会影响性能。
那么vue为什么解决这些问题呢？
第一：只需用v-for在view层一个地方遍历数据即可，无需复制一段html代码在js和html两个地方。
第二：vue通过Virtual Dom就是在js中模拟DOM对象树来优化DOM操作。
```

vuex
 1、vuex有哪几种属性？

```
答：有五种，分别是 State、 Getter、Mutation 、Action、 Module
```

2、vuex的State特性是？

```
答：
一、Vuex就是一个仓库，仓库里面放了很多对象。其中state就是数据源存放地，对应于与一般Vue对象里面的data
二、state里面存放的数据是响应式的，Vue组件从store中读取数据，若是store中的数据发生改变，依赖这个数据的组件也会发生更新
三、它通过mapState把全局的 state 和 getters 映射到当前组件的 computed 计算属性中
```

3、vuex的Getter特性是？

```
答：
一、getters 可以对State进行计算操作，它就是Store的计算属性
二、 虽然在组件内也可以做计算属性，但是getters 可以在多组件之间复用
三、 如果一个状态只在一个组件内使用，是可以不用getters
```

4、vuex的Mutation特性是？

```
答：
一、Action 类似于 mutation，不同在于：
二、Action 提交的是 mutation，而不是直接变更状态。
三、Action 可以包含任意异步操作
```

5、Vue.js中ajax请求代码应该写在组件的methods中还是vuex的actions中？

```
答：
一、如果请求来的数据是不是要被其他组件公用，仅仅在请求的组件内使用，就不需要放入vuex 的state里。
二、如果被其他地方复用，这个很大几率上是需要的，如果需要，请将请求放入action里，方便复用，并包装成promise返回，在调用处用async await处理返回的数据。如果不要复用这个请求，那么直接写在vue文件里很方便。
```

6、不用Vuex会带来什么问题？

```
答：
一、可维护性会下降，你要想修改数据，你得维护三个地方
二、可读性会下降，因为一个组件里的数据，你根本就看不出来是从哪来的
三、增加耦合，大量的上传派发，会让耦合性大大的增加，本来Vue用Component就是为了减少耦合，现在这么用，和组件化的初衷相背。
```

### 什么是vue生命周期？

```
答： Vue 实例从创建到销毁的过程，就是生命周期。也就是从开始创建、初始化数据、编译模板、挂载Dom→渲染、更新→渲染、卸载等一系列过程，我们称这是 Vue 的生命周期。
```

### vue生命周期的作用是什么？

```
答：它的生命周期中有多个事件钩子，让我们在控制整个Vue实例的过程时更容易形成好的逻辑。
```

### vue生命周期总共有几个阶段？

```
答：它可以总共分为8个阶段：创建前/后, 载入前/后,更新前/后,销毁前/销毁后
```

### 第一次页面加载会触发哪几个钩子？

```
答：第一次页面加载时会触发 beforeCreate, created, beforeMount, mounted 这几个钩子
```

### DOM 渲染在 哪个周期中就已经完成？

 答：DOM 渲染在 mounted 中就已经完成了。

### 简单描述每个周期具体适合哪些场景？

```
答：生命周期钩子的一些使用方法： beforecreate : 可以在这加个loading事件，在加载实例时触发 created : 初始化完成时的事件写在这里，如在这结束loading事件，异步请求也适宜在这里调用 mounted : 挂载元素，获取到DOM节点 updated : 如果对数据统一处理，在这里写上相应函数 beforeDestroy : 可以做一个确认停止事件的确认框 nextTick : 更新数据后立即操作dom 
```

### axios的特点有哪些？

```
答：
一、Axios 是一个基于 promise 的 HTTP 库，支持promise所有的API
二、它可以拦截请求和响应
三、它可以转换请求数据和响应数据，并对响应回来的内容自动转换成 JSON类型的数据
四、安全性更高，客户端支持防御 XSRF
```

### axios有哪些常用方法？

```
答：
一、axios.get(url[, config])   //get请求用于列表和信息查询
二、axios.delete(url[, config])  //删除
三、axios.post(url[, data[, config]])  //post请求用于信息的添加
四、axios.put(url[, data[, config]])  //更新操作
```

### 说下你了解的axios相关配置属性？

```
答：
`url`是用于请求的服务器URL
 
`method`是创建请求时使用的方法,默认是get
 
`baseURL`将自动加在`url`前面，除非`url`是一个绝对URL。它可以通过设置一个`baseURL`便于为axios实例的方法传递相对URL
 
`transformRequest`允许在向服务器发送前，修改请求数据，只能用在'PUT','POST'和'PATCH'这几个请求方法
 
`headers`是即将被发送的自定义请求头
headers:{'X-Requested-With':'XMLHttpRequest'},
 
`params`是即将与请求一起发送的URL参数，必须是一个无格式对象(plainobject)或URLSearchParams对象
params:{
ID:12345
},
 
`auth`表示应该使用HTTP基础验证，并提供凭据
这将设置一个`Authorization`头，覆写掉现有的任意使用`headers`设置的自定义`Authorization`头
auth:{
username:'janedoe',
password:'s00pers3cret'
},
 
'proxy'定义代理服务器的主机名称和端口
`auth`表示HTTP基础验证应当用于连接代理，并提供凭据
这将会设置一个`Proxy-Authorization`头，覆写掉已有的通过使用`header`设置的自定义`Proxy-Authorization`头。
proxy:{
host:'127.0.0.1',
port:9000,
auth::{
username:'mikeymike',
password:'rapunz3l'
}
}
```

### VNode是什么？虚拟 DOM是什么？

Vue在 页面上渲染的节点，及其子节点称为“虚拟节点 (Virtual Node)”，简写为“VNode”。“虚拟 DOM”是由 Vue 组件树建立起来的整个 VNode 树的称呼。

### 为什么使用key？

当有相同标签名的元素切换时，需要通过 key 特性设置唯一的值来标记以让 Vue 区分它们，否则 Vue 为了效率只会替换相同标签内部的内容。 

### vue-loader是什么？使用它的用途有哪些？

vue-loader是解析.vue文件的一个加载器。

用途：js可以写es6、style样式可以scss或less、template可以加jade等

### scss是什么？在vue.cli中的安装使用步骤是？有哪几大特性？ 

答：scss是css的预编译。

**使用步骤**：

​        第一步：先装css-loader、node-loader、sass-loader等加载器模块

​        第二步：在build目录找到webpack.base.config.js，在那个extends属性中加一个拓展.scss

​        第三步：在同一个文件，配置一个module属性

​        第四步：然后在组件的style标签加上lang属性 ，例如：lang=”scss”

**特性**:

​        可以用变量，例如（$变量名称=值）； 

​        可以用混合器，例如（） 

​        可以嵌套

\--------------------- 

**Vuex**的工作流程，以及它的作用，使用场景。

a) 在vue组件里面，通过dispatch来触发actions提交修改数据的操作。

b) 然后再通过actions的commit来触发mutations来修改数据。

c) mutations接收到commit的请求，就会自动通过Mutate来修改state（数据中心里面的数据状态）里面的数据。

d) 最后由store触发每一个调用它的组件的更新

Vuex的作用：项目数据状态的集中管理，复杂组件(如兄弟组件、远房亲戚组件)的数据通信问题。

\--------------------- 

### 一、什么是MVVM？

MVVM是Model-View-ViewModel的缩写。MVVM是一种设计思想。Model 层代表数据模型，也可以在Model中定义数据修改和操作的业务逻辑；View 代表UI 组件，它负责将数据模型转化成UI 展现出来，ViewModel 是一个同步View 和 Model的对象。

在MVVM架构下，View 和 Model 之间并没有直接的联系，而是通过ViewModel进行交互，Model 和 ViewModel 之间的交互是双向的， 因此View 数据的变化会同步到Model中，而Model 数据的变化也会立即反应到View 上。

ViewModel 通过双向数据绑定把 View 层和 Model 层连接了起来，而View 和 Model 之间的同步工作完全是自动的，无需人为干涉，因此开发者只需关注业务逻辑，不需要手动操作DOM, 不需要关注数据状态的同步问题，复杂的数据状态维护完全由 MVVM 来统一管理。

### 二、mvvm和mvc区别？它和其它框架（jquery）的区别是什么？哪些场景适合？

mvc和mvvm其实区别并不大。都是一种设计思想。主要就是mvc中Controller演变成mvvm中的viewModel。mvvm主要解决了mvc中大量的DOM 操作使页面渲染性能降低，加载速度变慢，影响用户体验。

区别：vue数据驱动，通过数据来显示视图层而不是节点操作。
 场景：数据操作比较多的场景，更加便捷

### 三、vue的优点是什么？

- 低耦合。视图（View）可以独立于Model变化和修改，一个ViewModel可以绑定到不同的"View"上，当View变化的时候Model可以不变，当Model变化的时候View也可以不变。
- 可重用性。你可以把一些视图逻辑放在一个ViewModel里面，让很多view重用这段视图逻辑。
- 独立开发。开发人员可以专注于业务逻辑和数据的开发（ViewModel），设计人员可以专注于页面设计。
- 可测试。界面素来是比较难于测试的，而现在测试可以针对ViewModel来写。

### 四、 组件之间的传值？

·       父组件与子组件传值
 父组件通过标签上面定义传值
 子组件通过props方法接受数据

·       子组件向父组件传递数据
 子组件通过$emit方法传递参数

### 五、路由之间跳转

声明式（标签跳转） 编程式（ js跳转）

### 六、vue.cli中怎样使用自定义的组件？有遇到过哪些问题吗？

·       第一步：在components目录新建你的组件文件（indexPage.vue），script一定要export default {}

·       第二步：在需要用的页面（组件）中导入：import indexPage from '@/components/indexPage.vue'

·       第三步：注入到vue的子组件的components属性上面,components:{indexPage}

·       第四步：在template视图view中使用，
 例如有indexPage命名，使用的时候则index-page

### 七、vue如何实现按需加载配合webpack设置

webpack中提供了require.ensure()来实现按需加载。以前引入路由是通过import 这样的方式引入，改为const定义的方式进行引入。
 不进行页面按需加载引入方式：import home from '../../common/home.vue'
 进行页面按需加载的引入方式：const home = r => require.ensure( [], () => r (require('../../common/home.vue')))

### 八、vuex面试相关

#### （1）vuex是什么？怎么使用？哪种功能场景使用它？

vue框架中状态管理。在main.js引入store，注入。新建一个目录store，….. export 。场景有：单页应用中，组件之间的状态。音乐播放、登录状态、加入购物车

#### （2）vuex有哪几种属性？

有五种，分别是 State、 Getter、Mutation 、Action、 Module

·       vuex的State特性
 A、Vuex就是一个仓库，仓库里面放了很多对象。其中state就是数据源存放地，对应于一般Vue对象里面的data
 B、state里面存放的数据是响应式的，Vue组件从store中读取数据，若是store中的数据发生改变，依赖这个数据的组件也会发生更新
 C、它通过mapState把全局的 state 和 getters 映射到当前组件的 computed 计算属性中

·       vuex的Getter特性
 A、getters 可以对State进行计算操作，它就是Store的计算属性
 B、 虽然在组件内也可以做计算属性，但是getters 可以在多组件之间复用
 C、 如果一个状态只在一个组件内使用，是可以不用getters

·       vuex的Mutation特性
 Action 类似于 mutation，不同在于：Action 提交的是 mutation，而不是直接变更状态；Action 可以包含任意异步操作。

#### （3）不用Vuex会带来什么问题？

·       可维护性会下降，想修改数据要维护三个地方；

·       可读性会下降，因为一个组件里的数据，根本就看不出来是从哪来的；

·       增加耦合，大量的上传派发，会让耦合性大大增加，本来Vue用Component就是为了减少耦合，现在这么用，和组件化的初衷相背。

### 九、 v-show和v-if指令的共同点和不同点

·       v-show指令是通过修改元素的display的CSS属性让其显示或者隐藏

·       v-if指令是直接销毁和重建DOM达到让元素显示和隐藏的效果

### 十、 如何让CSS只在当前组件中起作用

将当前组件的<style>修改为<style scoped>

### 十一、<keep-alive></keep-alive>的作用是什么?

<keep-alive></keep-alive> 包裹动态组件时，会缓存不活动的组件实例，主要用于保留组件状态或避免重新渲染。

### 十二、Vue中引入组件的步骤?

1）采用ES6的import ... from ...语法或CommonJS的require()方法引入组件
 2）对组件进行注册,代码如下

```
// 注册
Vue.component('my-component', {
  template: '<div>A custom component!</div>'
})
```

3）使用组件`<my-component></my-component>`

### 十三、指令v-el的作用是什么?

提供一个在页面上已存在的 DOM 元素作为 Vue 实例的挂载目标.可以是 CSS 选择器，也可以是一个 HTMLElement 实例

### 十四、在Vue中使用插件的步骤

·       采用ES6的import ... from ...语法或CommonJSd的require()方法引入插件

·       使用全局方法Vue.use( plugin )使用插件,可以传入一个选项对象Vue.use(MyPlugin, { someOption: true })

### 十五、请列举出3个Vue中常用的生命周期钩子函数

·       created: 实例已经创建完成之后调用,在这一步,实例已经完成数据观测, 属性和方法的运算, watch/event事件回调. 然而, 挂载阶段还没有开始, $el属性目前还不可见

·       mounted: el被新创建的 vm.$el 替换，并挂载到实例上去之后调用该钩子。如果 root 实例挂载了一个文档内元素，当 mounted 被调用时 vm.$el 也在文档内。

·       activated: keep-alive组件激活时调用

### 十六、active-class是哪个组件的属性？

vue-router模块的router-link组件。

### 十七、怎么定义vue-router的动态路由以及如何获取传过来的动态参数？

在router目录下的index.js文件中，对path属性加上/:id。
 使用router对象的params.id。 

### 十八、vue-router有哪几种导航钩子？

三种，一种是全局导航钩子：router.beforeEach(to,from,next)，作用：跳转前进行判断拦截。
 第二种：组件内的钩子；
 第三种：单独路由独享组件 

### 十九、生命周期相关面试题

总共分为8个阶段创建前/后，载入前/后，更新前/后，销毁前/后。

·       创建前/后： 在beforeCreate阶段，vue实例的挂载元素el和数据对象data都为undefined，还未初始化。在created阶段，vue实例的数据对象data有了，el还没有。

·       载入前/后：在beforeMount阶段，vue实例的$el和data都初始化了，但还是挂载之前为虚拟的dom节点，data.message还未替换。在mounted阶段，vue实例挂载完成，data.message成功渲染。

·       更新前/后：当data变化时，会触发beforeUpdate和updated方法。

·       销毁前/后：在执行destroy方法后，对data的改变不会再触发周期函数，说明此时vue实例已经解除了事件监听以及和dom的绑定，但是dom结构依然存在

#### （1）、什么是vue生命周期

答： Vue 实例从创建到销毁的过程，就是生命周期。也就是从开始创建、初始化数据、编译模板、挂载Dom→渲染、更新→渲染、卸载等一系列过程，我们称这是 Vue 的生命周期。

#### （2）、vue生命周期的作用是什么

答：它的生命周期中有多个事件钩子，让我们在控制整个Vue实例的过程时更容易形成好的逻辑。

#### （3）、vue生命周期总共有几个阶段

答：可以总共分为8个阶段：创建前/后, 载入前/后,更新前/后,销毁前/销毁后

#### （4）、第一次页面加载会触发哪几个钩子

答：第一次页面加载时会触发 beforeCreate, created, beforeMount, mounted 这几个钩子

#### （5）、DOM 渲染在 哪个周期中就已经完成

答：DOM 渲染在 mounted 中就已经完成了。

#### （6）、简单描述每个周期具体适合哪些场景

答：生命周期钩子的一些使用方法：

·       beforecreate : 可以在这加个loading事件，在加载实例时触发

·       created : 初始化完成时的事件写在这里，如在这结束loading事件，异步请求也适宜在这里调用

·       mounted : 挂载元素，获取到DOM节点

·       updated : 如果对数据统一处理，在这里写上相应函数

·       beforeDestroy : 可以做一个确认停止事件的确认框

·       nextTick : 更新数据后立即操作dom

### 二十、说出至少4种vue当中的指令和它的用法？

v-if：判断是否隐藏；v-for：数据循环；v-bind:class：绑定一个属性；v-model：实现双向绑定

### 二十一、vue-loader是什么？使用它的用途有哪些？

解析.vue文件的一个加载器。
 用途：js可以写es6、style样式可以scss或less、template可以加jade等

### 二十二、scss是什么？在vue.cli中的安装使用步骤是？有哪几大特性？

答：css的预编译。
 使用步骤：
 第一步：先装css-loader、node-loader、sass-loader等加载器模块
 第二步：在build目录找到webpack.base.config.js，在那个extends属性中加一个拓展.scss
 第三步：在同一个文件，配置一个module属性
 第四步：然后在组件的style标签加上lang属性 ，例如：lang=”scss”

特性:

·       可以用变量，例如（$变量名称=值）；

·       可以用混合器，例如（）

·       可以嵌套

### 为什么避免 v-if 和 v-for 用在一起

当 Vue 处理指令时，v-for 比 v-if 具有更高的优先级，通过v-if 移动到容器元素，不会再重复遍历列表中的每个值。取而代之的是，我们只检查它一次，且不会在 v-if 为否的时候运算 v-for。

###  VNode是什么？虚拟 DOM是什么？

Vue在 页面上渲染的节点，及其子节点称为“虚拟节点 (Virtual Node)”，简写为“VNode”。“虚拟 DOM”是由 Vue 组件树建立起来的整个 VNode 树的称呼。

### 说说Vue和Angular、ReactJS的相同点和不同点

**与React的相同：**

●都使用了Virtual DOM

●提供了响应式和组件化的视图组件

●将注意力集中保持在核心库，而将其他功能如路由和全局状态管理交给相关的库。

**与React的区别：**

●组件的响应式渲染

React的组件的数据状态发生变化时，它会以该组件为根，重新渲染整个组件子树；而Vue不只去渲染需要渲染的组件。

●HTML+CSS的编写

React使用的JSX语法，将HTML、CSS和JS混写；而Vue使用的是templates模板方式，完全融合与经典的Web技术。

**与Angular的相同：**

Vue早起的灵感是来源于Angular，所以很多语法是类似的，如v-if和ng-if。

**与Angular的区别：**

●与Angular 1对比，Vue的性能更加优越，Angular性能会随着watcher的增加而变慢，而且Angular中一些watcher会出触发另一个更新，使得“脏检查循环”可能会运行多次。

●Angular事实上必须用TypeScript来开发，而且Angular对于TS的支持非常全面，而Vue暂时对于TS的支持还在改进阶段。

●Vue的体积更小，一个包含了 vuex + vue-router 的 Vue 项目 (30kb gzipped) 相比使用了这些优化的 angular-cli 生成的默认项目尺寸 (~130kb) 还是要小的多。

### 简单描述一下Vue中的MVVM模型

Vue是以**数据为驱动**的，Vue自身将DOM和数据进行绑定，一旦创建绑定，DOM和数据将保持同步，每当数据发生变化，DOM会跟着变化。

ViewModel是Vue的核心，它是Vue的一个实例。Vue实例是作用在某个HTML元素上的，这个HTML元素可以是body，也可以是某个id所指代的元素。 DOM Listeners和Data Bindings是实现双向绑定的关键。DOM Listeners监听页面所有View层DOM元素的变化，当发生变化，Model层的数据随之变化；Data Bindings监听Model层的数据，当数据发生变化，View层的DOM元素随之变化。

### 如何阻止Vue中的绑定事件不发生冒泡

可以使用“**事件修饰符**”来处理事件冒泡，如：v-on:click.stop阻止事件冒泡

或v-on:submit.prevent阻止默认事件。

### 父、子组件间是如何通信的？

在Vue中，每个组件实例的作用域是孤立的。这也意味着不能（也不应该）在子组件的模板内直接饮用父组件的数据。父组件通过Props向子组件传递数据，而子组件通过Events向父组件传递数据。 

非父子层级的组件如何实现通信？

简单的应用场景下，可以使用一个空的Vue实例作为中央事件总线。 

在复杂的情况下，可以考虑使用Vue 官方提供的状态管理模式——Vuex来进行管理。

### 什么是动态组件？他的作用是什么？

通过使用保留的 <component> 元素，动态地绑定到它的 is 特性，我们让多个组件可以使用同一个挂载点，并可以动态地切换。

除此之外，Vue还提供了keep-alve指令。keep-alive指令允许把切换出去的组件保留在内存中，并保留它的状态或避免重新渲染。

### 为什么组件中的data属性的值必须是一个函数？

因为在一个组件被多次引用的情况下，如果data的值是一个Object的话，那么由于Object是一个引用类型，所以即使是该组件被多次引用，而其实操作的是同一个对象，最终导致了引用该组件的所有位置都同步的显示了。

### vue与react的对比,如何选型？从性能，生态圈，数据量，数据的传递上，作比较

（1）React 和 Vue 有许多相似之处，它们都有：

使用 Virtual DOM

提供了响应式（Reactive）和组件化（Composable）的视图组件。

将注意力集中保持在核心库，伴随于此，有配套的路由和负责处理全局状态管理的库。

（2）性能：

到目前为止，针对现实情况的测试中，Vue 的性能是优于 React 的。

（3）生态圈

Vue.js: E6+Webpack+unit/e2e+Vue+vue-router+单文件组件+vuex+iVew

React: ES6+Webpack+Enzyme+React+React-router+Redux

（4）什么时候选择Vue.js

如果你喜欢用（或希望能够用）模板搭建应用，请使用Vue

如果你喜欢简单和“能用就行”的东西，请使用Vue

如果你的应用需要尽可能的小和快，请使用Vue

如果你计划构建一个大型应用程序，请使用React

如果你想要一个同时适用于Web端和原生App的框架，请选择React

如果你想要最大的生态圈，请使用React

 

### vue slot是做什么的?

简单来说，假如父组件需要在子组件内放一些DOM，那么这些DOM是显示、不显示、在哪个地方显示、如何显示，就是slot分发负责的活。

### vue路由实现原理?

以官方仓库下 examples/basic 基础例子来一点点具体分析整个流程。

和流程相关的主要需要关注点的就是 components 、 history 目录以及 create-matcher.js 、 create-route-map.js、index.js 、 install.js。

从入口，作为插件，实例化 VueRouter，实例化 History，实例化 Vue，defineReactive 定义 _route，router-link 和 router-view 组件等几个方面展开分析

### 你们vue项目是打包了一个js文件，一个css文件，还是有多个文件？

根据vue-cli脚手架规范，一个js文件，一个CSS文件。

 

### vue遇到的坑，如何解决的？

Vue1.0升级2.0有很多坑: 生命周期；路由中引入静态js，全局组件，全局变量，全局function；v-for循环的key，value值互换了位置，还有track-by；filter过滤器；遍历数组时，key值不能做model；父子通信等。

 

### vue的双向绑定的原理，和angular的对比

在不同的 MVVM 框架中，实现双向数据绑定的技术有所不同。

AngularJS 采用“脏值检测”的方式，数据发生变更后，对于所有的数据和视图的绑定关系进行一次检测，识别是否有数据发生了改变，有变化进行处理，可能进一步引发其他数据的改变，所以这个过程可能会循环几次，一直到不再有数据变化发生后，将变更的数据发送到视图，更新页面展现。如果是手动对 ViewModel 的数据进行变更，为确保变更同步到视图，需要手动触发一次“脏值检测”。

VueJS 则使用 ES5 提供的 Object.defineProperty() 方法，监控对数据的操作，从而可以自动触发数据同步。并且，由于是在不同的数据上触发同步，可以精确的将变更发送给绑定的视图，而不是对所有的数据都执行一次检测。

### Vue里面router-link在电脑上有用，在安卓上没反应怎么解决？

Vue路由在Android机上有问题，babel问题，安装babel polypill 插件解决。

 

**备注：**

```
前端的路上我们一起携手共进！如果转载，请标注本链接地址。
```

​[MIT] (https://github.com/famensaodiseng/Front-End/blob/master/LICENSE)	 ©[杨方涛](https://github.com/famensaodiseng)   		

Email:58267980@qq.com