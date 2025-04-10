ClickHouse 单机版本

## 访问信息

端口：8123

帐号：default

密码：admin123

## 修改密码

- 获取sha256

```shell
$ echo -n 'admin123' | sha256sum | tr -d '-'
240be518fabd2724ddb6f04eeb1da5967448d7e831c08c8fa822809f74c720a9
```

- 在conf/users.xml 第20行修改
