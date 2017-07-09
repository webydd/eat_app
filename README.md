# eat_app
# 这是一个React app demo
----------------------------------------------------------------------------------------------------------------------------------
## react技术栈
- react react-router4 redux react-redux

## 初始化package.json
```
$ yarn init -y
```
## webpack
```
$ yarn add webpack webpack-dev-server --dev
```
## babel
```
$ yarn add babel-core babel-loader babel-preset-es2015 babel-preset-stage-0 babel-preset-react css-loader style-loader less less-loader html-webpack-plugin --dev
```
## react
```
$ yarn add react redux react-redux react-router-dom  react-dom(渲染到dom)
```
## fetch  (前端获取后台数据)
```
$ yarn add es6-promise whatwg-fetch --dev
```
## express
```
$ yarn add express 
```
## scripts
```
"start","webpack-dev-server --port 5000 --open --progress --colors",
"build","webpack -p"(p打包)
```

### 目录结构
- components 组件   木偶组件
- containers 页面组件，或者自己的subpage页面下
   - Home
       - subpage   智能组件
       -index.js
       
       
- index.js 用来操控哪个页面

#### redux

- store onlyOne
- action 用户发布动作（改变redux的状态
- reducer 定义规则的
- action-types action的名字
### 引入轮播图的插件
```
yarn add swipe-js-iso react-swipe
```
```
<ReactSwipe className="carousel" swipeOptions={{continuous: false}}>
                <div>PANE 1</div>
                <div>PANE 2</div>
                <div>PANE 3</div>
            </ReactSwipe>
```
- continuous: false 轮播到末尾不能继续滑动


- 404 或者 504 是因为服务端没重启或者数据没有拿回来导致的

### connect
- connect 是负责把redux里面的状态和动作以属性的方式传给react (中间件)
```
import {connect} from 'react-redux';
```

### 获取当前元素的位置离屏幕顶端的距离，  可以上下左右
```
getBoundingClientRect().top;// 不兼容
```

### refs.属性值 指定某一个特定的dom元素
```
在react里
<div ref="more"></div>
在方法中 this.refs.more 就指这个div
```
```
this.refs.more.getBoundingClientRect().top
```

### routes
```
/detail/:id    :id表示必须有可以不写
:route?        可有可无
```

### 
```
   {/*将内容转换成html插入到页面中*/}
                <div dangerouslySetInnerHTML={{__html:desc}}></div>
```


### redux 插件 Redux DevTools 在redux里的配置
```
createStore(reducers,initState,window.devToolsExtension?window.devToolsExtension():undefined);
```


### 用于接收请求体的数据 body-parser
```
let bodyParser = require('body-parser');
app.use(bodyParser.urlencoded({extended:true}));
```

### 移动端弹性盒模型:
- display:flex;
- justify-content: space-around;/*水平居中*/
- justify-content: space-between;/*水平分布*/
- align-items:center; 垂直居中
