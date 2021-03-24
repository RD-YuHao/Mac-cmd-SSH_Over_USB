#Mac终端cmd控制设备 SSH_Over_USB

### [使用usbmuxd通过USB进行SSH](https://iphonedevwiki.net/index.php/SSH_Over_USB)
 
一、[安装 usbmuxd](https://github.com/libimobiledevice/usbmuxd)
    [usbmuxd 安装细节](https://www.jianshu.com/p/49c4386ad9cc?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation)
    
二、[安装 MonkeyDev](https://github.com/AloneMonkey/MonkeyDev/wiki)

`Building for iOS, but linking in .tbd file (/opt/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd) built for iOS Simulator, file '/opt/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd' for architecture arm64`
    
  [MonkeyDev 报错CydiaSubstrate.tbd处理方法](https://www.jianshu.com/p/060be025eb13)
    
三、[越狱设备命令cmd等插件和安装ipa包](https://www.jianshu.com/p/b46a96bb7416)

四、常用cmd命令

(```)

    killall -9 SpringBoard // 重启App桌面

    open com.apple.Preferences // 打开设置

    killall -9 Preferences // 关闭设置

    open YourAppBundleID // 打开App

    killall -9 YourAppName // 关闭App
    
(```)

