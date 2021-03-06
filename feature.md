# 数据库驱动
ESAP整合了多种数据库驱动，可以连接大部分数据库。

## SqlServer 2005+
```yaml
driver: mssql
port: 1433
server: localhost
user: sa
pwd: 123
db: esapp1
```

## SqlServer 2000
```yaml
driver: sql2000
port: 1433
server: localhost
user: sa
pwd: 123
db: esapp1
```

## mysql
```yaml
driver: mysql
port: 3306
server: localhost
user: root
pwd: 123
db: db
```

## postgresql
```yaml
driver: postgres
port: 5432
server: localhost
user: postgres
pwd: 123
db: db
```

## sqlite
```yaml
driver: sqlite
db: "d:\\mydb.db"
```

## access
```yaml
driver: access
db: "d:\\mydb.mdb"
```

## excel
```yaml
driver: excel
db: "d:\\mydb.xls"
```

## 驱动企业ERP平台
ESAP服务器直接与SQL交互，使用SQL的程序或系统都可以移植，包括并不限于下列项目：

+ 聚表
+ 勤哲
+ 冠日
+ 金蝶
+ 用友
+ 速达
+ SAP
+ FineReport
+ 快表
+ 云表

## 驱动Excel服务器

* 如果使用聚表2.3.22+版，将安装包中的`JUAP_提醒`模板导入即可。

* 如果使用勤哲9.4+版，将安装包中的`ESAP_提醒`模板导入即可。

* 如果是聚表其他版，或者勤哲9.4以下版本，例如7.1.7，8.4，9.2等，则需自建这些`模板`，并保证表名和字段名一致。

## 驱动其他系统

* 只要是使用`SQL`，都可以自行建立这些`esap_`前缀的数据表，并保证`名称类型`一致即可。
