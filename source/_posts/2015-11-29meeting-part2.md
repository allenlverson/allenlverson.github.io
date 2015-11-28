title: 2015-11-29meeting-part2
date: 2015-11-28 15:13:46
categories:
  - web开发
tags:
  - nodejs
  - javascript
  - mongodb
  - express

---
 <!-- HTML -->
<blockquote class="blockquote-center">城市慷慨，亮整夜光。
 
                                                  [历历万乡] 陈粒</blockquote>

<img src="/uploads/pic03.jpeg" />
<!--more-->
# 项目实战
实验室网站项目中所用的开发技术

## 前端
### jade ——源于 Node.js 的 HTML 模板引擎
在我辛苦学习了html之后，前端工程师们又觉得html太啰嗦。于是开始用jade。
http://segmentfault.com/a/1190000000357534
html2jade： 
http://www.html2jade.org/
### 前端ui框架
经典的twitter bootstrap: http://getbootstrap.com, 
semantic ui: http://semantic-ui.com  
google扁平化风格http://materializecss.com/getting-started.html
## 后端

### nodejs

nodejs：avaScript是一种运行在浏览器的脚本，它简单，轻巧，易于编辑，这种脚本通常用于浏览器的前端编程，但是一位开发者Ryan有一天发现这种前端式的脚本语言可以运行在服务器上的时候，一场席卷全球的风暴就开始了。
Node.js是一个基于Chrome JavaScript运行时建立的平台， 用于方便地搭建响应速度快、易于扩展的网络应用。Node.js 使用事件驱动， 非阻塞I/O 模型而得以轻量和高效，非常适合在分布式设备上运行的数据密集型的实时应用。
#### 异步I/O

#### 事件与回调函数

#### 模块机制

### Express
Express 是一个基于 Node.js 平台的极简、灵活的 web 应用开发框架，它提供一系列强大的特性，帮助你创建各种 Web 和移动设备应用。

#### 路由(route)
路由是指如何定义应用的端点（URIs）以及如何响应客户端的请求。
路由是由一个 URI、HTTP 请求（GET、POST等）和若干个句柄组成，它的结构如下： app.METHOD(path,[callback...], callback)， app 是 express 对象的一个实例， METHOD 是一个 HTTP 请求方法， path 是服务器上的路径， callback 是当路由匹配时要执行的函数。
路由方法源于 HTTP 请求方法，和 express 实例相关联。
路由路径和请求方法一起定义了请求的端点，它可以是字符串、字符串模式或者正则表达式。
中间件：Express 是一个自身功能极简，完全是由路由和中间件构成一个的 web 开发框架：从本质上来说，一个 Express 应用就是在调用各种中间件。

#### 中间件（Middleware） 
中间件（Middleware） 是一个函数，它可以访问请求对象（request object (req)）, 响应对象（response object (res)）, 和 web 应用中处于请求-响应循环流程中的中间件，一般被命名为 next 的变量。
中间件的功能包括：
1. 执行任何代码
2. 修改请求和响应对象
3. 终结请求-响应循环。
4. 调用堆栈中的下一个中间件。
如果当前中间件没有终结请求-响应循环，则必须调用 next() 方法将控制权交给下一个中间件，否则请求就会挂起。
Express 应用可使用如下几种中间件：
1. 应用级中间件
2. 路由级中间件
3. 错误处理中间件
4. 内置中间件
5. 第三方中间件
使用可选则挂载路径，可在应用级别或路由级别装载中间件。另外，你还可以同时装在一系列中间件函数，从而在一个挂载点上创建一个子中间件栈。

### mongoDB与mongooes

为了保存网站的用户数据和业务数据，通常需要一个数据库。MongoDB和Node.js特别般配，因为MongoDB是基于文档的非关系型数据库，文档是按BSON（JSON的轻量化二进制格式）存储的，增删改查等管理数据库的命令和JavaScript语法很像。如果你在Node.js里访问MongoDB的数据，会有我们是一家人的感觉，特别亲切。Node.js有针对MongoDB的数据库驱动：mongodb。你可以使用“npm install mongodb”来安装。
不过直接使用mongodb模块虽然强大而灵活，但有些繁琐，我就使用mongoose吧。如果你对原始的驱动模块感兴趣，可以从这里开始：https://docs.mongodb.org/getting-started/node/client/。
mongoose构建在mongodb之上，提供了Schema、Model和Document对象，用起来更为方便。我们可以用Schema对象定义文档的结构（类似表结构），可以定义字段和类型、唯一性、索引和验证。Model对象表示集合中的所有文档。Document对象作为集合中的单个文档的表示。mongoose还有Query和Aggregate对象，Query实现查询，Aggregate实现聚合。
### keystone.js
以Express和MongoDB为基础搭建的Node.js CMS和web应用程序平台。
http://keystonejs.com/zh/



