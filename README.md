# tms-db

封装数据库操作，支持 MySQL，SQLite，支持读写分离。

每一次完整的业务处理过程称之为一个`context`，可以理解为它是业务级的事物。支持多次数据库请求使用同一个数据库连接，支持追踪 sql 语句，支持业务级事物的标识，支持在一次业务处理过程中涉及多个数据库。

编译

```
npm run build
```

# API

## 初始化

支持的配置信息如下：

```
{
  mysql:{
    master: {},
    writalbe: {}
  },
  sqlite:{
    path: '',
    memory: false
  }
}
```

## 实例

每个实例保留一个连接
