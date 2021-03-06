# 图形客户端

V2Ray 项目组似乎对 GUI 不是很感兴趣，然而事实上有太多的人需要图形界面，于是催生了很多开发者开发 GUI 的 V2Ray 软件。在这些软件中，大部分其实只是一个图形界面而已，代理部分还是直接调用 V2Ray 内核的，其实这种图形界面和核心剥离开来分别开发是 V2Ray 项目组一早就设计好的。这种模式的优点是分工明确，总体效率高：V2Ray 只需处理代理协议，快速迭代；图形客户端只需处理好图形界面，跟进新功能，不必重写一遍代理的协议。其实这种模式在现代社会相当常见，比如说大家天天都在用的手机。

本节将简单介绍各个平台上的 GUI 客户端，由于这些客户端都不是由 V2Ray 项目组直接开发，所以有时也称为第三方客户端。注意，只是介绍而已，不是说明书也不是教程，并且带有**严重的主观倾向**，请理智看待。

-----
## Windows 平台

### V2Ray-Taskbar 

最早的客户端，非常简单，唯一的功能就是重启 V2Ray。在 V2Ray 面世的早期能有一个 GUI 客户端可以说明当时已经有人对 V2Ray 感兴趣，但早就不更新了。优点：功能简单；缺点：功能简单。

### V2Tray
 
他的出现是为了让 V2Ray 能够隐藏右下角的任务栏中，与 V2Ray-Taskbar 同时期，结果也一样。

### V2RayZero

后 V2Ray-Taskbar 的软件，他的出现标志着 V2Ray 可以通过图形化的方式配置 V2Ray 了。我只用过一次，不太记得了，配置界面好像一定程度上借鉴了 Shadowsocks-Windows。同样地，昙花一现。

### V2RayW

好像比 V2Zero 还早点。这位作者很良心，他已经不用 Windows 操作系统了，但还是装了虚拟机开发 V2RayW。作者很细心，看得出比较注重细节，不是那种“能用就行”心态。功能较少，对新功能的跟进稍慢一些，操作逻辑跟 Shadowsocks-Windows 差不多，至今还在更新。

### V2RayN

出生于 V2RayW 之后，公认的 Windows 上最易用的 GUI 客户端，摒弃了 Shadowsocks-Windows 的界面风格，新手操作友好。还制定了二维码和订阅的格式，便于机场用户使用。对配置处理得不好，对路由功能利用比较粗糙。

### V2RayGCon

比较特别的客户端，对于喜欢用一些 V2Ray 高级功能的用户来说这应该是最适合他的，可以同时满足图形化配置和高级自定义的需求，还有测试器等其他比较有特点的功能。不太适合小白，因为一些操作逻辑上跟他们平常用的软件不太一样。我认为这是 Windows 最好的 GUI 客户端，一是 V2Ray 内核契合最好的，二是有操作文档。

### 其他

其他的还有好几个，但是我都没用过就不提了。

-----
## Android 平台

### V2RayGo 

最早的 Android 客户端，一位从来没写过 Android app 的大佬现学现卖写的。要自己写配置文件，功能界面很简单。但意义非常重大，因为它携带着适用于 Android 的 V2Ray 内核(AndroidLibV2Ray)出现，从另一个角度看，可以认为它是 AndroidLibV2Ray 的演示。

### Actinium

一位医学大佬的作品，基于 AndroidLibV2Ray，重构了图形界面。用导入文件的方式加载配置，仍然需要自己写配置，但是操作上比 V2RayGo 简单还加入了分应用代理等。在当时来说用 V2Ray 的人基本上都会用 Actinium。结果也是弃坑。

### V2RayNG 

基于 Actinium，加入了图形化配置的方式，由于作者跟 V2RayN 的是同一人，也有订阅和二维码配置，对于多服务器和机场用户友好。特点与 V2RayN 一样，DNS 处理得也不好（早期测试，不清楚后来是否优化）。反正有订阅，机场喜欢，能用。

### BifrostV

前身是 Bifrost，一个包含代理协议但没有人见过的项目，后来发现 V2Ray 的模块化实现得比较完整就转身做 V2Ray 的 GUI客户端了。细节处理得很好，界面层次分明，又能与 V2Ray 的配置一一对应，有 V2Ray 完整的路由功能，还加入了额外的 DNS，使用体验不错。有广告，广告不是问题，问题是有时突然弹出全屏广告会造成心理上的错愕，氪金可解。综合地说，在 Android 上 BifrostV 使用体验最好。

-----
## iOS 平台

### ShadowRocket

最早的 iOS 客户端，考虑到平台限制，不像 Android 客户端那样直接调用 V2Ray 内核，所以在 ShadowRocket 上使用 VMess 协议其实跟用 ss 是一样的体验，代理协议不同而已。也正因为不是调用内核，ShadowRocket 支持的 V2Ray 特性非常少，关于 V2Ray 的新功能也几乎没有跟进速度可言。

### Pepi

与 ShadowRocket 师出同门，只支持 V2Ray，但对 V2Ray 支持的功能与 ShadowRocket 一样，所以众多网友更倾向使用 ShadowRocket，Pepi 已经快被大家遗忘在角落里了。

### Kitsunebi

直接使用 V2Ray 内核，对 V2Ray 的支持要好一些。由于 iOS 的原因，有时会有断流的现象。对不起！说错了，不关系统的事。

### Kitsunebi Lite

精简版的 Kitsunebi，主要是少了导入自定义 JSON 配置，其他的与 Kitsunebi 差不多。

### Quantumult

与 ShadowRocket 一样重写了代理协议，支持的特性有限。

-----
## MAC 平台

### V2RayX

V2RayW 的作者开发的，目前 MAC 上唯一的 GUI 客户端。没用过，不知怎样。

-----
（未完）
