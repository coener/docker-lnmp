# docker-lnmp

### 前置条件

- docker

- docker-compse

### 使用镜像

```
nginx:1.16.0
redis:5.0.5
mysql:8.0.16
php:7.3.5-fpm
```

##   开始使用

权限(根据自定义配置来给权限)，此目录作为网站站点

```
mkdir /data
chmod -R 755 /data
```

运行

```
git clone https://github.com/coener/docker-lnmp.git
cd docker-lnmp
docker-compose up -d
```
###小技巧

我们可以通过别名在主机上为其它容器添加一些快捷命令。 比如：

```
vim ~/.bashrc
# 添加php与mysql容器执行命令
alias php='docker exec -it php php'
alias composer='docker exec -it php composer'
alias mysql='docker exec -it mysql mysql'
alias redis-cli='docker exec -it redis redis-cli'

# 生效
source ~/.bashrc

```
