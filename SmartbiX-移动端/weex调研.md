
#Weex调研
###weex的原理
js写原生app，js代码使用mvvm风格的Vue书写。
![](https://raw.githubusercontent.com/18511968604/blogPicture/master/flow.png)

###weex的生态现状
主要为阿里内部的一些实践，阿里内部双11主会场活动页面是用weex实现。阿里之外，生态不丰富。

###适用场景
阿里巴巴研发weex的目的：解决无线电商动态化问题，处理webView性能低，原生更新难的矛盾。
参考：https://github.com/amfe/article/issues/13

###weex的限制
1. Weex 环境中没有 DOM。Weex 的运行环境以原生应用为主，在 Android 和 iOS 环境中渲染出来的是原生的组件，不是 DOM Element。
2. 并不支持 Web 中所有的事件类型，不区分事件的捕获阶段和冒泡阶段，相当于 DOM 0 级事件。
3. Weex 环境中没有 BOM
4. 没有 window 、screen 、 document 对象
5. 阿里开源的项目口碑不太好，有断更风险。如果有bug，可能要得不到支持，要自行填坑。
参考http://weex.apache.org/cn/references/platform-difference.html

###简单总结weex的特点
js写原生，取得性能、热更新、跨平台的兼得，但阉割了很多前端能力，
本质上还是在写原生app，在界面简单，逻辑不多时，很适用。

###与Smartbi 移动端的适用性分析
Smartbi移动端的功能大致可以划分为以下三种情况：
1. 报表导航。（九宫格、列表）
2. 报表浏览。（webview打开前端报表）
3. 能力扩展。（SNS分享，语音识别）

对于报表浏览和能力扩展，weex无能为力。对于报表导航，如果用weex重构，可以提升性能。


