# Hello World Render

从最简单的Hello World开始说起。

React的Hello World极其简单，只需要思行代码就可以搞定。例如：

```js
//index.js
import React from "react";
import ReactDOM from "react-dom"
const App = () => "Hello World"; 
ReactDOM(<App />,document.querySelector(".app"));
```

`import`是`es6`新出的一个模块导出方法，