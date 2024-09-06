# CasaOS_CentOS7-manual
 一份帮助你在CentOS 7 Linux 上安装CasaOS的向导/A guide to help you install CasaOS on CentOS 7 Linux.
## 已在CentOS 7 2009通过测试，资料源自互联网，如有侵犯您的合法权益，请联系我删除。

### Tested on CentOS 7 2009.  If it infringes your legal rights, please contact me to delete it.

3288922513@qq.com

## ![image-20240906200327461](C:\Users\shich\AppData\Roaming\Typora\typora-user-images\image-20240906200327461.png)

## CasaOS安装向导

### 1、克隆本仓库以下载所需软件包：

```
git clone
```

### 2、安装ntfs-3g

```
tar -xf ntfs-3g_ntfsprogs-2022.10.3.tgz 
cd ntfs-3g_ntfsprogs-2022.10.3/
./configure
make
chmod a+x ./src/ntfs-3g
cp ./src/ntfs-3g /usr/local/bin/
cd
```

### 3、安装udevil

```
wget -O udevil-next.tar.gz https://github.com/IgnorantGuru/udevil/tarball/next
tar -xf udevil-next.tar.gz 
cd IgnorantGuru-udevil-77a6180/
yum -y install intltool glib* udev* libudev*
./configure --prefix=/usr
make
make install
cd
```

### 4、安装mergerfs

```
wget https://ghproxy.net/https://github.com/trapexit/mergerfs/releases/download/2.40.2/mergerfs-2.40.2.tar.gz
tar -xf mergerfs-2.40.2.tar.gz
cd mergerfs-2.40.2
make
cd build
chmod a+x mergerfs
cp ./mergerfs /usr/local/bin/mount.mergerfs
cd
```

### 5、修改系统版本为ubuntu

```
sudo sed -i 's/ID="centos"/ID="ubuntu"/g' /etc/os-release
```

### 6、安装CasaOS

```
sh get_casaOS.sh
```

### 7、Enjoy!
