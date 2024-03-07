# Vue实战

## package.json
 - dependencies（生产环境依赖）:
    - 这个字段包含了项目在运行时所需的依赖项，即在部署和生产环境下需要的模块或库。
    - 当使用 npm install 安装包时，这些依赖项会被安装。
    - 通常包括项目的主要依赖，比如框架、库以及其他必要的模块。
 - devDependencies（开发环境依赖）:
    - 这个字段包含了仅在开发过程中需要的依赖项，例如测试框架、构建工具、代码检查工具等。
    - 当运行 npm install --only=dev 或 npm install --dev 时，只会安装这些依赖项。
    - 这些依赖通常不会被包含在生产环境的构建结果中。
在实际项目中，将开发和生产环境的依赖项分开可以帮助减少部署时不必要的依赖，提高生产环境的性能和安全性。

## 工程化相关
 - vite：打包工具
 - lint-staged：校验相关
 - cspell：拼写检查
 - commitizen：commit检查
 - cz-git：提交的快捷处理
 - husky：git提交拦截
 - zx：写js脚本
 - tsno：就是ts-node

## 规范约束
 - 代码相关约束：js、ts、style
 - 单词拼写规范
 - git提交规范（git flow）有哪些分支，每个分支含义，发布流程是什么？

## 路由
现在一般不用哈希路由了，因为哈希路由有太多问题了，比如说想要重构成ssr以及做权限和资源管理会很麻烦，现在一般用内存路由和BrowserRouter

## 可以用策略模式抹平端的差异

## 插件机制
vue必须提供一个install方法才可以用的，在这个install方法中可以拿到vue的实例（app）

## 本地持久化
通常，我们在前端可以临时缓存数据，而后通过更新队列将数据同步至后端服务。本地存储通常采用的方案有：
1. localstorage
2. indexedDB
3. webSQL，已废弃，不用了解

通常小数据量可以直接选用 localStorege，但是需要注意的是其数据序列化与反序列化的实现。（）
对于较大数据量，我们可以选用 indexedDB，当然直接操作会略微有点麻烦，我们可以选择使用 Dexie https://github.com/dexie/Dexie.js

indexedDB + service worker 就能实现本地离线应用

## webpack的treeshaking
treeshaking的前提条件：ESmodule

## 图表渲染器
用来做大屏类的项目一般选用d3+svg，一般用svg做渲染的时候选择使用d3进行封装处理；
数据量比较大、3d的比较炫酷的就用canvas；

## echarts双引擎
echarts底层用的是zrender

## 专业术语
图表渲染器、图表数据格式化器、数据校验器、数据协议、组件通用协议、组件数据协议、图表数据协议