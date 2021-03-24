#Mac终端cmd控制设备 SSH_Over_USB

### [使用usbmuxd通过USB进行SSH](https://iphonedevwiki.net/index.php/SSH_Over_USB)
 
一、[安装 usbmuxd](https://github.com/libimobiledevice/usbmuxd)
    [usbmuxd 安装细节](https://www.jianshu.com/p/49c4386ad9cc?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation)
    
二、[安装 MonkeyDev](https://github.com/AloneMonkey/MonkeyDev/wiki)

    Building for iOS, but linking in .tbd file (/opt/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd) built for iOS Simulator, file '/opt/theos/vendor/lib/CydiaSubstrate.framework/CydiaSubstrate.tbd' for architecture arm64
    
  [MonkeyDev 报错CydiaSubstrate.tbd处理方法](https://www.jianshu.com/p/060be025eb13)
    
三、[越狱设备命令cmd等插件和安装ipa包](https://www.jianshu.com/p/b46a96bb7416)

四、常用cmd命令

    killall -9 SpringBoard // 重启App桌面

    open com.apple.Preferences // 打开设置

    killall -9 Preferences // 关闭设置

    open YourAppBundleID // 打开App

    killall -9 YourAppName // 关闭App
    
五、命令操作

      AppledeMac-mini:~ apple$ 
      AppledeMac-mini:~ apple$ ssh -P2222 root@localhost
      ssh: connect to host localhost port 22: Connection refused
      AppledeMac-mini:~ apple$ ssh localhost
      ssh: connect to host localhost port 22: Connection refused
      AppledeMac-mini:~ apple$ 
      AppledeMac-mini:~ apple$ ssh localhost
      The authenticity of host 'localhost (127.0.0.1)' can't be established.
      ECDSA key fingerprint is SHA256:P3X5QOIilX5bTb/OJvDQjLgCIu8FRL3qoMf0Gj5SGmY.
      Are you sure you want to continue connecting (yes/no)? y
      Please type 'yes' or 'no': no
      Host key verification failed.
      AppledeMac-mini:~ apple$ 
      AppledeMac-mini:~ apple$ ssh -P2222 root@localhost
      The authenticity of host 'localhost (127.0.0.1)' can't be established.
      ECDSA key fingerprint is SHA256:P3X5QOIilX5bTb/OJvDQjLgCIu8FRL3qoMf0Gj5SGmY.
      Are you sure you want to continue connecting (yes/no)? yes
      Warning: Permanently added '[localhost]:2228' (RSA) to the list of known hosts.
      root@localhost's password: 
      4136-142-b:~ root# exit
      logout
      Connection to localhost closed.
      AppledeMac-mini-2:~ apple$ 
      AppledeMac-mini-2:~ apple$ 
      AppledeMac-mini-2:~ apple$ ssh -p2228 root@localhost
      ssh_exchange_identification: read: Connection reset by peer
      AppledeMac-mini-2:~ apple$ ssh -p2228 root@localhost
      @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
      @    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
      @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
      IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
      Someone could be eavesdropping on you right now (man-in-the-middle attack)!
      It is also possible that a host key has just been changed.
      The fingerprint for the RSA key sent by the remote host is
      SHA256:5qn0rLzl2lSSTNnwiOMLFe46Wpffhrnnc+SSwnkob3s.
      Please contact your system administrator.
      Add correct host key in /Users/apple/.ssh/known_hosts to get rid of this message.
      Offending ECDSA key in /Users/apple/.ssh/known_hosts:1
      RSA host key for [localhost]:2228 has changed and you have requested strict checking.
      Host key verification failed.
      AppledeMac-mini-2:~ apple$ rm /Users/apple/.ssh/known_hosts
      AppledeMac-mini-2:~ apple$ ssh -p2228 root@localhost
      The authenticity of host '[localhost]:2228 ([127.0.0.1]:2228)' can't be established.
      RSA key fingerprint is SHA256:5qn0rLzl2lSSTNnwiOMLFe46Wpffhrnnc+SSwnkob3s.
      Are you sure you want to continue connecting (yes/no)? yes
      Warning: Permanently added '[localhost]:2228' (RSA) to the list of known hosts.
      root@localhost's password: 
      413612-black:~ root# 
      413612-black:~ root# launchctl load /Library/LaunchDaemons/com.oych.ModianDaemon.plist 
      413612-black~ root# 
      413612-black:~ root# launchctl load /Library/LaunchDaemons/com.oych.ModianDaemon.plist 
      /Library/LaunchDaemons/com.oych.ModianDaemon.plist: service already loaded
      413612-black~ root# 
      413612-black~ root# killall -9 SpringBoard
      4136-124-black:~ root# 
      413612-black~ root# killall -9 ModianDaemon
      4136-124-black:~ root# 
      413612-black:~ root# ldid -S /usr/bin/ModianDaemon

