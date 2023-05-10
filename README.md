# Zhang Bao's Personal Website

Hello, My Chinese name is "张宝". I am a front-end development programmer (more than 6 years of experience)from Shanghai, China. I usually write in Chinese.

I am active in many Chinese communities, such as [juejin(掘金)][juejin], [Yuque(语雀)][yuque] and [bilibili(B站)][bilibili].

Here is a list of what I publish on these platforms:

## 周刊 & 教程

- [一周前端技术分享][fe-weekly]
- [《现代 JavaScript 教程》][javascript.info]

## JavaScript

- 🎥 [手撕 Promise A/+ 实现](https://www.bilibili.com/video/BV1dV4y1f7AP/)
- ES2016
  - [指数运算符（`**`）](https://juejin.cn/post/7216594811423834169)
    - 功能上 `**` 等价于 `Math.pow()`
  - [`Array.prototype.includes()`](https://juejin.cn/post/7218023263463702587)
    - 方法内部使用了 SameValueZero 算法，与 `.indexOf()` 不同之处在于 `[NaN].includes(NaN)` 判定结果为 `true`
- [ES6 `class X {}` 的 ES5 解释](https://juejin.cn/post/7212087651809787960)
  - 本质上就是构造函数的语法糖
- [ES6 `class X {} extends` 的 ES5 解释](https://juejin.cn/post/7212576051166478394)
  - 内部执行步骤
    1. 将 `X.prototype` 的原型对象设置成 `P.prototype`
    2. 将 `X` 的原型对象设置成 `P`
    3. 执行 `P` 构造函数逻辑
    4. 执行 `X` 构造函数逻辑

## Node.js

- [图解事件循环系列](https://juejin.cn/post/7220352362798825509)（7 篇）
  - Node.js 事件循环比浏览器稍复杂些
  - 事件循环执行顺序
    - 微任务队列（microtask queue）→计时器队列（timer queue）→I/O 队列（I/O queue）→检查队列（check queue）→关闭队列（close queue）
    - 事件循环的开始、结束以及队列之间都会执行微任务队列，另外
    - 计时器队列/检查队列每执行完一次回调函数之后会执行微任务队列
- `util.promisify()` 函数
  - 将基于回调的函数转换为基于 Promise 的，方法是通过代理最后一个 `callback` 回调参数

## React

- [React Hooks 内部工作原理](https://juejin.cn/post/7231106434834268221)
  - 没什么魔法，就是使用的数组 + 记录当前要访问的 Hook 的索引值（每次渲染完记得重置）
  - 基于实现方式，因此 Hook 严格依赖执行顺序，所有影响执行顺序的代码组织方式都会导致 BUG（比如：在条件语句或循环语句中使用），因此要求 Hook 要写在函数体顶层（top level）
- [修复 React `useEffect` 中的竞态条件问题](https://juejin.cn/post/7230350725460115514)
  - 这种情况还是蛮常见的，解决方案两个：一个是借助布尔标志 `ignore`，一个是 AbortController 的 `.abort()` 方法

## TypeScript

- 🎥 [如何编写声明文件?](https://www.bilibili.com/video/BV1ng4y1j7wA/)
- 🎥 [最常用的 12 种工具类型?](https://www.bilibili.com/video/BV1gL411Y7Mf/)

## 其他

- 🎥 [VS Code 中 5 个最常用的快捷键](https://www.bilibili.com/video/BV19a4y1M7aD/)
- 🎥 [VS Code 中使用 Live Server 插件实现本地网页实时预览](https://www.bilibili.com/video/BV1oa4y1M7pS/)
- 🎥 [Emmet 教程之 HTML 篇：快速构建你的HTML网页代码](https://www.bilibili.com/video/BV1HN411P7pH/)
- 🎥 [Emmet 教程之 CSS 篇：快速书写网页的 CSS 代码](https://www.bilibili.com/video/BV1684y1T7Bn/)

<!-- divider -->

[juejin]: https://juejin.cn/user/1363050148666824
[yuque]: https://www.yuque.com/zhangbao
[bilibili]: https://space.bilibili.com/629205276
[fe-weekly]: https://www.yuque.com/zhangbao/weekly
[javascript.info]: https://www.yuque.com/zhangbao/javascript
