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