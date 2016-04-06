<!--
author: cailinhan
date: 2016-04-05
title: mysql用户管理
tags: mysql
category: database
status: publish
summary: 你好！GitBlog
-->

创建用户
```
CREATE USER 'username'@'host' IDENTIFIED BY 'password'; 
```
授权超级管理员
```
GRANT all ON *.* TO linhan IDENTIFIED BY 'password' WITH GRANT OPTION;
```
开启root远程权限
```
GRANT all on *.* to root@'%' identified by 'password' WITH GRANT OPTION;
```
修改密码
```
UPDATE user SET password=PASSWORD('password') WHERE user='linhan';
```
刷新权限表
```
flush privileges
```
WEB用户
```
GRANT CREATE,DROP,ALTER,CREATE VIEW,SHOW VIEW,REFERENCES,SELECT, INSERT, UPDATE, DELETE
    ON *.*
    TO 'linhan'@'%' IDENTIFIED BY 'password' WITH GRANT OPTION;
```