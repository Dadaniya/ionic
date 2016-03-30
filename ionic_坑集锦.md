##ionic 坑集锦
### android
1. 配置环境

```
error: plase install android-23
=》在项目里改下project.poperties中的target改成你的，androidManifest也改
=》更改build-tools目录，样式为22.0.1而不是android-6
```

###OS X
1. 很多命令加sudo（此处有坑，下面解释）
2. ionic emulate出错解决办法

```
通过ios-sim --verison查看你所支持的name（或通过XCODE的window=>devicer看）
执行命令大坑：projectName/platforms/ios/cordova/lib/run.js中43行定义了validTargets，及检索规则。
```
**如果以上还解决不了，两下两方法换着用**：

```
=>删了resources文件夹，重新add ios..
=>删了resources文件夹,更改project读写权限 chown -R /Users/name Target,然后不用sudo命令
```

[持续更新](https://github.com/Dadaniya/ionic)