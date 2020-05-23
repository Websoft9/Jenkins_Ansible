# Parameters

The Jenkins deployment package contains a sequence software (referred to as "components") required for Jenkins to run. The important information such as the component name, installation directory path, configuration file path, port, version, etc. are listed below.

## Path

### Jenkins

Jenkins installation directory:  */data/wwwroot/jenkins*  
Jenkins logs directory:  */data/logs/jenkins*  

### Java

Java Directory: */usr/lib/jvm*

### Nginx

Nginx vhost configuration file: */etc/nginx/conf.d/default.conf*    
Nginx main configuration file: */etc/nginx/nginx.conf*   
Nginx logs file: */var/log/nginx*  
Nginx rewrite rules directory: */etc/nginx/conf.d/rewrite* 

## Ports

You can control(open or shut down) ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** of your Cloud Server whether the port can be accessed from Internet.

You can run the cmd `netstat -tunlp` to list all used ports, and we list the following most useful ports for you:

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| TCP | 80 | HTTP requests for Jenkins Console| Required |
| TCP | 443 | HTTP requests for Jenkins Console| Optional |
| TCP | 8080 | Jenkins network port, used nginx for proxy | Optional |


## Version

You can see the version from product page of Marketplace. However, after being deployed to your server, the components will be automatically updated, resulting in a certain change in the version number. Therefore, the exact version number should be viewed by running the command on the server:


```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Nginx  Version
nginx -V

# Java version
java -v

# Docker Version
docker -v

# Jenkins version
yum info jenkins
apt show jenkins

```