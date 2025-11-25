# Thinkpad-L490-hackintosh

硬件配置：

	1. CPU: i5-8250U
	2. 内存：8Gx2
	3. 硬盘：512G ssd
	4. 显卡：核心显卡Intel UHD Graphics 620
	5. 网卡：Intel 9260

## 1. 适用MacOS Ventura 13.7.8 OpenCore EFI

使用OpCore-Simplify构建，网卡选择airportitlwm，可以使用原生的WiFi与蓝牙。



感谢：

> [lzhoang2801/OpCore-Simplify: A tool designed to simplify the creation of OpenCore EFI](https://github.com/lzhoang2801/OpCore-Simplify)



## 2. 适用MacOS Sequoia 15.7.1 OpenCore EFI

因无法使用airportitlwm，网卡选择itlwm，需要搭配Heliport.app使用WiFi，需要注意的是Heliport不支持需要登录认证的企业级安全性。



以上两个版本均通过实际安装测试。
