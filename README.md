# 游戏手柄指令显示面板
本项目的开发基础是`gamepadviewer.com`，以资源本地化和使用便利性为核心目标，创建更能配合国内游戏直播需求的辅助工具。
本应用程序提供的虚拟手柄面板与直播软件捕获的游戏画面组合，使观众更容易理解主播对游戏的操作，提升直播中的交互效率。


## 原理简介
本应用程序利用`Chrome`原生支持游戏手柄指令的特性，构建可视化的虚拟游戏手柄面板来显示实时的操作指令。
直播软件 [OBS Studio] 自带的 [Browser] 插件本质上是一个基于 Chrome 内核的网页浏览器外壳；
因此，只要在 OBS 中添加一个 `浏览器` 组件，就相当于在直播画面中常驻了一个微型的 Chrome 窗口，设定好来源 URL，使其显示本应用程序的画面。
**本程序绿色、安全，无需安装任何额外软件，无需修改任何系统设置，无需额外权限；特别适合洁癖主播。**  


## 主要功能特性
> 1. 支持 Xbox 手柄面板和实时指令显示；
> 2. 支持 PlayStation 手柄面板和实时指令显示；
> 3. 支持 `OBS Studio Browser Plugin` 插件整合 `Open Broadcaster Software (OBS)` 直播推流；
> 4. 支持 `Chrome 浏览器` 测试手柄；
> 5. 高实时性：纯客户端应用，启用后在本地运行，不依赖服务器和网络；
> 6. 高扩展性：跟随 Chrome 内核升级可原生支持更多手柄类型；
> 7. 高兼容性：支持所有主流直播平台。  

![使用 Chrome 打开主页](images/home.jpg)
  
  
  
## OBS 直播手柄面板使用步骤
1. 将游戏手柄连接到计算机。参考下述连接方式：

|手柄类型              |有线连接    |蓝牙连接    |适配器连接   |
|-------              |-------    |-------    |-------     |
|Xbox 全系列手柄       |支持        |支持       |支持         |
|DualShock 5          |支持        |支持       |不适用       |
|DualShock 4          |支持        |支持       |不适用       |
|PlayStation 早期      |支持        |不支持     |不支持       |
|支持 XINPUT 的其它手柄 |支持        |支持       |支持        |

*注：微软第二代适配器仅支持 Windows 10；可考虑某些第三方适配器，既兼容多种操作系统又支持多种手柄类型。*
  
2. 确认手柄已经被系统识别。打开`设备和打印机`可以设置游戏控制器。  
![在设备和打印机中设置游戏控制器](images/devices.jpg)

3. 使用 Chrome 浏览器打开应用主页: http://sb.plusii.com/
4. 找到正确的手柄图示，点击`复制 URL`。
5. 打开 OBS 直播软件，新建一个`浏览器`来源，并设置名称、URL、宽度、高度等参数。  
![OBS-新建浏览器来源](images/obs-1.jpg)  
![OBS-设置来源参数](images/obs-2.jpg)  

6. 最后调整好手柄尺寸和位置，开播！  
![OBS-调整直播画面](images/obs-3.jpg)
  
  
  
## Chrome 浏览器测试手柄步骤
1. 参照上节步骤连接好游戏手柄。
2. 使用 Chrome 浏览器打开应用主页: http://sb.plusii.com/
3. 找到正确的手柄图示，点击`测试手柄`。  
![测试-启动按钮](images/test-1.jpg)

4. 在弹出的对话框中启动测试。  
![测试-测试手柄](images/test-2.jpg)
  
  
## 疑难解答：若面板不响应手柄的操作指令？
0. 本工具理论上支持所有 XINPUT 模式的手柄；
1. 确保手柄已正确连接到计算机，并且被系统识别（参考使用步骤）；
2. 若使用`蓝牙连接`，请断开所有其它的蓝牙设备；或改用线缆连接、适配器连接；
3. 尝试重启 OBS，清除浏览器缓存，以便脚本重新初始化；
4. 尝试访问网站 http://sb.plusii.com/ 在线测试您的手柄；
5. 若连接了多个手柄，请利用`测试手柄`确定正确的`通道`，在 OBS 中要使用对应的 URL；
![测试-切换手柄通道](images/test-3.jpg)
6. PlayStation 手柄建议借助 [DS4Windows] 工具模拟为 XINPUT 模式；
7. [Steam] 接管手柄可能导致输入指令无法被捕捉，请尝试在`控制器设置`中取消特定手柄的勾选。  
  
  
-------------------------------------------------  
使用中有任何问题和建议，欢迎 [在此留爪] 或 QQ [9812152]。  
(聊表心意，金额随意)  
![微信扫码捐赠](https://static.plusii.com/images/donate-wechat.jpg)


[OBS Studio]: https://obsproject.com/
[Browser]: https://obsproject.com/forum/resources/browser-plugin.115/
[DS4Windows]: https://ryochan7.github.io/ds4windows-site/
[Steam]: https://store.steampowered.com/
[在此留爪]: https://github.com/HeddaZ/shoubing/issues
[9812152]: tencent://message/?uin=9812152
