- http://cocos2d.org/
- https://www.cocos.com/
- https://github.com/cocos2d
- [Cocos 资料大全](https://github.com/fusijie/Cocos-Resource)
- [王哲 - Cocos引擎首席客服，知乎上的回答](https://www.zhihu.com/people/walzer/answers)
- :star:[[cocos creator]]:star:



## Cocos2dx-lua
- [mac下的开发环境搭建](http://sunhantao.github.io/2016/02/13/Mac%E4%B8%8B%E7%BC%96%E7%A0%81%E8%B0%83%E8%AF%95Cocos2dx-lua%E7%9A%84%E5%B7%A5%E5%85%B7/)

#### [Quick-Cocos2d-x](https://github.com/chukong/quick-cocos2d-x)
- Quick-Cocos2dx 是 Cocos2dx-lua 的增强版，封装了部分 API 更易于 lua 的开发。  
- Quick 官方稳定版本是 Quick-3.3final，最新版是 Quick-3.5，之后官方不再维护。

#### [Quick-Cocos2dx-Community](https://github.com/u0u0/Quick-Cocos2dx-Community)
- 基于 Quick-3.3final 的社区版。3.7 版本，改动很大不建议老项目使用；[4.0 版本](https://github.com/u0u0/Cocos2d-Lua-Community)，改动更大，也不建议老项目使用
  - 维护老项目，推荐继续使用 [3.6.5 版本](https://github.com/u0u0/Quick-Cocos2dx-Community/tree/3.6.5_Release)，或 [3.6.5 Doubility Sky 版]()
- [Cocos2d-x Lua 社区版](http://www.cocos2d-lua.org/) 官方网站
- [pbc 集成到quick-cocos2dx](http://www.cnblogs.com/suncoolcat/p/3297313.html)
- [Quick和Luajit使用注意](http://tairan.com/archives/10561/)
- [Quick资源加密](http://tairan.com/archives/10157/) 注：非zip加密方式下(-m files)：AppDelegate.cpp 启动代码是
  ```C++
  stack->executeString("require 'src.main'"); 
  ```
- [Quick使用webview](http://my.oschina.net/u/1582495/blog/465695) （注：目标目录是tools/tolua） 其他要导出的接口类似，操作过程中需要依赖的python组件安装参照[cocos2dx tolua说明](https://github.com/cocos2d/cocos2d-x/tree/c9306a053f051325a03b5297be7be6d645584780/tools/tolua)
- [Mac 下编译 Quick-Cocos2dx-Community 的 Android 版本](http://tairan.com/archives/10567/)
- [Quick-Cocos2dx develop for vscode](https://github.com/leitwolf/vscode-QuickXDev)

#### quick心得(cocos v3.10, quick v3.6.1)
- 所有导出的C＋＋到lua的API：Quick-Cocos2dx-Community/cocos/scripting/lua-bindings/auto/api/*.lua
- TextField设置文本排列时，要靠设置锚点实现，用setTextHorizontalAlignment无效。靠左排列＝setAnchorPoint(0, 0.5)
- cocos studio中的AtlasLabel无法使用，用代码创建LabelAtlas代替。
- cocos studio中的BitmapLabel无法使用，暂未找到解决办法。
- [Quick在iphone5s以上的ios64位下黑屏问题](http://www.cnblogs.com/yans/p/yans.html)
- quick的音效有时候播放不出问题：在第一个界面触发一下，原因未知：
  ```lua
    audio.setSoundsVolume(0.0)
    audio.playSound("res/Sound/HkFiveCard/SEND_CARD.wav")
    scheduler.performWithDelayGlobal(function ()
        audio.setSoundsVolume(1)
    end, 0.1)
  ```
- Player 打印行数太多显示不全  
  修改 `ConsoleWindowController.m` 定义的宏  
  ```cpp
  #define SKIP_LINES_COUNT    200
  ```



## Cocos Studio
- **注意！官方已不再维护，目前最后一个版本为 3.10**
- Mac上卡死问题 http://forum.cocos.com/t/cocosstudio/41214
  - 打开 /etc/hosts 文件 加入 127.0.0.1 cs.ucenter.appget.cn

