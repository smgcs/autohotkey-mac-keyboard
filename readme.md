# 基于 AutoHotKey 的键位优化方案

## 背景

白天在公司使用公司提供的 MacBook Pro 工作，晚上回家使用神舟 Z7M 学习和工作。一个系统是 OS X，一个是 Windows，两个系统的键位区别还是挺大的。本项目旨在尽可能的统一两个系统下的键位，做到无缝的切换。

## 分析

OS X 的键位比较适合编程人员，譬如 『Ctrl + A』等同于『HOME』等。另外，『Command』键的引入，对左手小拇指压力减轻不少，同时发挥了左手拇指的作用。

Windows 下的快捷键乏善可陈，『Ctrl』、『Shift』需要经常蜷缩左手小指，『Win』键出了全局系统热键（『Win + R』、『Win + E』）外，无法被应用程序捕获，无法正常使用，『Alt』键被系统菜单接管。

故 OS X 的键位相对更合理一下，我们的目标就是调整 Windows 下的键位。

## 方案

『AutoHotKey』是 Windows 下著名的改键工具，本方案采用 AutoHotKey 作为改键软件。

1. 更换 『Alt』键和『Win』键：采用注册表的方式，可以减少 AutoHotKey 的改动量。
2. 『Win』键由于无法被应用程序正常捕获，所以需要在应用程序中将快捷键改为 『Ctrl + Shift + Alt + ?』的方式。
3. 采用全局钩子的方式，截获『Win』键等特殊键位。

下载https://www.autohotkey.com/download/ahk-install.exe,安装转化器，打开安装目录+\Compiler\Ahk2Exe.exe

![](.\示例.PNG)