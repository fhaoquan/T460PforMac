## 前言

> 这里讨论的配置是：美版thinkpad T460P i7 6820hq  系列
> 如果是I5  请修改下面字段的值,clover config 可以修改
> 		<key>ig-platform-id</key>


### 存在的问题：
- 触摸板你可以自行测试最新的[VoodooPS2Controller](https://github.com/RehabMan/OS-X-Voodoo-PS2-Controller)或[SmartTouchpad](http://forum.osxlatitude.com/index.php?/topic/1948-elan-focaltech-and-synaptics-smart-touchpad-driver-mac-os-x/)，当然，更推荐的是 @syscl [定制过手势的VoodooPS2Controller](https://github.com/syscl/OS-X-Voodoo-PS2-Controller)。

## 各资源目录的作用

- `ALC298(3266)-Info`，声卡相关的节点，LayoutID，ConfigData信息，原始Codec，还有从windows10注册表提取出来的PinConfigData，有需要可以自己拿来修改
- `CLOVER-Install`，完整的Clover配置（你下载后自己把名字改回Clover），根据你的需要进行修改。
- `DSDT-HotPatches`，Clover的DSDT/SSDT热补丁dsl源码，可以从[RehabMan主页](https://github.com/RehabMan/OS-X-Clover-Laptop-Config/tree/master/hotpatch)得到。
- `MoreKexts-LE`，安装好系统后再安装的第三方驱动。
- 如果你需要修改声卡Layout-ID，请在`SSDT-Config.dsl`修改`Name(AUDL, 你的id十进制)`，然后编译成aml，放回`ACPI/patched`


## 开始

#### 1. 系统镜像

- 如果你已有硬盘EFI分区的Clover，下载原版的DMG也可以
- 我的百度云盘有一份比较旧版本不介意可以先用着
- 链接: https://pan.baidu.com/s/1sljny9Z 密码: 2mf4
- 或者10.12.3 链接: https://pan.baidu.com/s/1bWQM7s 密码: qy2m

#### 2. 镜像写入U盘

还是老伙计，`Transmac`
链接: https://pan.baidu.com/s/1hrAZQHe 密码: 7kyq

，网上找个和谐版吧，写入U盘的过程我不说了，参考我上一篇教程，写入完毕后：

- 如果你有硬盘Clover，把你EFI里的Clover文件夹改名成bak，用我的Clover文件夹代替。
- 如果你没有硬盘Clover，那就删除U盘EFI分区里面的Clover文件夹，用我的Clover文件夹代替。
- 把我提供的MoreKext-LE复制到U盘安装系统的分区里（方便你安装系统后立刻可以访问）

Clover Configurator.app
链接: https://pan.baidu.com/s/1o8jt2aQ 密码: qer2

#### 3. 安装系统

用Clover引导安装你写入了U盘的镜像系统，完成并进入系统

#### 4. 安装其他驱动

最新的git 支持10.12.4 屏幕亮度,声音,简单触控板手势,能满足日常工作需要,需要的同学可以直接拷贝git 到clover 里面配置和渠道就可直接跑起来, 待有时间可以更加完善T460P黑苹果方案


## 结束


完美黑苹果的路还很远，大家一起努力！


## 特别鸣谢

- [RehabMan](https://github.com/RehabMan)
- [syscl](https://github.com/syscl)