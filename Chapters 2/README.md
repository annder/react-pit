# React 组件

[] 状态组件

[] 无状态组件

[] HOCT组件

[] 嵌套组件

[] 组件通信

[] 生命周期组件

[] 无父节点组件

[] 字符串组件

组件的写法分为两种。一种是函数式组件，类组件：


```js
//functionals component

const Comit = ()=> <h1>Hello World</h1>;  

//Class Component:

class App extends Component {
    render (){
        <h1>Hello World</h1>
    }
}

```

状态组件：

状态组件就是有state的组件,使用class 写的组件:

```js
 class App extends Component {
     constructor (props){
         super(props);
         this.state = {
             data:"Hello World"
         }
     }
    render (){
        return (<h1>
                {this.state.data}
            </h1>)
    }
 }
```

无状态组件就是Functional Component :

```js
const App = () => <h1>Hello World</h1>
```

---

子节点向父节点通信：


```js
    class App extends Component {
        constructor (props){
            super();
            this.state({
                data:"hello"
            })
        }
        render (){
            const {data} = this.state;
            return [
                <div>   
                {data}
                    <button onClick={()=> this.setSate({
                        data:"name"
                    })}>x</button> 
                </div>
            ]
        }
    }
```