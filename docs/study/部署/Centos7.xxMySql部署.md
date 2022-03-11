##### 1、 下载mysql源
```
    wget https://dev.mysql.com/get/mysql57-community-release-el7-9.noarch.rpm
```

##### 2、 进行repo的安装
```
    rpm -ivh mysql57-community-release-el7-9.noarch.rpm
```

##### 3、 安装MySql
```
    yum install mysql-server
```

*如果出现以下错误*

``` 
    The GPG keys listed for the "MySQL 5.7 Community Server" repository are already installed but they a ...
```
解决方案

```
    rpm --import https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
```



##### 4、 启动
```
    systemctl start mysqld
```


##### 5、 修改密码

```
    1 、 查看密码 grep 'temporary password' /var/log/mysqld.log
    2 、 修改密码 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456'；
    3 、 远程访问 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '@Chw2022ly'
```