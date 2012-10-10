自动依赖分析器
===
项目的目标是创建一个小程序，自动帮用户分析出一个项目中所require的模块，以帮助用户编写出精确的`package.json`文件的dependencies和devDependencies属性。

## 实现思路
通过扫描目录中的js文件，正则表达式匹配require调用，提取出项目中require到的所有模块。并且排除掉Node的原生模块、文件模块，提取出依赖的第三方模块。并自动从NPM服务器上查看最新的版本以提供一个推荐的依赖列表。  

## 求谁来帮忙实现
哥太忙了。求对Node感兴趣的人来帮忙实现下。可以玩玩分析文本文件。项目完成后，**奖励两本图灵社区的书**。

##使用

```
var dp=require("dependparser")
dp(process.cwd()) //结果会显示在终端上，如果npm info 请求失败，版本会为空
```
