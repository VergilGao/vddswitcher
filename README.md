## Table of Contents
- [Introduction about vddswitcher](#Introduction-about-vddswitcher)
- [How to use](#How-to-use)
- [Supported resolution](#Supported-resolution)
- [Customize Resolution](#Customize-Resolution)

## 目录
- [介绍](#关于vddswitcher)
- [使用方法](#使用方法)
- [支持的分辨率](#支持的分辨率)
- [自定义分辨率](#自定义分辨率)

# Introduction about vddswitcher

A "just work" VDD program for Sunshine streaming.

Main features:

- Create a virtual display when streaming starts.

- Automatically set the resolution of the virtual display based on the resolution set by the Moonlight client (if supported).

- Close the virtual display when streaming ends.

## How to use

Make sure you have installed the following drivers

- [parsec-vdd-v0.41](https://builds.parsec.app/vdd/parsec-vdd-0.41.0.0.exe) 

Place `vddswitcher.exe` and `vddswitcherd.exe` in your preferred location.

For first-time use, you need to configure the virtual desktop as the main display:

Right-click the Windows icon - Run - Enter `cmd`
In the opened cmd window, type

`cmd /C "your_path_to_vddswitcherd.exe" -x "your_main_display_pixel_width" -y "your_main_display_pixel_height" -r "your_main_display_refresh_rate"`

This will create a virtual display with the same resolution as your main display.

Go to the display configuration page, select the created virtual display, and check the option to set it as the main display. (Note: This operation will make your desktop look strange, but everything can be restored.)

If you find that your mouse is missing and some windows have moved to the virtual display, it’s usually easier to just restart your computer.

After restarting the computer, you will find that the virtual display has disappeared.

Open Sunshine and go to `Configuration - General`.

In the Do Command field, enter `cmd /C "path_to_vddswitcherd.exe" -x %SUNSHINE_CLIENT_WIDTH% -y %SUNSHINE_CLIENT_HEIGHT% -r %SUNSHINE_CLIENT_FPS%`

For example:

`cmd /C "D:\game\utils\vddswitcher\vddswitcherd.exe" -x %SUNSHINE_CLIENT_WIDTH% -y %SUNSHINE_CLIENT_HEIGHT% -r %SUNSHINE_CLIENT_FPS%`

In the Undo Command field, enter `cmd /C "path to vddswitcher.exe"`

For example:

`cmd /C "D:\game\utils\vddswitcher\vddswitcher.exe"`

Save and submit, then wait for a restart. Use Moonlight to access the desktop.

Go to the Monitor Configuration page and disable monitors other than the virtual monitor to save energy.

## Supported resolution

| Resolution   | Common name      | Aspect ratio         | Refresh rates (Hz)
| -            | :-:              | :-:                  | :-:
| 4096 x 2160  | DCI 4K           | 1.90:1 (256:135)     | 24/30/60/144/240
| 3840 x 2160  | 4K UHD           | 16:9                 | 24/30/60/144/240
| 3840 x 1600  | UltraWide        | 24:10                | 24/30/60/144/240
| 3840 x 1080  | UltraWide        | 32:9 (2x 16:9 FHD)   | 24/30/60/144/240
| 3440 x 1440  |                  | 21.5:9 (43:18)       | 24/30/60/144/240
| 3240 x 2160  |                  | 3:2                  | 60
| 3200 x 1800  | 3K               | 16:9                 | 24/30/60/144/240
| 3000 x 2000  |                  | 3:2                  | 60
| 2880 x 1800  | 2.8K             | 16:10                | 60
| 2880 x 1620  | 2.8K             | 16:9                 | 24/30/60/144/240
| 2736 x 1824  |                  |                      | 60
| 2560 x 1600  | 2K               | 16:10                | 24/30/60/144/240
| 2560 x 1440  | 2K               | 16:9                 | 24/30/60/144/240
| 2560 x 1080  | UltraWide        | 21:9                 | 24/30/60/144/240
| 2496 x 1664  |                  |                      | 60
| 2256 x 1504  |                  |                      | 60
| 2048 x 1152  |                  |                      | 60/144/240
| 1920 x 1200  | FHD              | 16:10                | 60/144/240
|**1920 x 1080**| **FHD**         | **16:9**             | 24/30/**60**/144/240
| 1800 x 1200  | FHD              | 3:2                  | 60
| 1680 x 1050  | HD+              | 16:10                | 60/144/240
| 1600 x 1200  | HD+              | 4:3                  | 24/30/60/144/240
|  1600 x 900  | HD+              | 16:9                 | 60/144/240
|  1440 x 900  | HD               | 16:10                | 60/144/240
|  1366 x 768  |                  |                      | 60/144/240
|  1280 x 800  | HD               | 16:10                | 60/144/240
|  1280 x 720  | HD               | 16:9                 | 60/144/240


## Customize Resolution

[VDD Advanced Configuration](https://support.unity.com/hc/en-us/articles/26828920583444-VDD-Advanced-Configuration)

The current version supports 5 custom resolutions.

# 关于vddswitcher

一个 just work 的用于 sunshine 串流的 vdd 程序。

主要功能：

- 开始串流时创建虚拟显示器

- 自动根据 moonlight 客户端设置的分辨率设置虚拟显示器的分辨率(如果支持的话)

- 结束串流时关闭虚拟显示器

## 使用方法

确保你已经安装了以下驱动

- [parsec-vdd-v0.41](https://builds.parsec.app/vdd/parsec-vdd-0.41.0.0.exe) 

将 `vddswitcher.exe` 和 `vddswitcherd.exe` 放到你喜欢的位置

首次使用需要先配置虚拟桌面为主显示器：

右键开始图标 - 运行 - 输入 `cmd`
在打开的 cmd 窗口中输入 

`cmd /C "vddswitcherd.exe的路径" -x "你的主显示器像素宽度" -y "你的主显示器像素高度" -r "你的主显示器刷新率"`

此时将创建一个和你主显示器相同分辨率的虚拟显示器。

进入显示器配置页，选择创建出来的虚拟显示器，勾选设置为主显示器。(注意，此操作将会让你的桌面变得奇怪，但是这一切都是可以恢复的)

你发现你的鼠标找不到了，一些窗口也被移动到了虚拟显示器，此时不管你做什么都不如重启一下电脑来的方便。

重启电脑之后，你会发现虚拟显示器已经消失了。

打开 sunshine 转到 `Configuration - General` 

最下方 Do Command 栏填入 `cmd /C "vddswitcherd.exe的路径" -x %SUNSHINE_CLIENT_WIDTH% -y %SUNSHINE_CLIENT_HEIGHT% -r %SUNSHINE_CLIENT_FPS%`

例如:

`cmd /C "D:\game\utils\vddswitcher\vddswitcherd.exe"  -x %SUNSHINE_CLIENT_WIDTH% -y %SUNSHINE_CLIENT_HEIGHT% -r %SUNSHINE_CLIENT_FPS%`

Undo Command 栏填入 `cmd /C "vddswitcher.exe的路径"`

例如:

`cmd /C "D:\game\utils\vddswitcher\vddswitcher.exe"`

保存并提交，等待重启后，使用 moonlight 进入桌面。

进入显示器配置页，将虚拟显示器外的其他显示器禁用来节约能源。

## 支持的分辨率

| Resolution   | Common name      | Aspect ratio         | Refresh rates (Hz)
| -            | :-:              | :-:                  | :-:
| 4096 x 2160  | DCI 4K           | 1.90:1 (256:135)     | 24/30/60/144/240
| 3840 x 2160  | 4K UHD           | 16:9                 | 24/30/60/144/240
| 3840 x 1600  | UltraWide        | 24:10                | 24/30/60/144/240
| 3840 x 1080  | UltraWide        | 32:9 (2x 16:9 FHD)   | 24/30/60/144/240
| 3440 x 1440  |                  | 21.5:9 (43:18)       | 24/30/60/144/240
| 3240 x 2160  |                  | 3:2                  | 60
| 3200 x 1800  | 3K               | 16:9                 | 24/30/60/144/240
| 3000 x 2000  |                  | 3:2                  | 60
| 2880 x 1800  | 2.8K             | 16:10                | 60
| 2880 x 1620  | 2.8K             | 16:9                 | 24/30/60/144/240
| 2736 x 1824  |                  |                      | 60
| 2560 x 1600  | 2K               | 16:10                | 24/30/60/144/240
| 2560 x 1440  | 2K               | 16:9                 | 24/30/60/144/240
| 2560 x 1080  | UltraWide        | 21:9                 | 24/30/60/144/240
| 2496 x 1664  |                  |                      | 60
| 2256 x 1504  |                  |                      | 60
| 2048 x 1152  |                  |                      | 60/144/240
| 1920 x 1200  | FHD              | 16:10                | 60/144/240
|**1920 x 1080**| **FHD**         | **16:9**             | 24/30/**60**/144/240
| 1800 x 1200  | FHD              | 3:2                  | 60
| 1680 x 1050  | HD+              | 16:10                | 60/144/240
| 1600 x 1200  | HD+              | 4:3                  | 24/30/60/144/240
|  1600 x 900  | HD+              | 16:9                 | 60/144/240
|  1440 x 900  | HD               | 16:10                | 60/144/240
|  1366 x 768  |                  |                      | 60/144/240
|  1280 x 800  | HD               | 16:10                | 60/144/240
|  1280 x 720  | HD               | 16:9                 | 60/144/240


## 自定义分辨率

[VDD高级设置](https://support.unity.com/hc/en-us/articles/26828920583444-VDD-Advanced-Configuration)

目前版本支持5个自定义分辨率
