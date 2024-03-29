# 尚硅谷实战项目——尚品汇

# DAY-1

## Vue-cli脚手架初始化项目

node+webpack+淘宝镜像

- `node_modules`文件夹：项目依赖文件夹
- `public`文件夹：一般放置一些静态资源（图片），需要注意，放在public文件夹中的静态资源，webpack进行打包的时候，会原封不动打包到dist文件夹中。
- `src`文件夹（程序员源代码文件夹）：
- `assets`文件夹：一般也是放置静态资源（一般放置多个组件共用的静态资源），需要注意，放置在assets.文件夹里面静态资源，在webpack打包的时候，webpack会把静态资源当做一个模块，打包JS文件里面。
- `components`文件夹：一般放置的是非路由组件（全局组件）
- `App.vue`: 唯一的根组件，Vue当中的组件(.vue)
- `main.js`: 程序入口文件，也是整个程序当中最先执行的文件
- `babel.config.js`: 配置文件(babel相关)
- `package.json`文件：认为项目‘身份证'，记录项目叫做什么、项目当中有哪些依赖、项目怎么运行。
- `package-lock.json`: 缓存性文件
- `README.md`: 说明性文件

## 项目的其他配置

### 项目运行起来的时候，让浏览器自动打开

```jsx
--package.json  文件中
"scripts":{
	"serve":"vue-cli-service serve **--open**",
	"build":"vue-cli-service build",
	"lint":"vue-cli-service lint"
}
```

### ESlint 校验功能关闭。

在根目录下，创建一个`vue.config.js`
比如：声明变量但是没有使用es1int校验工具报错。

```jsx
module.exports = {
	//关闭eslint
	lintonSave:false
}
```

### src文件夹简写方法，配置别名。

根目录下创建`jsconfig.json`文件，配置别名@提示。@代表src文件夹

```jsx
{
  "compileroptions": {
    "baseUrl": "./",
    "paths": {
      "@/": ["src / "]
    }
  },
  "exclude": ["node modules", "dist"]
}
```

## 项目路由的分析 vue-router

前端所谓路由：KV键值对。

`key`:  URL(地址栏中的路径)

`value`:  相应的路由组件