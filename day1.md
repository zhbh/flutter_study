### day1学习内容

- 学习记录
	1. 2019-12-01 issue：下载最新Xcode（7.6G），耗时8个小时
	2. 2019-12-02 issue: 相应更新最新系统，耗时大约1个小时；调试启动模拟器。

- 安装开发环境
	1. macOs系统安装flutter

	2. 问题
		1. flutter sdk下载
			1. git下载速度非常慢，而且下载会失败
			2. ~~改为flutter的github主页点击下载，比较快。~~
			3. 用chrome下载[flutter sdk](https://flutter.dev/docs/development/tools/sdk/releases?tab=macos#macos)，记住解压包的路径，终端和开发环境需要引用这个路径，调用flutter sdk。
		2. flutter sdk 引用问题
			1. 终端引用路径命令：
				`export PATH=~/[flutter sdk安装路径]/bin:$PATH`
				`echo $PATH` 查看是否添加到环境变量中
				以上方式，在电脑重启之后，调用命令会失败，添加命令路径会消失（只是暂存缓存中）。
				永久存在在用户的环境变量bash_profile文件中，
				`vi ~/.bash_profile`，再次添加`export PATH=~/[flutter sdk安装路径]/bin:$PATH`，重启此文件，使命令生效：`source ~/.bash_profile`。
			2. 开发环境VS code的flutter sdk路径，第一次有对话框提示flutter sdk安装路径。如果要再次修改此路径，可以到VS code的setting找到extensions的dart设置fluttersdkpath。
		3. 运行flutter run问题，提示没有设备连接
			1. 在macOS中xcode版本需要10以上，才能远行flutter编译。
			2. 下载最新的xcode时候，在终端上选择最新xcode版本，执行
				`sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer` 
				如果下载不在applications文件夹和xcode.app的名字不一样（例如xcode-beta.app），相应都要改下载路径和名称。
			3. 打开Xcode的许可协议，为了可以调用Xcode的模拟器和相关程序。
				`sudo xcodebuild -license`
			4. 命令输入打开模拟器
				`open -a Simulator`
			5. 运行当前程序
				`flutter run`
			6. 其他问题
				以上命令在系统终端运行，在VS code的终端没有反应。在VS code重新输入以上命令。

