# phicomm-n1-soft
linux软件

[转自恩山]: https://www.right.com.cn/forum/forum.php?mod=viewthread&amp;tid=733144&amp;extra=page%3D2%26filter%3Dtypeid%26typeid%3D21

刷机包下载地址 https://yadi.sk/d/pHxaRAs-tZiei

最新5.89桌面版
无需替换文件，已经替换好了，N1直接使用
链接：https://pan.baidu.com/s/1xhZYdhJdgS82sLr0ksB99g 
提取码：vnof 

需要替换文件，原版
链接：https://pan.baidu.com/s/1i3EAammARBHsXbzR-YBb6Q 
提取码：jw39  

------

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/204503g0nxvsv6tvtvauxn.jpg)

写入设备EMMC命令：/root/install.sh

有网友反映在安装和编辑文本使用命令过程不能正常安装和编辑，请把命令前sudo删除
如果你想要EMMC安装使用armbian的，不要在U盘启动的系统里添加任何应用。直接启动登入后命令写入EMMC。
如果一开始用U盘使用的，并且在U盘里安装了OMV，不要再用这个带OMV的U盘写入设备EMMC。这样操作虽然MOV能一起写入EMMC，MOV也能启动，但是会出现不可预知的问题，比如：会出现移动硬盘不能共享的问题，设置保存过程中会报错

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/19/153635s7ltt4cstit7tt41.jpg) 



## 一、安装OpenMediaVault的方法

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/120339ztktxu10kgxus1ov.jpg) 



### 1.设置中国时区：



![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/120916x9qi9lkk9zd0lkyd.jpg) 



### 2.替换 APT 软件源，有助于提升访问速度和安全性（仅适用于 Debian）（可选操作）：

sed -i "s/http:\/\/httpredir/https:\/\/deb/g" /etc/apt/sources.list

### 3.更新软件包：

apt update && apt upgrade -y



### 4.重启系统：

reboot

### 5.启动 Armbian 配置菜单：

armbian-config

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/121801kvauot090qsv0hwv.jpg) 



### 6.选择 [Software] → [Softy] → 选中 (空格) [OMV] → 回车 → 等待安装完成

### 7.完成后浏览器输入你的IP地址，账号登入（你的armbian账号密码）

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/121134h65ijkrcvy8i6545.jpg) 

## 二、中文化armbian桌面系统

### 1.编辑文件

sudo nano /etc/locale.gen                    

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/122145cp1p7wka3g911743.jpg) 

  去掉zh_CN.UTF-8前面的#保存退出

### 2.安装中文字体：

sudo apt-get install ttf-wqy-zenhei

### 3.编辑文件：

sudo nano ~/.xprofile  

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/122346jrgaxbxpp829p9ul.jpg) 

  添加：
export LC_ALL=zh_CN.UTF-8
保存退出

### 4.编辑文件：

sudo nano /etc/default/locale  

![img](https://www.right.com.cn/forum/data/attachment/forum/201906/18/123039cjd889lm8m8hmj9m.jpg) 