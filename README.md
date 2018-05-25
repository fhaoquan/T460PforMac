## 前言

> 这里讨论的配置是：美版thinkpad T460P i7 6820hq  系列
> 如果是I5  请修改下面字段的值,clover config 可以修改
> 		<key>ig-platform-id</key>


### 存在的问题：
亮度快捷键和电池电量没驱动，需要自行处理






## 开始

#### 1. 系统镜像

这里提供一份可用的10.13 的系统
链接: https://pan.baidu.com/s/12nVWwnMdR22Y1XhTCmRg4g 密码: 9v9j

#### 2. 镜像写入U盘

还是老伙计，`Transmac`
链接: https://pan.baidu.com/s/1hrAZQHe 密码: 7kyq

，网上找个和谐版吧，写入U盘的过程我不说了，写入完毕后：

- 如果你有硬盘Clover，把你EFI里的Clover文件夹改名成bak，用我的Clover文件夹代替。
- 如果你没有硬盘Clover，那就删除U盘EFI分区里面的Clover文件夹，用我的Clover文件夹代替。

或者网上下个最新版本吧，我的可能有点旧了
Clover Configurator.app
链接: https://pan.baidu.com/s/1o8jt2aQ 密码: qer2

#### 3. 安装系统

用Clover引导安装你写入了U盘的镜像系统，完成并进入系统

#### 4. 安装其他驱动

触摸板是用苹果原生的驱动， 如果用惯了Windows 触摸可能不太习惯， 无线网卡是博通BCM94360芯片 DW1830 无线额外安装渠道， 亮度调节快捷键需要自己折腾，平时工作忙能用就行了没去折腾。


## 结束


完美黑苹果的路还很远，大家一起努力！

