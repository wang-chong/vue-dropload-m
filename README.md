# vue-dropload-m


> 基于vue实现的移动端下拉刷新、上拉加载更多组件

## use

import 'dropload' from 'vue-dropload-m'
Vue.use(dropload)

## code
<code>%3Cdiv%3E%09%3Cdropload%20ref=%22drop%22%20:loadUpFn=%22reFreshData%22%20:loadDownFn=%22getMoreData%22%3E%09%09%3Cdiv%20v-for=%22item%20in%20datalist%22%20class=%22list%22%3E%09%09%20%20%09%E6%88%91%E6%98%AF%E5%86%85%E5%AE%B9%7B%7Bitem%7D%7D%EF%BC%81%EF%BC%81%EF%BC%81%09%09%3C/div%3E%09%3C/dropload%3E%3C/div%3E</code>

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
