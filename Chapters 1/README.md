# Hello World Render

从最简单的Hello World开始说起。

React的Hello World极其简单，只需要几行代码就可以搞定。例如：

```js
import React from "react";
import ReactDOM from "react-dom"

const App = () => "Hello World"; 

ReactDOM.render(<App />,document.querySelector(".app"));
```

**react这个文件是必备的，因为是React框架的核心**。

`import`是`es6`新出的一个模块导出方法。

意思就是，将`React`和`ReactDOM`全部导入到此文件中。

当然如果每次写`ReactDOM.render()`会很麻烦，还有一个更加便捷的方法，那就是将ReactDOM的render直接导入进文件：


```js
import React from "react";
import ReactDOM ,{render} from "react-dom";

render(<App />,document.querySelector(".app"));
```

带有`JSX`的Hello World：

```js
    render(<h1>HELLO WORLD</h1>,document.querySelector(".app"));
``` 

**不要将组件渲染到body节点上。如果有动态脚本在此节点内的话，React的计算会变困难。**

## render上的回调函数：

一个例子：

```js
render("Hello World",document.querySelector(".app"),()=>{
    alert("Hello World");
});
```

根据JavaScript上的callback函数的特性，当"Hello Wolrd"渲染到.app这个节点的后，调用回掉函数。
