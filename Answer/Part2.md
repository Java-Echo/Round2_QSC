# 初探Linux
1. 二者的值并不一样,，因为MY-VALUE作用范围只是当前进程，而在当前进程被杀死后，MY-VALUE的值便消失，因此无法读取MY-VALUE的值  
2. 创建一个文件，编辑文件内容为`MY-VALUE=233`,之后打开shell时候只需要执行`source myvalue`，MY-VALUE便成功的被赋值为233，不管在那个shell中，只要myvalue该文件被读取，MY-VALUE便可以被成功赋值
3. 见 /Answer/uploads/2-3 bashrc.txtw
4. 先使用命令`sudo adduser dino`创建新的用户dino  
  接着输入`sudo su`进入原用户的root模式，输入`vim /etc/sudoers`利用vim编辑器进行编辑sudoers文件，找到`# Allow members of group sudo to execute any command`该行的下面一行，即`%sudo ALL=(ALL:ALL) ALL`进行编辑，进入插入模式，输入`dino ALL=(ALL:ALL) ALL`，之后退出插入模式，按shift+:键，并输入`wq!`进行强制保存，之后进入dino用户，可以通过`sudo`执行root命令  
5. 以下面代码为例`ruby:x:1000:1000:ubuntu 19.10,,,:/home/ruby:/bin/bash` 
   + 用户名：ruby，用户登陆时候系统使用的用户名
   + 密码：x，密码位
   + UID：1000，用户标识号
   + GID：1000，缺省组标识号
   + 注释性描述:ubuntu 19.10，存放用户的全名
   + 宿主目录：用户登陆系统后的缺省目录
   + 命令解释器：用户使用的shell，一般默认为bash
6. xterm是一个windows system上的终端模拟器，用来提供多个独立的shell输出
7. Main：Main包含自由软件的软件包，这些软件包和自由软件的观念一致，并且安装ubuntu时就默认可用，所有Main组件中的软件包都可以免费获得安全更新和技术支持，OpenOffice.org Abiword和Apache网络服务器就在其中。  
  Universe：Universe包含了数千个不由Canonical官方支持的软件包，这些软件包授权于各种自由软件许可协议来自各种公共来源，组件只能通过互联网下载。  
  Multiverse：Multiverse包含非自由软件，也就是说软件的许可协议需求和Ubuntu Main组件的许可协议规则不符，用户需要负责验证自己是否有权使用该软件并且接受单一许可协议条款。其中包含VLC和Adobe FLash插件等。  
  Parter:   
  Restricted:  
8. `cd ../../../..`其中n个`..`、
9. `ls -d .*`
10. `ls *conf`
11. 文件类型为`l``b``d``c`  
  	其中l代表链接文件，d代表目录文件，b代表设备文件（设备文件是普通文件和程序访问硬件的入口），c代表字符设备文件，一次传输一个字节的设备被称为字符文件，如键盘、字符终端等，传输数据的最小但闻为一个字节
12. u代表所有者，x代表执行权限，+表示增加权限  
  即表示在此基础上增加可执行权限
13. `1,$s/unix/linux/g`
14. `set number`  见uploads
