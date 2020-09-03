# vue-webpack-template

> vue+webpack+webpack单页应用开发脚手架
git地址：[vue+express+webpack](https://github.com/HEJIN2016/vue-webpack-template)，求star

### webpack优化点
1.引入happypack，实现webpack多线程打包，显著提高本地打包速度；

2.引入webpack DllReferencePlugin，提前打包公共代码（polyfill和vue全家桶），提高构建速度；

3.支持less、sass，支持postcss配置，自动引入polyfill（可删除）；

3.手动搭建webpack脚手架，脱离vue-cli，可自我根据需要自定义调整webpack配置；



### 技术栈

webpack4 + Es6 + vue

### 运行

```
#下载工程
git clone https://github.com/HEJIN2016/vue-webpack-template

cd vue-webpack-template

#安装依赖
npm install

#打包lib
npm run postinstall

#本地开发
npm run dev

#本地打包
npm npm build

#线上打包
npm npm build-project

#访问地址
http://localhost:3200
```

### npm脚本介绍
```
#打包lib（npm install时自动调用该钩子）
npm run postinstall

#执行webpack.dll.js，打包lib
npm run build-lib

#本地运行
npm run dev


```

### 目录结构
```txt
  ├── build                       // webpack配置
  │   ├── webpack.client.js       // webpack client端打包配置
  │   ├── webpack.dll.js          // webpack DllPlugin打包配置
  ├── lib                         // DllPlugin 相关lib
  ├── src                         // 源代码
  │  ├── assets                   // 静态资源
  │  ├── components               // 公用组件
  │  ├── layout                   // 布局组件
  │  ├── views                    // 页面路由组件
  │  ├── stores                   //  store，状态管理
  │  ├── tool                     // 通用公共函数
  │  ├── index.html               // html模板
  │  ├── main.js                  // 入口
  ├── static                      // 静态文件目录
  ├── babele.config.js            // babel-loader 配置
  ├── config                      // 工程全局公共配置（port、host等）
  ├── postcss.config.js           // postcss-loader 配置
  ├── .editorconfig               // 编辑器配置
  ├── .gitignore                  // git 忽略项
  ├── package-lock.json           // npm 锁文件
  ├── package.json                // npm 配置
  ├── README.md                   // README 文档
```
