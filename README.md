# 开发
npm run dev

# 编译
npm run pub

打开页面
1. 腾讯新闻主页
127.0.0.1:9000/index.html
2. 腾讯新闻spa页


# 多个页面的开发
* 添加html到src/目录下
* 在webpack.config.js文件里的的config.html添加对应的html名称，例子如下
```
var config = {
	html: ['index', 'spa'],
	/** other code */
};
```

# Devtools
ctrl + h进行切换
ctrl + q切换位置
其它命令可以参考src/page/common/DevTools
可以调defaultSize设置自己喜欢的大小
目前默认设置在底部，占30%的屏幕大小

# 文件目录
单页面文件可参考 src/page/index
单页应用可参考 src/page/spa


# 合图代码
请统一放在 src/page/xxx/container/xxx.scss中，可参考src/page/index里面的做法
这里的问题囿于插件局限性，之后建议找更好的插件，或者我们自己写一个

目前构建已经支持多个合图。只需要在src/img/sprites/下面新建文件夹，然后放在需要合的图，就会自动在src/css/文件夹下生成sprites/文件夹，里面包含了对应的合图和scss