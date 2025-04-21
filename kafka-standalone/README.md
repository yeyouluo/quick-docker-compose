# kafka

## 启动

```
docker compose up -d
```

## 访问kafka-ui

浏览器访问 [http://127.0.0.1:8080](http://127.0.0.1:8080)

帐号密码：admin/admin123

## 其他细节

注意要在hosts中配置映射(建议使用SwitchHosts)，否则其他程序无法正常使用：

```
127.0.0.1 kafka
```
