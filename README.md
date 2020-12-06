## 神舟k680e-g6d1黑苹果efi

### 配置:

|    硬件    |     型号      |   状态   |
| :--------: | :-----------: | :------: |
|    CPU     |    i5-7400    |  已睿频  |
|   图形卡   |     HD630     |  已驱动  |
|  图形卡2   |  GTX 1050Ti   |  已屏蔽  |
|    声卡    |    ALC269     |  已驱动  |
| Wi-Fi&蓝牙 | 自带Intel网卡 |  已驱动  |
|    USB     |               |  已定制  |
|    睡眠    |               | ~~正常~~ |
|   FN映射   |               | ~~正常~~ |
|   触摸板   |               |   正常   |

### TODO:

- 修改亮度调节快捷键
- 修复Intel网卡无法正常睡眠

### ChangeLogs:

#### 2020.12.05(by [Takoyaki White](https://github.com/takoyakiwhite))

- 屏蔽独显（防止S3下独显启用导致的崩溃）
- ~~亮度键调节~~
- 去除无用驱动（I2C等）
- 去除无用HotPatch（PMC、SBUS等）
- ~~替换ACPIBatteryManager为VirtualSMC Plugins~~
- 去除NoTouchID（Big Sur下已失效）
- 添加Sinetek驱动
- 添加_PTS _WAK睡眠修补（with Rename）
- 精简无用Quirk/无用添加项
- 添加屏蔽_PRW唤醒
- 仿冒环境光传感器
- 添加背光修补
- 更新驱动至最新（12.4编译）
- 去除操作系统补丁
- 去除KASLR注入方式
- 将PCI下Layout ID更改为boot-args参数（便于调试）
- 去除无用NVRAM项
- 去除SMBIOS下UUID
- 去除USB限制解除
- 修复启动磁盘判断
- 去除KEXT崩溃信息
- 修复音频崩溃问题（Kaby lake）
