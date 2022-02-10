---
title: 在 React Native 项目中使用 FinClip 小程序容器遇到的坑
date: 2022-02-10 14:21:54
tags:
---
## 起因

因为在鹿山App使用 React Native 框架的项目的各种活动更新要求很频繁，对于开发效率和上线频率要求就很高，但是每次都提交一次版本会导致用户体验大打折扣，热更新的局限性太大，就考虑采用 小程序容器 的解决方案。

## 选品

小程序容器解决方案有考虑到两个选品，分别是 FinClip 和 OpenApplus。
<!-- more -->
相比 FinClip，OpenApplus 的开发、接入文档有些潦草，并不全面，为了方便后期的开发，选择了 FinClip。

## FinClip 的坑

### FinClip 提供的 IDE

虽然 FinClip 提供了 IDE，但还是建议在 VSCode 里配置好小程序开发用的插件。因为 FinClip 提供的 IDE **不支持代码提示补全......**
可以把 FinClip IDE 理解为快速生成符合 FinClip 小程序的调试工具，仅此而已。

### FinClip 的文档

FinClip 官方提供了 React Native 项目的接入文档，但是并不全面。特别是在官方的 React Native 项目集成文档中出现了“在 ```main.dart``` 文件中增加以下小程序引擎初始化方法。”（如图下）

![文档截图](https://api-serv.tzih.top/blog_res/202202101323469.png)对于没有 ```main.dart``` 的 RN 项目，我最后通过分析官方提供的 React Native Demo 才完成 SDK 集成。

集成了 SDK 后整个流程也十分顺利，不过官方对于 RN SDK 的态度是有些“摆烂”的，很多特性都没有针对 RN 做单独说明或者文档。

这是通过工单与官方沟通的记录，仅供参考：![工单回复截图](https://api-serv.tzih.top/blog_res/202202101410599.png)



（完）