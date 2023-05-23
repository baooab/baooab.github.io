# Zhang Bao's Personal Website

Hello, My Chinese name is "张宝". I am a front-end development programmer (more than 6 years of experience)from Shanghai, China. I usually write in Chinese.

I am active in many Chinese communities, such as [juejin(掘金)][juejin], [Yuque(语雀)][yuque] and [bilibili(B站)][bilibili].

Here is a list of what I publish on these platforms:

## 周刊 & 教程

- [《一周一库》][fe-awesome]: 每周二更新，介绍前端领域的库、框架或工具
- [《一周前端技术分享》][fe-weekly]: 每周一更新，前端技术和其他
- [《现代 JavaScript 教程》][fe-javascript]: 翻译自 [javascript.info 站点][javascript.info]

## JavaScript

- 🎥 [手撕 Promise A/+ 实现（分四部分讲解）](https://www.bilibili.com/video/BV1dV4y1f7AP/)
  1. Promise API 介绍
  2. 基本功能实现：实现具备 `.then` 方法的 Promise 对象
  3. 异步功能支持：支持 `pending` 状态 `then` 回调函数的收集和异步调用功能（借助更精确的 `queueMicrotask` 而非 `setTimeout`）
  4. 链式调用支持：实现 `.then` 方法返回一个 Promise 对象的功能
- ES2016
  - [指数运算符（`**`）](https://juejin.cn/post/7216594811423834169)
    - 功能上 `**` 等价于 `Math.pow()`
  - [`Array.prototype.includes()`](https://juejin.cn/post/7218023263463702587)
    - 方法内部使用了 SameValueZero 算法，与 `.indexOf()` 不同之处在于 `[NaN].includes(NaN)` 判定结果为 `true`
- [ES6 `class X {}` 的 ES5 解释](https://juejin.cn/post/7212087651809787960)
  - 本质上就是构造函数的语法糖
- [ES6 `class X extends P {}` 的 ES5 解释](https://juejin.cn/post/7212576051166478394)
  - 内部执行步骤
    1. 将 `X.prototype` 的原型对象设置成 `P.prototype`
    2. 将 `X` 的原型对象设置成 `P`
    3. 执行 `P` 构造函数逻辑
    4. 执行 `X` 构造函数逻辑

## Node.js

- [图解：Node.js 事件循环系列](https://juejin.cn/post/7220352362798825509)（共 7 篇）
  - Node.js 事件循环比浏览器稍复杂些
  - 事件循环执行顺序
    - 微任务队列（microtask queue）→计时器队列（timer queue）→I/O 队列（I/O queue）→检查队列（check queue）→关闭队列（close queue）
    - 事件循环的开始、结束以及队列之间都会执行微任务队列，另外
    - 计时器队列/检查队列每执行完一次回调函数之后会执行微任务队列
- [`util.promisify()` 函数](https://juejin.cn/post/7216594811423539257)
  - 将基于回调的函数转换为基于 Promise 的，方法是通过代理最后一个 `callback` 回调参数

## React

- [React Hooks 内部工作原理](https://juejin.cn/post/7231106434834268221)
  - 没什么魔法，就是使用的数组 + 记录当前要访问的 Hook 的索引值（每次渲染完记得重置）
  - 基于实现方式，因此 Hook 严格依赖执行顺序，所有影响执行顺序的代码组织方式都会导致 BUG（比如：在条件语句或循环语句中使用），因此要求 Hook 要写在函数体顶层（top level）
- [修复 React `useEffect` 中的竞态条件问题](https://juejin.cn/post/7230350725460115514)
  - 这种情况还是蛮常见的，解决方案两个：一个是借助布尔标志 `ignore`，一个是 `AbortController` 的 `.abort()` 方法

## Vue

- [Vue3: 如何在 ref() 与 reactive() 中间做正确选择？](https://juejin.cn/post/7235118809605308471)
  - `ref(val)` 本质上就是 `reactive({ value: val })`，为了方便，我们应该地盲目地选择 `ref()` 而不是 `reactive()`

## TypeScript

- 🎥 [如何声明函数类型?](https://www.bilibili.com/video/BV1TV4y1r7yH/)
- 🎥 [如何编写声明文件?](https://www.bilibili.com/video/BV1ng4y1j7wA/)
- 🎥 [最常用的 12 种工具类型?](https://www.bilibili.com/video/BV1gL411Y7Mf/)

## 前端工程化

- [如何从零开始设置 webpack 5](https://juejin.cn/post/7215828320402817082)
  - webpack 5 是目前的最新版本，本文是特别适合小白的基础教程（基础概念、HTML &CSS 及 JavaScript 转译处理等）
- [模块打包器是什么，它是如何工作的？](https://juejin.cn/post/7214398563023142949)
  - webpack 和 rollup 是当天比较流行的打包器，本文分别概述了两者打包方式及区别
- [一步步教你如何编写自定义的 Babel 转换](https://juejin.cn/post/7214635327406211131)
  - Babel 是前端领域最常用的一个 JavaScrit 转译器，本文教你如何如果操作 AST 来编写自己的 Babel 插件
- [Koa 与 Express 的比较：多数场景下选择 Express 就对了](https://juejin.cn/post/7234057613776076857)
  - Express 是现在最流行的 Node.js Web 应用框架，Koa 是它的轻量级版本，相较前者没有内置路由、模板引擎等功能
- [最小化 JavaScript 中间件模式实现](https://juejin.cn/post/7214053344809861179)
  - 学习下 Koa 中间件系统是如何运作的（装 middlewares 的 `stack` + `runner(0)`）

## 其他

- 🎥 [网页开发技巧：移除网页图片的默认拖拽效果](https://www.bilibili.com/video/BV13L41167fe/)
- 🎥 [VS Code 中 5 个最常用的快捷键](https://www.bilibili.com/video/BV19a4y1M7aD/)
- 🎥 [VS Code 中使用 Live Server 插件实现本地网页实时预览](https://www.bilibili.com/video/BV1oa4y1M7pS/)
- 🎥 [Emmet 教程之 HTML 篇：快速构建你的HTML网页代码](https://www.bilibili.com/video/BV1HN411P7pH/)
- 🎥 [Emmet 教程之 CSS 篇：快速书写网页的 CSS 代码](https://www.bilibili.com/video/BV1684y1T7Bn/)

---

## 常用代码片段

```js
// 获取一个对象上所有的属性键。Symbol 和字符串，枚举和不可枚举
function getOwn(obj) {
    return Object.getOwnPropertyNames(obj).concat(Object.getOwnPropertySymbols(obj))
}

// 判定一个对象上是否包含指定属性键
Object.hasOwn(obj, propKey)
```

<!-- divider -->

[juejin]: https://juejin.cn/user/1363050148666824
[yuque]: https://www.yuque.com/zhangbao
[bilibili]: https://space.bilibili.com/629205276
[fe-weekly]: https://www.yuque.com/zhangbao/weekly
[fe-awesome]: https://www.yuque.com/zhangbao/awesome
[fe-javascript]: https://www.yuque.com/zhangbao/javascript
[javascript.info]: https://javascript.info/
