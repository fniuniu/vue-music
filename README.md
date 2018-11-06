# vue-music

> A Vue.js project

问题一、npm err 无法安装node_modules
解决：直接用命令清理缓存，控制台输入：npm cache clean --force

问题二、目录
  assets里面的会被webpack打包进你的代码里，而static里面的，就直接引用了。一般在static里面放一些类库的文件，在assets里面放属于该项目的资源文件。简单的讲，static放别人家的，assets放自己写的
src下创建
1.api//与后端相关代码  ajax jsonp
2.common//通用字体 图片  样式
  fonts
  image
  stylus
3.components //公用vue组件
4.router //router相关
5.App.vue //主页
6.main.js //主页相关
7.store //vue 的代码

问题三、stylus //CSS预处理器框架 其他还有sass/less
npm install stylus stylus-loader -D
在main.js中引入import './common/stylus/index.styl'
在组件中
<style scoped lang="stylus" rel="stylesheet/stylus">
@import "./common/stylus/variable"

1.variable.styl 设计规范 自定义
2.base.styl  引入variable.styl
3.reset 重置样式
4.index.styl 先引入重置样式
5. mixin和variable 不在index中引入，用到时才用
6.mixin 定义函数

问题四、npm install babel-runtime -D //es语法转译
npm install fastclick  -D //解决移动端点击300ms 点击延迟问题,写在在main.js 引入fastclick.attach(document.body)
npm install babel-polyfill -D //ES6 API转译，Promise，写在main.js最上面

问题五：webpack.base.conf中alias 目录简写
