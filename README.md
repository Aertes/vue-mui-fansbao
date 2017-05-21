
##### 开发环境依赖模块说明

```
vue                            //构建用户界面的
vue-resource                   //vue 的http ajax请求插件（本项目没有用它，暂时保留）
vue-router                     //vue 路由插件
vue-html-loader                //vue html加载器
vue-loader                     //vue加载器
vue-style-loader               //vue的样式加载器
vue-template-compiler          //vue的模板编译器
vuex                           //组件状态管理
autoprefixer                   //css  浏览器兼容性问题处理
babel-core                     //ES6  代码转换器
babel-eslint                   //ES6的代码检查
babel-loader                   //ES6  代码转换器，webpack插件
babel-plugin-transform-runtime //和polyfill类似，替换助手函数
babel-preset-es2015            //ES6  代码编译成现在浏览器支持的ES5
babel-preset-stage-2           //ES6  ES7要使用的语法阶段
babel-register                 //用于改写require命令,为它加上一个钩子。此后,每当使用require加载.js、.jsx、.es和.es6后缀名的文件,就会先用Babel进行转码。
babel-polyfill                 //Babel默认只转换新的JavaScript句法（syntax），而不转换新的API，babel-polyfill就是为当前环境提供一个垫片。解决一些浏览器不能识别的语法，比如：Promise
cross-env                      //解决跨平台设置NODE_ENV的问题
css-loader                     //css  生成
less                           //css  预处理器less
less-loader                    //css  预处理器less的webpack插件
file-loader                    //webpack的文件加载器，主要用于字体  将字体文件打包
html-loader                    //webpack的html加载器，主要用于html文件的加载
html-webpack-plugin            //html  文件编译
jshint                         //Js代码检查工具
jshint-loader                  //webpack的jshint加载器，主要用于Js代码检查工具
style-loader                   //webpack的style加载器，主要用于css  插入到style标签
url-loader                     //webpack的url加载器，主要用于图片加载及限制
extract-text-webpack-plugin    //把额外的数据内容加到编译好的文件中 (独立打包样式文件)
webpack                        //用来构建打包程序
webpack-dev-server             //开发环境下，设置代理服务器
webpack-require-http           //webapck打包环境下的requrire加载http文件的插件
```

## 项目目录说明

```
|-- build                               // webapck打包后的文件目录
|-- logo                                // 存放app的图表地址目录
|-- src                                 // 源码目录
|   |-- components                      // 存放公共组件的目录
|       |-- member-qrcode.vue           // 会员二维码公共组件
|       |-- ...                         // 其他公共组件
|   |-- css                             // 存放各种css文件目录
|       |-- app.css                     // app的公用样式文件 
|       |-- icons-extra.css             // icons的扩展字体样式 
|       |-- mui.css                     // mui框架css
|       |-- ...                         // 其他css
|   |-- fonts                           // 存放各种fonts文件目录
|       |-- ...                         // 其他fonts文件
|   |-- imgs                            // 存放各种图片文件目录
|       |-- test                        // 存放开发测试的图片文件目录
|           |-- ...                     // 其他测试图片文件
|       |-- ...                         // 其他图片文件
|   |-- js                              // 存放各种js文件目录
|       |-- components                  // 存放各种js组件的目录
|           |-- app-routers.js          // 站点路由插件（只做路由的操作，不涉及实际的业务处理）
|           |-- signalR.js              // signalR组件
|           |-- ...                     // 其他JS组件
|       |-- config                      // 存放打包各种环境的目录
|           |-- DEV.js                  // DEV环境配置文件
|           |-- GQC.js                  // GQC环境配置文件
|           |-- PRD.js                  // PRD环境配置文件
|           |-- ...                     // 其他环境配置文件
|       |-- lib                         // 第三方JS lib目录
|           |-- mui.js                  // mui插件
|           |-- ...                     // 其他第三方JS插件
|       |-- services                    // app自己的业务目录
|           |-- global-service.js       // APP 全局业务逻辑方法，主要处理登录、登出的业务逻辑
|       |-- store                       // vuex管理webApp的数据状态目录
|           |-- index.js                // app数据管理入口文件
|           |-- app-data.js             // app临时数据管理
|           |-- app-event.js            // app事件管理
|           |-- router-status.js        // app路由状态管理
|       |-- utils                       // app的存放工具
|           |-- directives.js           // vue 自定义指令文件
|           |-- log.js                  // app log日志
|           |-- update.js               // app在线更新
|           |-- utils.js                // app站点页面表单验证框架工具类
|           |-- ....                    // 其他工具JS文件
|   		|-- app.js                      // app配置以及其他方法
|   		|-- entrance.js                 // app程序入口文件，加载各种公共组件
|   		|-- routers.js                  // vue的路由配置文件
|   |-- json                      			// 测试的json数据存放目录
|   |-- less                      			// 存放各种less文件的目录
|   		|-- app.less                    // app基础样式，包含其他less文件的入口
|   		|-- ...                         // 其他less样式文件
|   |-- views                      			// 存放各种页面视图组件目录
|   		|-- error                       // 存放错误视图组件目录
|   				|-- 404.vue                 // 404页面视图
|   		|-- users                      	// 存放用户的视图组件目录
|   				|-- login.vue               // 登录页面
|   				|-- user-center.vue         // 用户中心页面
|   				|-- welcome.vue         		// 欢迎页面
|   				|-- ...         		// 其他视图页面
|   		|-- ...                     // 其他功能模块目录
|   		|-- app.vue                     // app页面入口文件
|   		|-- barcode.vue                 // barcode页面入口文件
|   		|-- home.vue                    // app首页面
|   |-- index.html                      // app的html模板页面
|-- unpackage                           // app编译包目录
|-- .babelrc                            // ES6语法编译配置
|-- .editorconfig                       // 编辑器编码规范配置
|-- .gitignore                          // git忽略文件
|-- index.html                          // webapp的首页加载文件
|-- manifest.json                       // 打包app的配置文件
|-- package.json                        // 配置项目相关信息，通过执行 npm init 命令创建
|-- webpack.config.js                   // webpack配置文件
```

## 运行程序

通过`npm`安装本地服务第三方依赖模块(需要已安装[Node.js](https://nodejs.org/))

```
npm install
```
启动DEV服务(http://localhost:8083)

```
npm run R_DEV (window)
npm run MR_DEV (MAC)
```
打包发布DEV代码

```
npm run B_DEV (window)
npm run MB_DEV (MAC)
```
