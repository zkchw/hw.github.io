##### 1、 创建环境根目录

```
   mkdir /usr/java
```

##### 2、 解压压缩包到环境根目录


```
    tar -zxvf jdk-8u171-linux-x64.tar.gz -C /usr/java/
```


##### 3、 配置环境变量

```{.line-numbers}
1 vi  /etc/profile
2 追加到最后
export JAVA_HOME=/usr/java/jdk1.8.0_171
export CLASSPATH=.:${JAVA_HOME}/jre/lib/rt.jar:${JAVA_HOME}/lib/dt.jar:${JAVA_HOME}/lib/tools.jar
export PATH=$PATH:${JAVA_HOME}/bin
```

#### 4、验证
```
    java -version
    
```

![GitHub Logo](.images/cent7_jdk.png)


