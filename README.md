# Jenkins自动化安装与部署

本项目是基于Ansible的[Jenkins](https://jenkins.io)自动化安装脚本，实现在Ansible上一键安装Jenkins。本项目是开源项目，支持MIT开源协议。如果您不熟悉Ansible的使用，您可以直接使用我们在公有云上提供的镜像。

## 操作系统

目前仅支持Ubuntu16.x以上部署此脚本

## 服务器配置要求

最低4G内存，30G系统盘空间，否则无法安装

## 版本

本项目采用Yum安装，版本查看


## 安装指南

本Ansible脚本支持root用户、普通用户（+su权限提升）等两种账号模式，也支持密码和秘钥对登录方式。

其中普通用户登录需要增加变量：

~~~
//假设普通用户的username为
admin_username: websoft9
~~~

## 组件
Jenkins,Nginx

## 使用指南

文档链接：[readme.txt](readme.txt)
