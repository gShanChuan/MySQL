# 1. MySql的安装与使用
## 1.1 启动和停止MySQL服务
__方式一：通过计算机管理方式__  
&emsp;右击计算机—管理—服务—启动或停止MySQL服务

__方式二：通过命令行方式__  
* 启动：`net start mysql服务名 ` 
* 停止：`net stop mysql服务名`

## 1.2 MySQL服务端的登录和退出
__方式一：MySQL 8.0 Command Line Client__  
&emsp;仅限root用户  

__方式二：通过命令行方式__   
&emsp;`mysql –h 主机名 –u用户名 –p`

## 1.3 MySQL常用命令
* 查看 mysql 中有哪些个数据库:   
  `show databases;`
* 使用一个数据库:   
  `use 数据库名称;`
* 新建一个数据库:   
  `create database 数据库名;` 
* 查看当前所在的库：  
  `select database();`
* 查看当前库的所有表:  
  `show tables;`
* 查看指定的数据库中有哪些数据表:   
  `show tables from 库名;`
* 创建表：
    ```
    create table 表名(  
    列名1 列类型1，
    列名1 列类型1，
    ...
    列名n 列类型n
    );```
* 查看表的结构：  
  `desc 表名;`
* 查看表里的数据：  
  `select * from 表名;`
* 查看mysql数据库的版本：  
  `select version(); 或 mysql --version`
## 1.4 MySQL语法规范
* 不区分大小写，关键字最好大写 
* 命令用 ; 结尾
* 命令可以换行
* 注释：
    * 单行注释：#注释文字 或 --注释文字
    * 多行注释：/\*注释文字\*/

# 2. SQL语言
## 2.1 DQL语言
* __2.1.1 基础查询__  
语法：  
&emsp;___select 查询列表 from 表名;___  
&emsp;类似于：System.out.println();  
特点：  
&emsp;1.查询列表可以是：表中的字段、常量值、表达式、函数  
&emsp;2.查询的结果是一个虚拟的表格

    * __查询字段__
    ```
    #查询表中的单个字段
    SELECT last_name FROM employees;

    #查询表中的多个字段
    SELECT last_name,salary,email FROM employees;

    #查询表中所有的字段
    #`字段名`标识其为字段名
    SELECT `employee_id`,`first_name`,`last_name`,`email`,`phone_number`,
    `job_id`,`salary`,`commission_pct`,`manager_id`,`department_id`,`hiredate`
    FROM employees;

    SELECT * FROM employees;
    ```
    * __查询常量、表达式、函数__
    ```
    #查询表中的单个字段
    SELECT last_name FROM employees;

    #查询表中的多个字段
    SELECT last_name,salary,email FROM employees;

    #查询表中所有的字段
    #`字段名`标识其为字段名
    SELECT `employee_id`,`first_name`,`last_name`,`email`,`phone_number`,
    `job_id`,`salary`,`commission_pct`,`manager_id`,`department_id`,`hiredate`
    FROM employees;

    SELECT * FROM employees;
    ```






  





