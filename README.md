# 雷柏v500在Linux系统不能使用Ctrl和Alt问题
1、下载驱动
2、解压
3、cd到解压的文件夹
4、执行make
5、执行make install
6、执行sudo sh install-rapoo-keyboard-driver.sh
#### 添加开机启动项
```java
sudo vim /etc/rc.local
```
#### 编辑启动文件
```bash
#!/bin/sh -e
#
# rc.local
#
# This script is executed at the end of each multiuser runlevel.
# Make sure that the script will "exit 0" on success or any other
# value on error.
#
# In order to enable or disable this script just change the execution
# bits.
#
# By default this script does nothing.
/home/landv/Downloads/rapoo-keyboard-driver-master/install-rapoo-keyboard-driver.sh
exit 0
```


# rapoo-keyboard-driver
Some bugfix for rapoo keyboard where some keys are invalid.

# Quick Usage
Compile the driver module with make, make install and run ./install-rapoo-keyboard-driver.sh.

Job done! Then enjoy typing!

# Notice
After installing new kernel(contains compile and install kernel),
you must reinstall hid-rapoo module again by "make install".
