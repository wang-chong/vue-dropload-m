# vue-dropload-m


> 基于vue实现的移动端下拉刷新、上拉加载更多组件

## use

import 'dropload' from 'vue-dropload-m'
Vue.use(dropload)

## code
<code>&lt;div&gt;<br />
<span style="white-space:pre;"> </span>&lt;dropload ref="drop" :loadUpFn="reFreshData" :loadDownFn="getMoreData"&gt;<br />
<span style="white-space:pre;"> </span>&lt;div v-for="item in datalist" class="list"&gt;<br />
<span style="white-space:pre;"> </span>&nbsp; <span style="white-space:pre;"> </span>我是内容{{item}}！！！<br />
<span style="white-space:pre;"> </span>&lt;/div&gt;<br />
<span style="white-space:pre;"> </span>&lt;/dropload&gt;<br />
&lt;/div&gt;<br />
  </code>

## props

### loadUpFn(function)
下拉刷新函数，获取数据渲染之后运行该组件的resetUp方法（必须）进行恢复状态

### loadDownFn(function)
上拉刷新函数，获取数据渲染之后运行该组件的resetDown方法（必须）进行恢复状态


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
