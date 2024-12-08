# Nand2Tetris
计算机系统要素：从零开始构建现代计算机
### 关于为什么要学这本书：
大一的必修课 Computer Systems Fundamentals 课程设计提及本书，区别在与实际教学使用mips。


## 软件安装问题（MacOS）
请浏览：https://www.nand2tetris.org/software 

在“Install the Nand2Tetris Software Suite”部分，安装教程指示在终端中输入“~/Desktop/nand2tetris/tools/HardwareSimulator.sh”。

而终端中显示类似于如下：
```bash
zsh: permission denied: /Users/group/Desktop/nand2tetris/tools/HardwareSimulator.sh
```
其原因应是脚本文件没有执行权限，可以这样操作：

1.在终端中运行以下命令来检查 HardwareSimulator.sh 文件的权限：
```bash
ls -l ~/Desktop/nand2tetris/tools/HardwareSimulator.sh
```
会看到类似输出：
```bash
-rw-r--r--  1 user  group  1234 Date HardwareSimulator.sh
```
如果权限中没有 x ，说明文件没有可执行权限。

2.运行以下命令给脚本添加执行权限：
```bash
chmod +x ~/Desktop/nand2tetris/tools/HardwareSimulator.sh
```

3.提供一个可以快速添加所有文件权限的方法：

3.1 进入目录
```bash
cd ~/Desktop/nand2tetris/tools
```
3.2 一次性为所有 .sh 文件添加执行权限
```bash
chmod +x *.sh
```
3.3 检查访问权限
```bash
ls -l
```
终端应有类似输出如下：
```bash
-rwxr-xr-x  1 user  group  size date HardwareSimulator.sh
-rwxr-xr-x  1 user  group  size date CPUEmulator.sh
-rwxr-xr-x  1 user  group  size date Assembler.sh
-rwxr-xr-x  1 user  group  size date VMEmulator.sh
-rwxr-xr-x  1 user  group  size date JackCompiler.sh
```
出现 x 则表示成功添加权限。
