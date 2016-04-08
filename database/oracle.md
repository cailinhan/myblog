<!--
author: cailinhan
date: 2016-04-05
title: Oracle创建数据库
tags: oracle
category: database
status: publish
summary: 你好！GitBlog
-->
创建表空间
```
create tablespace my_data  
datafile 'my_data.dbf' 
size 100m  
autoextend on  
next 100m maxsize 20480m  
extent management local;
```
创建临时表空间
```
create temporary tablespace my_temp  
tempfile 'my_temp.dbf' 
size 100m  
autoextend on  
next 100m maxsize 20480m  
extent management local;
```
创建用户
```
create user linhan identified by "123456"  
default tablespace my_data  
temporary tablespace my_temp;
```
授权
```
grant connect,resource,dba to tahoe;
```