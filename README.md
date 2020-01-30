## 搭建项目过程  
### 1.使用npm进行全局安装koa-generator  
```
npm install -g koa-generator
```
----
### 2.使用koa-generator创建项目  
```
koa2 <项目名>
```
----
### 3.启动项目   
```
npm start (bin/www 文件有相关配置，如端口地址)
```  
----
### 4.设置层级路由  
app.js:  
```
var router = require('koa-router')();
var index = require('./routes/index');                  //子路由1
var users = require('./routes/users');                  //子路由2
app.use(router.routes()).use(router.allowedMethods());  //安装路由
router.use('/',index.routes());                         //安装子路由1
router.use('/users',users.routes());                    //安装子路由2
```
----
### 子路由1、2:  
```
var router = require('koa-router')();
router.get('/', function *(next) {
  yield this.render('index', {
    title: 'Hello World Koa!'
  });
});
module.exports = router;
```
----
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
### git常用命令  
```
git init
git add .
git commit -m '  '
git remote add origin [url]
git push origin master:master
```

清除缓存  
`git rm -r --cached .`
