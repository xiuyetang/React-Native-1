# react-native 一步步：环境搭建
系统要求

+ 一个装有 OS X 系统的开发机
+ [Homebrew](http://brew.sh/) 包管理工具
  ```
  brew install nvm
  brew install watchman
  brew install flow
  ```
+ 安装 Nodejs 4.0或者更新
  ```
  nvm install node && nvm alias default node
  ```
+ 定期执行 brew up && brew upgrade

## iOS 环境安装

+ 安装 XCode

## Android 环境安装

+ `brew install java`
+ `brew install android-sdk`，如果被墙，去 [AndroidDevTools](http://www.androiddevtools.cn/)
+ 修改配置文件：`~/.bash_profile`
  export ANDROID_HOME=/usr/local/opt/android-sdk
+ 在命令行运行 android，安装依赖的包
  - Android SDK Build-tools version 23.0.1
  - Android 6.0 (API 23)
  - Android Support Repository
+ 安装模拟器相关，可以和 4 一起安装
  - Intel x86 Atom System Image (for Android 5.1.1 - API 22)
  - Intel x86 Emulator Accelerator (HAXM installer)
+ 安装虚拟机加速模块（5完成后）
  安装：$SDK/extras/intel/Hardware_Accelerated_Execution_Manager/IntelHAXM.dmg
  控制台执行：kextstat | grep intel
  验证输出有：com.intel.kext.intelhaxm
+ 配置虚拟机（如果创建失败了，试试其它机型，如 Nexus 4）
  运行 android avd

![demo](CreateAVD.png)

## npm 安装工具
```
npm install -g react-native-cli
```

### 测试

```
react-native init BookSearch
cd BookSearch/
```

### iOS 启动

* 用 XCode 打开 ios/AwesomeProject.xcodeproj
* Cmd+B 编译
* Cmd+R 刷新

### Android 启动

+ `react-native android` 部署安卓环境，要下载很多东西
+ 启动虚拟机 `android avd`
+ `react-native run-android`
