# CasaOS_CentOS7-manual
 一份帮助你在CentOS 7 Linux 上安装CasaOS的向导/A guide to help you install CasaOS on CentOS 7 Linux.
## 已在CentOS 7 2009通过测试，资料源自互联网，如有侵犯您的合法权益，请联系我删除。

### Tested on CentOS 7 2009.  If it infringes your legal rights, please contact me to delete it.

3288922513@qq.com

## ![image](https://github.com/user-attachments/assets/dcb0c09c-e77e-4b96-924a-504b1635d255)


## CasaOS安装向导

### 1、克隆本仓库以下载所需软件包：

```
git clone https://github.com/L1keava/CasaOS_CentOS7-manual
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

### 7、恢复系统版本更改

```
sudo sed -i 's/ID="ubuntu"/ID="centos"/g' /etc/os-release
```

### 8、Enjoy!

## Thanks
- [IceWhaleTech](https://github.com/IceWhaleTech) for CasaOS
