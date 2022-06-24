## 安装

```
yum install -y redis
```

## 设置开机自启

```
systemctl enable redis

# 判断是否为开机自启，开启时enabled，关闭时disabled
systemctl is-enabled redis
```

## 启动Redis

```
systemctl start redis
```

## 查看Redis状态

```
systemctl status redis
```

## 停止服务

```
systemctl stop redis
```

## 重启服务

```
systemctl restart redis
```

## 设置远程连接和密码

```
vim /etc/redis.conf
```

```
1. 注释掉 bing 127.0.0.1
2. 将保护模式改为no，protected-mode-mode no，默认就是no
3. 修改密码，requirepass ***
```

## 测试密码

```
redis-cli auth 密码
```

