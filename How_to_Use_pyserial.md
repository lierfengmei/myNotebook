# 如何使用pyserial？:blush:

**Label**:  *Linux*   *python*    *SerialPort*   *Ubuntu*


   * [如何使用pyserial？<g-emoji alias="blush" fallback-src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f60a.png" ios-version="6.0">😊</g-emoji>](#如何使用pyserialblush)
   * [Table of Contents](#table-of-contents)
    * [1. 安装pyserial](#1-安装pyserial)
    * [2. 学习<a href="http://pyserial.readthedocs.io/en/latest/pyserial.html">pySerial 参考资料官方文档</a>](#2-学习pyserial-参考资料官方文档)
    * [3. 编写简单的串口通信程序](#3-编写简单的串口通信程序)
    * [参考资料:](#参考资料)


### 1. 安装pyserial
- [下载](https://pypi.python.org/pypi/pyserial)pyserial安装包pyserial-3.3.tar.gz (md5)
- 通过下列命令安装
 ```tar zxvf pyserial-3.3.tar.gz
cd  pyserial-3.3
python3 setup.py install
 ```
- 通过命令lsusb查看usb是否存在
```Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 002 Device 004: ID 0403:6001 Future Technology Devices International, Ltd FT232 USB-Serial (UART) IC
Bus 002 Device 003: ID 0e0f:0002 VMware, Inc. Virtual USB Hub
Bus 002 Device 002: ID 0e0f:0003 VMware, Inc. Virtual Mouse
Bus 002 Device 001: ID 1d6b:0001 Linux Foundation 1.1 root hub
 ``` 
 - 查看可用端口(python -m serial.tools.list_ports)
 ```/dev/ttyS0
    /dev/ttyS1          
    /dev/ttyUSB0        
    3 ports found 
```

可以看出可用的端口是/dev/ttyUSB0


### 2. 学习[pySerial 参考资料官方文档](http://pyserial.readthedocs.io/en/latest/pyserial.html)

### 3. 编写简单的串口通信程序

**注意**，如果出现"/dev/ttyUSB0 permission denied.”，因为不是root权限。
所以```sudo chmod 777 /dev/ttyUSB0```即可。




#### 参考资料:
1. [pySerial 参考资料官方文档](http://pyserial.readthedocs.io/en/latest/pyserial.html) (非常全面)
1. [树莓派+Python+pyserial 2.7实现串口通信](http://blog.csdn.net/Burgess_Liu/article/details/41745159)
2. [/dev/ttyUSB0 permission denied　解决办法：永久有可操作权限](http://blog.csdn.net/w383117613/article/details/44216653) (永久修改的办法ＭＭ还没尝试)
