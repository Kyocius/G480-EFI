# Lenovo G480 Clover EFI
基本上可以完美使用!
## 配置
- CPU `i5-3230M`*（2.6GHZ）*

- 声卡 `ALC-269`

- 显卡 `HD4000`

- 无线网卡 `AR9485`

- 无 蓝牙 *（没有驱动...）*

- Clover版本 `4132`

- MacOS `Big Sur 11.6.1`

## 截图
> 图中序列号为随机生成

![图片三](https://github.com/worrix64/G480-EFI/blob/main/screenshot.png?raw=true)

![图片一](https://github.com/worrix64/G480-EFI/blob/main/%E6%88%AA%E5%B1%8F2022-01-13%20%E4%B8%8B%E5%8D%884.30.00.png?raw=true)

![图片二](https://github.com/worrix64/G480-EFI/blob/main/%E6%88%AA%E5%B1%8F2022-01-13%20%E4%B8%8B%E5%8D%884.31.15.png?raw=true)

## 问题
- [ ] 显示器没有出识别型号
- [ ] 没有亮度滑块
- [ ] 睡眠十分钟左右会自动唤醒
- [ ] 存在信号显示掉格，但不影响网速

## 鸣谢

### @mjs520 和他的[EFI仓库](https://github.com/mjs520/Lenovo-G480)
  
- 我在他的EFI基础上，增加了网卡`AR9485`的三个`kext`驱动
  > 参考[@Asly 的教程](https://www.asly.top/archives/17/)
- 定制了USB驱动
  > 使用 `Hackintool` 定制USB补丁
- 睡眠没有他的完美(没搞明白)

### @mjs520 的原文

1. 睡眠唤醒声音正常

2. 触控板手势基本正常

3. Hacktool打缓冲针补丁，显卡HD4000驱动正常，显示PCI信息，注入EDID信息

4. 修改显存2048mb

5. USB端口定制2.0、3.0正常

6. 有线网卡正常

7. AR9485无线网卡正常

8. ALC269声卡仿冒正常

9. EC0重命名EC，ACPI添加仿冒SSDT-EC

10. 添加了FixEDID修补，提高色彩温和度，增加了桌面分辨率选择

11. 修改DSDT，加载LPC硬件ID加载原生电源管理

12. 变频正常 (CPUFried+sSDTPRGen)

13. 增加了XMPDetection(只适用DDR3)，即可将内存条自动超频到1600或更高值。

14. 添加亮度DSDT~HD4000亮度补丁+(GFX0重命名IGUP)+ACPIBacklight.kext亮度滑块正常。

15. 亮度、声音细腻调节1/4格,小太阳快捷键-功能键+F5、F6，声音快捷键-功能键+F11、F12

16. 添加热补丁(SSDT-ALS0+SMCLightsensors.kext)实现亮度保存，及自动调节选项。

17. 添加ACPIbatterymanage.kext实现电池百分比正常

18. 添加三码AppleStore正常下载，FaceTime，Imesge正常

19. 添加DSDT～SMBus补丁加载SMBus成功

## 最后
本项目基于`GPLv3`协议开源，禁止倒卖，请遵守本开源协议!
