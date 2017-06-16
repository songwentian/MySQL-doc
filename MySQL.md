# 我的日志

## MySQL基本指令

*安装mysql指令*
 - sudo apt-get update  更新源
 - sudo apt-get install tasksel
 - sudo tasksel
 
*连接到本机上的MYSQL*
 - 键入命令mysql -u root -p，回车后提示你输密码.注意用户名前可以有空格也可以没有空格
 - 直接回车即可进入到MYSQL中了，MYSQL的提示符是： mysql>
 - 退出mysql命令：“exit+回车”

*创建数据库*
 - create database <数据库名>
 
*显示数据库*
 - show databases

*删除数据库*
 - drop database <数据库名>
 
*使用数据库*
 - use <数据库名> 
 
*输出相关的数据库信息*
 - 命令：mysql> select database();
 
*创建表*
 - 命令：create table <表名> (
 
*查看表结构*
 - desc <表名>
 
*删除表*
 - 命令：drop table <表名>
 
*往表中添加数据*
 - 命令：insert into <表名> [( <字段名1>[,..<字段名n > ])] values ( 值1 )[, ( 值n )]
 
*查询表中的数据*
 1. 查询所有行 命令： select <字段1，字段2，...> from < 表名 > where < 表达式 >
 2. 查询前几行数据 例如：查看表 MyClass 中前2行数据 mysql> select * from MyClass order by id limit 0,2;
 
*删除表中的数据*
 - delete from 表名 where 表达式
 
*修改表中的数据*
 - update 表名 set 字段=新值,... where 条件 例：mysql> update MyClass set name='Mary' where id=1;
 
*在表中增加字段*
 - 命令：alter table 表名 add字段 类型 其他; 例如：在表MyClass中添加了一个字段passtest，类型为int(4)，默认值为0 mysql> alter table MyClass add passtest int(4) default '0'
 
*添加索引*
 1. 加索引 mysql> alter table 表名 add index 索引名 (字段名1[，字段名2 ...]); 例子： mysql> alter table employee add index emp_name (name);
 2. 加主关键字的索引 mysql> alter table 表名 add primary key (字段名); 例子： mysql> alter table employee add primary key(id);
 3. 加唯一限制条件的索引 mysql> alter table 表名 add unique 索引名 (字段名); 例子： mysql> alter table employee add unique emp_name2(cardnumber);
 
*查看索引*
 - show index from <表名>
 
*删除索引*
 - 除某个索引 mysql> alter table 表名 drop index 索引名; 例子： mysql>alter table employee drop index emp_name;
 
*修改字段*
 1. mysql> ALTER TABLE table_name ADD field_name field_type;
 2. 修改原字段名称及类型： mysql> ALTER TABLE table_name CHANGE old_field_name new_field_name field_type;
 
*删除字段*
 - MySQL ALTER TABLE table_name DROP field_name;
 
*修改表名*
 - rename table 原表名 to 新表名;
