Language: [English](README.md) | [中文简体](README-ZH.md)

<p align="center">
  <img src="https://s1.ax1x.com/2018/12/29/FfM6Yt.png" alt="FfM6Yt.png" border="0" />
</p>

## V2LF

[![LICENSE](https://img.shields.io/badge/license-GPL%20v3.0-blue.svg?style=flat-square)](https://github.com/w4mxl/V2LF/blob/master/LICENSE)

`V2LF` 是一个 v2ex 技术社区的第三方 app。
**'V2LF' 名字是取 'way to love flutter' 的缩写。**
开发这个 app 的初衷是想在实战中学习 Flutter。

在 v2ex 网站功能基础上，V2LF 希望进一步扩展出更多有趣功能的 app。目前已经新增有：

- 夜间模式
- 往期热点
- 近期已读
- 主题切换
- 高效搜索
- 只看楼主


[![Get it from iTunes](https://lisk.io/assets/svg/download_on_the_app_store_badge.svg)](https://apps.apple.com/cn/app/v2lf/id1455778208?mt=8) [![Get it on Google Play](https://lisk.io/assets/svg/download_on_the_play_store_badge.svg)](https://play.google.com/store/apps/details?id=io.github.w4mxl.v2lf)

## 截图预览

![](https://i.loli.net/2019/08/19/NQVUa8p13GZdSxt.jpg)
![](https://i.loli.net/2019/08/19/CTg61O7XNWtb9V2.jpg)


## 编译运行

### 缺失 Key.Properties 文件

下载源码后首次运行，您将会收到一个错误，提示缺少 key.properties 文件。
请通过下面步骤解决这个问题，

1.  打开 V2LF\android\app\build.gradle 文件，然后参考下面，注释掉其中一些代码

```
//keystoreProperties.load(new FileInputStream(keystorePropertiesFile))

signingConfigs {
// release {
// keyAlias keystoreProperties['keyAlias']
// keyPassword keystoreProperties['keyPassword']
// storeFile file(keystoreProperties['storeFile'])
// storePassword keystoreProperties['storePassword']
// }
}
buildTypes {
// release {
// signingConfig signingConfigs.release
// }
}
```

2.  打开 V2LF\android\local.properties ，然后在最后添加下面几行代码：

```
flutter.versionName=1.0.0
flutter.versionCode=1
flutter.buildMode=release
```

### 开发环境

这个项目目前是在 Flutter Dev 分支 + Dart 2 环境下开发的，每次 Flutter SDK 升级后也会做相应的适配和兼容。
想正常编译运行此项目，请先确定您已经正确配置好 Flutter 开发环境。

## 后续开发

如您对此项目进展有兴趣，请通过关注 [trello](https://trello.com/b/YPOJsfQx/v2lf) 来追踪最新动态。

## 相关链接

- [邀请体验： V2LF - 用 Flutter 开发的 V2EX App](https://www.v2ex.com/t/548936#reply169)
- [V2LF - 使用 Flutter 开发的开源的 V2EX 客户端](https://www.v2ex.com/t/563913#reply57)

## 代码许可

[GPL v3.0 License](https://www.wikiwand.com/zh/GNU%E9%80%9A%E7%94%A8%E5%85%AC%E5%85%B1%E8%AE%B8%E5%8F%AF%E8%AF%81)
