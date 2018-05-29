---
title: CentOS7安装Gradle
tags:
- gradle
categories:
- gradle
---
### 下载安装包
```
wget https://downloads.gradle.org/distributions/gradle-3.2.1-all.zip

```
### 解压安装
#### 解压前先安装zip和unzip
```
yum install zip unzip
```
#### 解压
```
unzip gradle-3.2.1-all.zip
```
### 配置环境变量
打开 /etc/ 目录下的 profile 文件：
```
vi /etc/profile
```
将如下代码追加到 profile 文件末尾：
```
GRADLE_HOME=/usr/software/gradle-3.2.1
export PATH=${GRADLE_HOME}/bin:${PATH}
```
重载/etc/profile这个文件
```
source /etc/profile
```
### 检验是否安装成功
```
gradle -version 
```

#### 参考
[CentOS7 安装Gradle
](https://blog.csdn.net/jeikerxiao/article/details/72235411)

[CentOS7下zip解压和unzip压缩文件](https://www.cnblogs.com/zhi-leaf/p/6002303.html)