### 初始化项目 

`npm i` 或者 `yarn`

### 启动项目 

`npm start` 

- 设置环境：通过 `__ENV__` 可以设置不同的开发环境
  ```
  __ENV__=PROD npm start
  ```
- 设置端口
  ```
  PORT=5033 npm start
  ```

### 打包项目 

`npm run build`

- 设置环境
  ```
  __ENV__=PROD npm run build
  // 指令等同👆的效果
  npm run build:prod
  ```

#### 支持的 CMD 指令参数

- 环境变量 `__ENV__`
  
  在 cmd 指令上添加 `__ENV__=?` 后 webpack.DefinePlugin 会 在 js 的全局作用域里添加 `__ENV__` 

- 端口 `PORT`

  设置 debug 模式下的网站端口  

#### webpack 配置常量

在 `webpack/constants.js` 下可以修改常量

### 项目结构说明

```
├── src/
│   ├── commons/ 
│   │   ├── assets/ 静态资源目录
│   │   ├── styles/ 公共样式目录
│   │   ├── utils/ 公用方法目录
│   │   ├── constants.ts 项目常量配置
│   │   └── history.ts 项目使用的 history
│   ├── components/ 组件目录
│   ├── locales/ 国际化文件目录
│   ├── pages/ 页面目录
│   ├── services/ 
│   ├── index.html 网站页面模版
│   ├── index.scss 项目样式入口
│   ├── index.tsx 项目 js 入口
│   ├── router.tsx 项目的路由配置
│   └── ...
├── webpack/
│   ├── build.js 项目打包模式下的 webpack 配置
│   ├── constants.js webpack 配置常量
│   ├── debug.js 项目开发模式下的 webpack 配置
│   └── getConfig.js 获取公共的 webpack 配置
├── .gitignore
├── babel.config.js
├── index.d.ts
├── package.json
├── READEME.md
└── tsconfig.json
```
