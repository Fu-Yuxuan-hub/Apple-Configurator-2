# Apple-Configurator-2
在 Apple Silicon Mac 上 DFU 模式恢复 macOS 固件
# 1. 准备和要求
1. 一台额外的 Mac，我们这里称之为 “主 Mac”，配备 Type-C 接口，Intel 芯片和 Apple 芯片都可以
2. 系统版本 macOS Catalina 10.15.6 及以上
3. 下载 Apple Configurator 2(https://apps.apple.com/cn/app/apple-configurator-2/id1037126344?mt=12)
4. 下载 IPSW （可选），macOS Big Sur IPSW 下载
Apple Configurator 2 将自动下载 ipsw 固件（类似 iOS），可以使用下载管理器高速下载保存，直接拖拽到 Apple Configurator 2 中进行恢复。
5. USB-C to USB-C Cable：支持的 USB-C 转 USB-C 充电线，如 由 Apple 售卖的产品
6. 线缆的连接：主 Mac 可以任意 C 口，目标 Mac（要被恢复的 Mac）必须是指定 C 口（详见下文描述）
7. 确保 Mac 有充足的电源供应，有效的互联网访问
# 2. 步骤 1：连接 USB-C 线缆并在主 Mac 上打开 Apple Configurator 2
1. 插入（搭配任何需要的适配器）USB-C 线缆。
2. 插入 USB-C 线缆（搭配任何需要的转换器）并连接两台 Mac 电脑。
iMac（24 英寸，M1，2021 年）的背面，显示靠后的两个雷雳 3 (USB-C) 端口，其中标出了最右侧的端口。
iMac（24 英寸，M1，2021 年）的背面，显示靠后的两个雷雳 3 (USB-C) 端口，其中标出了最右侧的端口。

iMac（24 英寸，M1，2021 年）的背面，显示靠后的四个雷雳 3 (USB-C) 端口，其中标出了最右侧的端口。
iMac（24 英寸，M1，2021 年）的背面，显示靠后的四个雷雳 3 (USB-C) 端口，其中标出了最右侧的端口。

图像显示用户应该选择搭载 Apple 芯片的 Mac mini 上离以太网端口最近的端口。
图像显示用户应该选择搭载 Apple 芯片的 Mac mini 上离以太网端口最近的端口。

图像显示用户应该选择与搭载 Apple 芯片的 MacBook Pro 左侧显示器距离最近的端口。
图像显示用户应该选择与搭载 Apple 芯片的 MacBook Pro 左侧显示器距离最近的端口。

图像显示用户应该选择与搭载 Apple 芯片的 MacBook Air 左侧显示器距离最近的端口。
图像显示用户应该选择与搭载 Apple 芯片的 MacBook Air 左侧显示器距离最近的端口。

2021.10.30：关于 MacBook Pro (14-inch, 2021) 和 MacBook Pro (16-inch, 2021)，官方文档尚未更新，推测可以参照上述 MacBook Pro（13-inch，M1，2020）与 MacBook Air（13-inch，M1，2020），有待确认。
3. 启动 Apple Configurator 2。
img

# 3. 步骤 2：准备目标 Mac（被恢复的 Mac）
## 准备 iMac（24 英寸，M1，2021 年）（进入 DFU 模式）
1. 按下电源按钮。
2. 按住电源按钮的同时，按下以下所有三个按键大约 10 秒钟：
右 Shift 键
左 Option 键
左 Control 键
3.  秒钟后，立即松开这三个按键但继续按住电源按钮，直至 Apple Configurator 2 中出现 DFU 图标。
【注】 在您要修复或恢复的 iMac（24 英寸，M1，2021 年）上不会出现任何屏幕活动。
## 准备 Mac mini（进入 DFU 模式）
1. 插入显示器以便查看恢复过程何时完成。
2. 断开 Mac mini 的电源至少 10 秒钟。
3. 按住电源按钮。
4. 在按住电源按钮的同时重新连接电源。
5. 松开电源按钮。
状态指示灯应该呈琥珀色。
【注】Mac mini 不会出现任何屏幕活动。
## 准备 MacBook Air 或者 Macbook Pro（进入 DFU 模式）
1. 按下电源按钮。
2. 按住电源按钮的同时，按下以下所有三个按键大约 10 秒钟：
右 Shift 键
左 Option 键
左 Control 键
3. 10 秒钟后，立即松开这三个按键但继续按住电源按钮，直至设备出现在 Apple Configurator 2 中。
【注】Apple 笔记本电脑不会出现任何屏幕活动。

验证状态
在主 Mac 的 Apple Configurator 2 状态变化如下：

（1）目标 Mac 尚未启动到 DFU 模式，显示如下：

img

（2）目标 Mac 线缆连接正确，已经启动到了恢复模式选择窗口

img

（3）目标 Mac 已经正确启动到 DFU 模式

img

# 4. 步骤 3：拖拽 IPSW 文件到 DFU 画面进行恢复
请将下载的 macOS IPSW 文件拖拽到 DFU 图标上开始恢复。

img
macOS Big Sur IPSW Restore File

拖拽 macOS 11 IPSW 文件后，会弹出提示框，选择 “Restore”（“恢复”）将抹掉磁盘重新安装 macOS，整个过程大约需要 15 分钟。

img
弹出提示画面，选择 “Restore”（“恢复”）

如果你没有下载 IPSW（或者不知道哪里手动下载 IPSW），直接查看下面的替代 “步骤 3”

# 5. 步骤 3：修复或者恢复固件（无需准备 IPSW，自动联网下载）
## 选项 1：修复固件并安装最新的 recoveryOS
1. 在 Apple Configurator 2 的设备窗口中，选择要修复其芯片固件并将其 recoveryOS 更新到最新版本的 Mac。
Apple Configurator 2 显示 Mac，且弹出式菜单中选中了 “修复设备”。

2. 请执行以下一项操作：
选取 “操作” > “高级” > “修复设备”，然后点按 “修复”。
按住 Control 键点按所选设备并选取 “高级” > “修复设备”，然后点按 “修复”。
【注】 如果在此过程中任意一台 Mac 电量耗尽，请再次开始修复过程。
3. 等待过程完成。在此过程中，Apple 标志会出现和消失。
4. 修复过程完成后，Mac 会重新启动。
【重要事项】 修复固件时，必须确认已成功修复，因为 Apple Configurator 2 可能不会提醒您。
5. 退出 Apple Configurator 2，然后拔下任何适配器和线缆。

## 选项 2：恢复固件、抹掉所有数据并重新安装最新版本的 recoveryOS 和 macOS
1. 在 Apple Configurator 2 的设备窗口中，选择要恢复的 Mac。
img

2. 请执行以下一项操作：
选取 “操作” > “恢复”，然后点按 “恢复”。
按住 Control 键点按所选设备并选取 “操作” > “恢复”，然后点按 “恢复”。
【注】 如果在此过程中任意一台 Mac 电量耗尽，请再次开始恢复过程。
即将在 Apple Configurator 2 中恢复的 Apple 电脑。

3. 等待过程完成。在此过程中，Apple 标志会出现和消失。
4. 恢复过程完成后，Mac 会重新启动。
【重要事项】 恢复 Mac 时，必须确认已成功恢复，因为 Apple Configurator 2 可能不会提醒您。
5. 如果恢复成功，将显示 macOS 设置助理。
6. 退出 Apple Configurator 2 并拔下任何适配器和线缆。
