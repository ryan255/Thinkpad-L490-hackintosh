# Thinkpad-L490-hackintosh

| 型号       | ThinkPad L490                   |
| ---------- | ------------------------------- |
| CPU系列    | 第八代智能英特尔酷睿i5          |
| CPU型号    | i5-8265U                        |
| CPU主频    | 1.6Ghz                          |
| 最高睿频   | 3.9Ghz                          |
| 核心架构   | Whiskey Lake                    |
| 硬盘容量   | 512GB(M.2 SSD)                  |
| 光驱类型   | 无光驱                          |
| 屏幕尺寸   | 14.0英寸                        |
| 显示比例   | 16:9                            |
| 屏幕分辨率 | 1920x1080                       |
| 屏幕技术   | LED背光;TN防眩目显示屏          |
| 显卡类型   | 集成显卡                        |
| 显卡芯片   | Intel UHD Graphics 620          |
| 音频系统   | HD Audio, Realtek ALC3287 codec |
| 无线网卡   | Intel 9260(2x2 AC)              |
| 有线网卡   | Intel I219-V                    |
| 蓝牙       | BT 5.0                          |
| 数据接口   | 2个USB3.1,2个Type-C             |
| 视频接口   | HDMI                            |
| 读卡器     | Micro SD读卡器                  |
| 指取设备   | TrackPad 经典触控板 多点触控    |

## 1. 适用MacOS Ventura 13.7.8 OpenCore EFI

使用OpCore-Simplify构建，网卡选择airportitlwm，可以使用原生的WiFi与蓝牙。

### 以下驱动正常 👍

- 原生电源
- 睡眠
- 显卡
- HDMI及Type-c接口 外接显示器
- 声卡，Fn快捷键
- 小太阳，Fn快捷键
- 有线网卡
- 无线网卡
- USB、Type-c
- 蓝牙

### 已知问题

- 声卡支持不完美，实测3.5接口输出声音偏闷



## 2. 适用MacOS Sequoia 15.7.1 OpenCore EFI

因无法使用airportitlwm，网卡选择itlwm，需要搭配Heliport.app使用WiFi，需要注意的是Heliport不支持需要登录认证的企业级安全性。

itlwm.kext已经集成2.3.0，需要更新[点击这里](https://github.com/OpenIntelWireless/itlwm)，Heliport请自行[下载](https://github.com/OpenIntelWireless/HeliPort?tab=readme-ov-file)

### 以下驱动正常 👍

- 原生电源
- 睡眠
- 显卡
- HDMI及Type-c接口 外接显示器
- 声卡，Fn快捷键
- 小太阳，Fn快捷键
- 有线网卡
- 无线网卡 (不完美)
- USB、Type-c
- 蓝牙

### 已知问题

- 无线网卡使用itlwm驱动，部分企业级安全性WiFi不可连接，部分windows热点不可连接
- 声卡支持不完美，实测3.5接口输出声音偏闷



以上两个版本均通过实际安装测试。



感谢：

> [lzhoang2801/OpCore-Simplify: A tool designed to simplify the creation of OpenCore EFI](https://github.com/lzhoang2801/OpCore-Simplify)
>
> [OpenIntelWireless/itlwm: Intel Wi-Fi Drivers for macOS](https://github.com/OpenIntelWireless/itlwm)
>
> [OpenIntelWireless/HeliPort: Intel Wi-Fi Client for itlwm](https://github.com/OpenIntelWireless/HeliPort?tab=readme-ov-file)
