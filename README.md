# SQLite-TIPs
###基本操作
创建数据库

```
$sqlite3  databaseName.db
```

查看数据库

```
>.database
seq  name             file                                                      
---  ---------------  ----------------------------------------------------------
0    main             /Users/cocoalee/testDB.db
```

退出数据库

```
>.quit
```
备份数据库

```
$sqlite3 testDB.db .dump > testDB.sql
```
恢复数据库

```
 $sqlite3 testDB.db < testDB.sql
```
###表操作
创建表

```
sqlite> CREATE TABLE TEST_TABLE(
   ...> ID  INT   PRIMARY    KEY    NOT NULL,
   ...> NAME                 TEXT   NOT NULL,
   ...> AGE                  INT    NOT NULL
   ...> );
```
查看表

```
sqlite> .tables
COMPANY     DEPARTMENT  TEST_TABLE  TIME 
```
删除表

```
sqlite> DROP TABLE TEST_TABLE;
```
插入数据 INSERT

```
sqlite> INSERT INTO TEST_TABLE(ID,NAME,AGE)
   ...> VALUES(1,'Cocoa',25);
sqlite> INSERT INTO TEST_TABLE VALUES(2,'Cocoa1',22);

```
查询   SELECT

```
sqlite> SELECT * FROM TEST_TABLE;
ID          NAME        AGE       
----------  ----------  ----------
1           Cocoa       25        
2           Cocoa1      22 
```
条件查询

```
sqlite> SELECT * FROM TEST_TABLE WHERE NAME = 'Cocoa1';
ID          NAME        AGE       
----------  ----------  ----------
2           Cocoa1      22   
sqlite> SELECT * FROM TEST_TABLE WHERE AGE > 24;
ID          NAME        AGE       
----------  ----------  ----------
1           Cocoa       25 
```

运算

```
sqlite> .mode line
sqlite> SELECT 23 + 34;
23 + 34 = 57
sqlite> SELECT 23 - 34;
23 - 34 = -11
sqlite> SELECT 23 * 34;
23 * 34 = 782
sqlite> SELECT 23 / 34;
23 / 34 = 0
sqlite> SELECT 123 / 34;
123 / 34 = 3
sqlite> SELECT 123 % 34;
123 % 34 = 21
```
---
tag:2015-08-30
