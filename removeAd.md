#不用root，去除小米电视广告

##0. 安装沙发桌面、电视家等应用
	项目中保存部分apk，可以选择安装。

##1. 打开开发者模式：
    01、设置——关于——产品型号——连续按确认键5次以上，直到提示 “你已经处于开发者模式”

##2. 开启adb调试
    在设置-个人账户里面 开启adb调试

## 3. 链接到adb
	依次执行以下命令：
	adb kill-server
	adb start-server	
	adb connect 192.168.0.108:5555	
	注意(此处，请根据电视的实际IP来修改，端口5555不变)
	执行后，请在电视上选择允许adb调试
	删除系统自带桌面：(注：务必确定已经安装第三方桌面)
	adb shell pm uninstall --user 0 com.mitv.tvhome

## 4.其他注意事项
	删除自带桌面后，如果想打开系统设置，请通过双击Home键进入，否则无法打开。
	HDMI输入源 可以通过此方式打开选择



ps：参考链接：
	https://tieba.baidu.com/p/5552181422?red_tag=3125875557
	https://tieba.baidu.com/p/5696218809?red_tag=1743395294