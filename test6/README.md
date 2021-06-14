# 基于Oracle的图书管理系统的数据库设计



## 第1章 系统概述

 随着现代科学技术的进步，人类社会正逐渐走向信息化，图书馆拥有丰富的文献信息资源，是社会系统的重要组成部分，在信息社会中作用愈来愈重要。在当今知识大爆炸的时代，图书作为信息的一种载体，仍是人们获得知识的一种重要途径，因而作为图书管理与借阅的图书馆，它的运行情况则关系到知识的传播速度问题。以往旧的图书管理模式完全是手工操作，从新书的购买、编码、入库、上架，到借阅、续借、归还、查询，无-不是人工处理，需要大量的劳动力与工作量，而且由于人为的原因造成一些错误，也是再所难免的。当读者想要借阅一本书时，首先要查询大量的卡片，而且要有一定的图书管理知识，才能很快的查到。自己想要的图书，在借阅过程中还要填写许多相关的卡片，使得图书的管理效率低下，图书流通速度较慢，因而从一定程度上也影响了知识的传播速度。
   图书馆的信息化从最初的对图书馆业务管理实行信息化发展到对图书馆各个业务流程进行系统和网络话化管理,并建立大规模以个体文献目录联机查询为主的资源共享系统。进入21世纪，充分利用计算机网络和信息技术，逐步实现不同载体的实体文献的信息化管理和多方位的联机查询。图书馆的计算机信息化管理，就是将传统图书馆业务的手工操作转变成由计算机管理，既图书馆的图书期刊、音像资料等各种载体文献的采编、典藏、流通、检索及常规业务管理等工作，利用计算机技术，进行高效、准确的信息化管理。其根本目的是实现区域内.及地区、国家、国家间的资源共享。要达到资源共享的目的，必须制定-定的标准，只有各个系统都遵循这些标准，不同的系统间才可以实现联机查询、资源共享的效果。

## 第2章 数据结构需求分析

**书馆管理信息系统需要完成功能主要有:**

(1)  读者基本信息的输入，包括借书证编号、读者姓名、读者性别。

(2)  读者基本信息的查询、修改，包括读者借书证编号、读者姓名、读者性别等。

(3)  书籍类别标准的制定、类别信息的输入，包括类别编号、类别名称。

(4)  书籍类别信息的查询、修改，包括类别编号、类别名称。

(5)  书籍库存信息的输入，包括书籍编号、书籍名称、书籍类别、作者姓名、出版社名称、出版日期、登记日期。

(6)  书籍库存信息的查询，修改，包括书籍编号、书籍名称、书籍类别、作者姓名、出版社名称、出版日期登记日期等。

(7)  借书信息的输入，包括读者借书证编号、书籍编号、借书日期。

(8)  借书信息的查询、修改，包括借书证编号、读者编号、读者姓名、书籍编号、书籍名称、借书日期等。

(9)  还书信息的输入，包括借书证编号、书籍编号、还书日期。

(10) 还书信息的查询和修改，包括还书读者借书证编号、读者姓名、书籍编号、书籍名称、借书日期、还书日期等。

(11) 超期还书罚款输入，还书超出期限包括超出期限还书的读者借书证号，书籍编号，罚款金额。

(12) 超期还书罚款查询，删除，包括读者借书证编号、读者姓名、书籍编号、书籍名称，罚款金额等



 

## 第3章 事务处理需求分析

(1)  在读者信息管理部分,要求:

a.   可以查询读者信息。

b.   可以对读者信息进行添加及删除的操作。

(2)  在书籍信息管理部分，要求:

a.   可以浏览书籍信息，要求:

b.   可以对书籍信息进行维护，包括添加及删除的操作。

(3)  在借阅信息管理部分,要求:。

a.   可以浏览借阅信息。

b.   可以对借阅信息进行维护操作。

(4)  在归还信息管理部分，要求:

a.   可以浏览归还信息

b.   对归还信息可修改维护操作

(5)  在管理者信息管理部分，要求:

a.   显示当前数据库中管理者情况。

b.   对管理者信息维护操作。

(6)  在罚款信息管理部分,要求:

a.   可以浏览罚款信息

b.   对罚款信息可以更新

 



 

## 第4章 关系模式

(1)  书籍类别 (种类编号，种类名称)

(2)  读者(借书证编号，读者姓名，读者性别，读者种类，登记时期)

(3)  书籍(书籍编号，书籍名称，书籍类别，书记作者，出版社名称，出版日期，登记日期)

(4)  借阅(借书证编号，书籍编号，读者借书时间)

(5)  还书(借书证编号，书籍编号，读者还书时间)

(6)  罚款(借书证编号，读者姓名，借书证编号，书籍编号，读者借书时间)

 

 

 



 

## 第5章 方案图表设计

1、 图书类别实体E-R图

 <img src = ".\README.assets\clip_image002.jpg" />



2、读者信息实体E-R图：

<img src = ".\README.assets\clip_image004.jpg" /> 

3、信息实体E-R图：

<img src = ".\README.assets\clip_image006.jpg" /> 

4、记录信息实体E-R图

<img src = ".\README.assets\clip_image008.jpg" /> 

5、记录信息实体E-R图

<img src = ".\README.assets\clip_image010.jpg" /> 

6、罚款信息实体E-R图

<img src = ".\README.assets\clip_image012.jpg" /> 

7、总体信息实体E-R图

<img src = ".\README.assets\clip_image014.jpg" /> 

## 第6章 数据表的设计

1 书籍类别信息表

| 表中列名    | 数据类型 | 是否为空 | 主键/外键 | 说明     |
| ----------- | -------- | -------- | --------- | -------- |
| bookstyleno | varchar  | 否       | 主键      | 种类编号 |
| bookstyle   | varchar  | 否       |           | 种类名称 |

 

2 读者信息表格               

| 表中列名   | 数据类型 | 是否为空 | 主键/外键 | 说明         |
| ---------- | -------- | -------- | --------- | ------------ |
| readerid   | varchar  | 否       | 主键      | 读者借书证号 |
| readername | varchar  | 否       | 外键      | 读者姓名     |
| readersex  | varchar  | 否       |           | 读者性别     |
| readertype | varchar  | 是       |           | 读者种类     |
| regdate    | date     | 是       |           | 登记日期     |

 

3书籍信息表

| 表中列名    | 数据类型 | 是否为空 | 主键/外键 | 说明       |
| ----------- | -------- | -------- | --------- | ---------- |
| bookid      | Varchar  | 否       | 主键      | 书籍编号   |
| bookname    | Varchar  | 否       |           | 书籍名称   |
| bookstyle   | Varchar  | 否       |           | 书籍类别   |
| bookauthor  | Varchar  | 否       |           | 书籍作者   |
| bookpub     | Varchar  | 是       |           | 出版社名称 |
| bookpubdate | Date     | 是       |           | 出版日期   |
| bookindate  | Date     | 是       |           | 登记日期   |
| isborrowed  | Varchar  | 否       |           | 是否被借出 |

 

4借阅记录信息表

| 表中列名   | 数据类型 | 是否为空 | 主键/外键 | 说明           |
| ---------- | -------- | -------- | --------- | -------------- |
| readerid   | Varchar  | 否       | 外主键    | 读者借阅证编号 |
| bookid     | Varchar  | 否       | 外主键    | 书籍编号       |
| borrowdate | Varchar  | 否       |           | 读者借书时间   |

 

5借阅记录信息表

| 表中列名   | 数据类型 | 是否为空 | 主键/外键 | 说明           |
| ---------- | -------- | -------- | --------- | -------------- |
| readername | Varchar  | 否       | 外主键    | 读者借阅证编号 |
| readerid   | Varchar  | 否       | 外主键    | 书籍编号       |
| returndate | Date     | 否       |           | 读者还书时间   |

 

6罚款记录信息表

| 表中列名   | 数据类型 | 是否为空 | 主键/外键 | 说明           |
| ---------- | -------- | -------- | --------- | -------------- |
| readerid   | varchar  | 否       |           | 读者借书证编号 |
| readername | varchar  | 否       |           | 读者姓名       |
| bookid     | varchar  | 否       | 外主键    | 书籍编号       |
| bookname   | varchar  | 否       |           | 书籍名称       |
| bookfee    | varchar  | 否       |           | 罚款金额       |
| borrowdate | Date     | 否       |           | 借阅时间       |

 



 

## 第7章 数据库各表实现

7.1 创建数据库

创建了一个名叫tspdb的数据库，指定了它的存储位置，以及创建了数据库tspdb的管理员，具体sql如下

```sql
create PLUGGABLE database tspdb admin user ts 
identified by 123
file_name_convert=
('/home/oracle/app/oracle/oradata/orcl/pdbseed/',
' /home/oracle/app/oracle/oradata/orcl/tspdb')
```



<img src = ".\README.assets\clip_image016.jpg" /> 

7.2 授权给数据库tspdb

<img src = ".\README.assets\clip_image018.jpg" /> 

 

7.3 创建表空间

```sql
create temporary tablespace TSGL_TEMP  
tempfile '/opt/TSGL/TSGL_TEMP.dbf'  
size 50m    
autoextend on    next 50m maxsize 20480m   
extent management local;     

create tablespace TSGL_DATA 
logging    
datafile '/opt/TSGL/TSGL_DATA.dbf'  
size 50m    
autoextend on    
next 50m maxsize 20480m   
extent management local;

```

<img src = ".\README.assets\clip_image020.jpg" /> 

 

7.4 创建用户赋权

```sql
create user TSGL identified by 123456 
default tablespace TSGL_DATA  
temporary tablespace TSGL_TEMP ;
grant connect,resource,dba to TSGL;
```

<img src = ".\README.assets\clip_image022.jpg" /> 

**7.5 书本类别表建立**

```sql
create table book_style (  
  bookstyleno varchar(30) primary key,    
bookstyle varchar(30) ); 
```

<img src = ".\README.assets\clip_image023.png" /> 

**7.6** **创建书库表**

  ```sql
create table system_books (     
    bookid varchar(20) primary key,   
    bookname varchar(30) Not null,    
    bookstyleno varchar(30) Not null,   
    bookauthor varchar(30),   
    bookpub varchar(30) ,   
    bookpubdate datetime,   
    bookindate datetime , 
    isborrowed varchar (2) ,  foreign key (bookstyleno) references book_style (bookstyleno) 
);
  ```

<img src = ".\README.assets\clip_image025.jpg" /> 

 

 

**7.7** **借书记录表建立**

```sql
create table borrow_record  (
    bookid varchar(20)  primary key,   
    readerid varchar(9),   
    borrowdate datetime,   
    foreign key (bookid) references system_books(bookid),   
    foreign key (readerid) references system_readers(readerid) 
);
```

<img src = ".\README.assets\clip_image026.png" /> 

 

**7.8** **还书记录表建立**

```sql
create table return_record ( 
    bookid varchar(20) primary key,   
    readerid varchar(9),   
    returndate datetime,  
    foreign key (bookid) references system_books(bookid),   
    foreign key (readerid) references system_readers(readerid)
);
```

<img src = ".\README.assets\clip_image027.png" /> 



**7.9** **罚款单表建立**

```sql
create table reader_fee ( 
    readerid varchar(9)not null,   
    readername varchar(9)not null ,   
    bookid varchar(20) primary key,   
    bookname varchar(30) Not null,    
    bookfee varchar(30) ,   
    borrowdate datetime,  
    foreign key (bookid) references system_books(bookid),   
    foreign key (readerid) references system_readers(readerid)
);
```

<img src = ".\README.assets\clip_image028.png" /> 

 

## 第8章 数据库实施

（1）将书籍类别加入表book_style中

 ```sql
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (1，人文艺术类):
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (2，自然科学类);
INSERT INTO "TSGL"."BOOK_STYLE" ALUES (3，社会科学类);
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (4，图片艺术类);
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (5，政治经济类);
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (6，工程技术类);
INSERT INtO "TSGL"."BOOK_STYLE" ALUES (7，语言技能类);
 ```

<img src = ".\README.assets\clip_image029.png" /> 

（2）将已有的图书加入system_books表中

 ```sql
INSERT INTO "TSGL"SYSTEM_ BOOKS" ALUES (00125415153', 计算机组成原理，'6' '王爱英，'清华大学出版社’，TO_ DATE(2001-01-03 00:00:00'， 'YYYY-MM-DDHH24:MI:SS)。TO_ DATE(2003-11-15 00:00:00', 'YYYY-MM-DD HH24:MI:SS), '0');

INSERT INTO "TSGL"."SYSTEM BOOKS" ALUES (00456456', 数据库原理’，'6'; 萨师煊; '高等教育出版社'，TO_ DATE(2001-01-03 0:00:00, YYYY-MM-DD HH24:MI:SS'),TO_ DATE(2003-11-15 00:00:00'， 'YYY Y-MM-DD HH24:MISS), '1);

INSERT INTO "TSGL"."SYSTEM BOOKS" ALUES (12215121'; C程序设计'，'6';谭浩强，清华大学出版社'，TO_ DATE(2001-01-03 00:00:00%， 'YYYY-MM-DD HH24:MI:SS),TO_ DATE(2003-11-15 00:00:00', 'YYY Y-MM-DD HH24:MISS), '1);

INSERT INTO "TSGL"."SYSTEM BOOKS" VALUES (9787308020558; '计算机体系结构，'6'; '石教英'，浙江大学出版社，TO_ DATE(2001-01-03 00:00:001 'YYYY-MM-DDHH24:MI:SS'), TO_ DATE(2003-11-15 000:00; 'YYYY-MM-DD HH24:MI:SS), '1);INSERT INTO"TSGL"."SYSTEM BOOKS" ALUES (45456141414', 数据结构(C语言版)，'6', '吴伟民，严蔚敏，9清华大学出版社'，TO_ DATE(2001-01-03 00:00:00',YYYY-MM-DD HH24:MI:SS)， TO_ DATE(2003-11-15 00:00:00'， YYYY-MM-DDHH24:MI:SS), '1); 

INSERT INTO "TSGL"."SYSTEM BOOKS" ALUES ('5455515', 中华历史5000年，'1, '吴强，，北京大学出版社，TO_DATE(2001-01-03 0:00:00， YYYY-MM-DDHH24:MI:SS), TO_ DATE(2003-11-15 00:00:00'， 'YYYY-MM-DD HH24:MI:SS), '0);INSERT INTO "TSGL""SYSTEM BOOKS" ALUES (015115'， 古代埃及'，'3', 赵文华，'北京大学出版社'，TO_ DATE(2001-01-03 00:00:00'， 'YYYY-MM-DD HH24:MI:SS),TO_ DATE(2003-11-15 00:00:00'， 'YYY Y-MM-DD HH24:MISS). '0);

INSERT INTO "TSGL"SYSTEM BOOKS" ALUES (1514514, 日本文化, '1'; 吴小鹏’;北京大学出版社’' TO_ DATE(2001-01-03 00:00:00'， 'YYYY-MM-DD HH24:MI:SS),TO_ DATE(2003-11-15 00:00:00%, 'YYYY-MM-DD HH24:MI:SS), '1);

INSERT INTO "TSGL"."SYSTEM BOOKS" ALUES (15154656', 微观经济学'，'5'; 李小刚，北京大学出版社', TO_ DATE(2001-01-03 00:00:00%， 'YYYY-MM-DD HH24:MI:SS),TO_ DATE(2003-11-15 000:00 'YYYY-MM-DD HH24:MI:SS), '0);

INSERT INTO "TSGL"SYSTEM _BOOKS" ALUES (5658'; 影视文学，'4', 苏庆东',北京大学出版社，TO_DATE(2001-01-0300:00:00， YYYY-MM-DD HH24:IMI:SS).TO_ DATE(2003-11-15 00:0:00', 'YYYY-MM-DD HH24:MI:SS), '1);

INSERT INTO "TSGL" "SYSTEM BOOKS" ALUES ('565800020'， 探索宇宙奥秘'，'2'; '苏庆东，北京大学出版社，TO_DATE(2001-01-03 00:00:00'， 'YYYY-MM-DDHH24:MI:SS), TO_ DATE(2003-11-15 00:00:00'， YY Y Y-MM-DD HH24:MI:SS), '0);

INSERT INTO "TSGL""SYSTEM _BOOKS" ALUES (00125415152'; 计算机组成原理，'6', '王爱英，'清华大学出版社'。TO_ DATE(2001-01-03 00:00:00'， 'YYYY-MM-DDHH24:MISS'), TO_ DATE(2003-11-15 00:00:00, YYYY-MM-DD HH24:MI:SS), '0);
 ```

<img src = ".\README.assets\clip_image031.jpg" /> 

 

（3）将已有图书证的读者加入system_readers表中

```sql
INSERT INTO "TSGL""SYSTEM_ READERS" VALUES ('X05620206';陈特':男',学生'，TO_ DATE(2003-11-15 00:00:00, 'YYY Y-MM-DD HH24:MI:SS));

INSERT INTO "TSGL"."SYSTEM READERS" VALUES (X05620207';陈远鹏’，男',学生'，TO_DATE(2005-09-23 00:00:00', YY Y Y-MM-DD HH24:MISS));

INSERT INtO "TSGL"SYSTEM_ READERS" VALUES (X05620204', 赵铭静女'，学生'，TO_DATE(2005-09-23 00:00:00', 'YY Y Y-MM-DD HH24:MI:SS));

INSERT INTO "TSGL""SYSTEM READERS" VALUES (X05620202'; 潘虹':女',学生，TO_ DATE(2005-09-23 00:00:00', 'YYYY-MM-DD HH24:MI:SS));

INSERT INTO "TSGL"."SYSTEM _READERS" VALUES (008415; '蒋伟':男'，'教师TO_ DATE(2005-09-23 00:00:00', 'YYY Y-MM-DD HH24:MI:SS));

INSERT INTO "TSGL"SYSTEM_ READERS" VALUES (001456', '李叶风，女，'教师:TO_ DATE(2005-09-23 00:00:00'， 'YYY Y-MM-DD HH24:MISS));

```

<img src = ".\README.assets\clip_image033.jpg" /> 

 

 

 

 

（4）添加已借书读者的记录，同时将在已借出的借阅标记置

```sql
insert into borrow_record(bookid,readerid,borrowdate)  values('00125415152','X05620202','2007-09-27 11:24:54.123') 
update system_books set isborrowed=0  
where  bookid='00125415152'  

insert into borrow_record(bookid,readerid,borrowdate)  values('00125415153','X05620206','2007-12-27 08:26:51.452') 
update system_books set isborrowed=0  
where  bookid='00125415153' and isborrowed='1' 

insert into borrow_record(bookid,readerid,borrowdate) values('5455515','X05620207','2007-12-27 08:26:51.452') 
update system_books set isborrowed=0  
where bookid='5455515' and  isborrowed='1'

insert into borrow_record(bookid,readerid,borrowdate) values('015115','X05620204','2007-10-21 12:11:51.452') 
update system_books set isborrowed=0  
where bookid='015115' and  isborrowed='1'  

insert into borrow_record(bookid,readerid,borrowdate) values('15154656','001456','2007-12-28 14:11:51.312') 
update system_books set isborrowed=0  
where bookid='15154656' and  isborrowed='1'  

insert into borrow_record(bookid,readerid,borrowdate) values('565800020','008415','2007-08-28 15:11:31.512') 
update system_books set isborrowed=0  
where bookid='565800020' and  isborrowed='1'

```

<img src = ".\README.assets\clip_image035.jpg" /> 

 

 

 



 

## 第9章 系统定时自动备份

（1）编写rman增量备份脚本

```sql
#rman_level1.sh 
#!/bin/sh
export NLS_LANG='SIMPLIFIED CHINESE_CHINA.AL32UTF8'
export ORACLE_HOME=/home/oracle/app/oracle/product/12.1.0/dbhome_1  
export ORACLE_SID=orcl  
export PATH=$ORACLE_HOME/bin:$PATH  

rman target / nocatalog msglog=/home/oracle/rman_backup/lv1_`date +%Y%m%d-%H%M%S`_L0.log << EOF
run{
configure retention policy to redundancy 1;
configure controlfile autobackup on;
configure controlfile autobackup format for device type disk to '/home/oracle/rman_backup/%F';
configure default device type to disk;
crosscheck backup;
crosscheck archivelog all;
allocate channel c1 device type disk;
backup as compressed backupset incremental level 1 database format '/home/oracle/rman_backup/dblv1_%d_%T_%U.bak'
   plus archivelog format '/home/oracle/rman_backup/arclv1_%d_%T_%U.bak';
report obsolete;
delete noprompt obsolete;
delete noprompt expired backup;
delete noprompt expired archivelog all;
release channel c1;
}
EOF
exit
```

（2）启动linux的crontab定时任务，每天的凌晨一点自动进行备份

<img src = ".\README.assets\clip_image036.png" /> 

 

（3）演示备份与恢复：

   

① 执行rman_level1.sh脚本，进行数据库备份

<img src = ".\README.assets\clip_image038.jpg" /> 

 

② 破坏数据库，删除表空间文件xw_space1.bdf

<img src = ".\README.assets\clip_image040.jpg" /> 

 

③启用rman，进行数据库恢复

<img src = ".\README.assets\clip_image042.jpg" /> 

<img src = ".\README.assets\clip_image044.png" /> 

④查看删除的xw_space1，是否恢复

<img src = ".\README.assets\clip_image046.jpg" /> 

 

⑤由此可见，恢复成功

## 第10章 容灾

Data Guard是oracle提供的用于确保企业数据高可用性、数据保护和灾难恢复的一种方案。通过提供日志传送服务、日志应用服务和角色转换服务，DataGuard简化了备用数据库的建立、维护和管理操作，并且Data Guard使用产品数据库的事物变化来维护备用数据库。如果因不可预计的故障导致产品数据库不可用，则Data Guard可以切换到备用数据库，并将其转变为产品数据库，以最小化故障所引起的停机时间。Data Guard由一个产品数据库和一个或多个备用数据库组成，并且这些数据库可以分布到不同的位置和不同地区，它们之间的互联通过oracle net 来完成的。主数据库。主数据库是指用于存放应用系统数据的oracle数据库，它也被称为产品数据库或目标数据库。备用数据库。 备用数据库是主数据库的事务致性副本， 它包括物理备用数据库和逻辑备用数据库两种类型，每个主数据库最多可以建立9个备用数据库。

 

三种数据保护模式:

大数据保护模式( MAXIMIZEPROTECT IION);提供最高等级的数据保护，重作信息从主库同步送到备用库。直到备用库成功接收重作信息，主库上的事务才会提交。如果由于网络等问题，导致备用库不可用，那么主库也同时会被关闭。这种模式保证了完全没有数据罢失。

最大可用性模式(MAXIMIZE AVAILABILITY);在备用库正常的情况下，该模式提供了跟“最大数据保护模式”一样的机制，保证没有任何数据丢失。如果备用库不可用，那么将转换到“最大性能模式”，操作可以在主库上继续执行。当备用库重新可用之后，将会继续同步。但是如果在同步完成之前，主库由于故障损坏，将会丢失数据

最大性能模式(MAXIMIZE PERFORMANCE);这种模式下，主库上的重作信息是异步传递到备用库上，不论备用库上是否已经成功接收了重作信息，主库上的操作都会成功执行。所以这种模式

提供了最好的性能，但是最低的数据保护。这是Oracle10g配置DataGuard的默认模式。

 

(1)在两台主机上分别安装ORACLE数据库并建立数据库。

提示:两台主机ORACLE的安装目录和数据文件存放目录尽可能保持一致

两台数据库的SID均配置为ORACLE10主数据唯一-数据库名为primary,备用唯一数据库名为standby

(3)配置监听程序和网路服务名。因为主数据库和备用数据库的交互时通过oracle net来完成的，所以必须进行网络配置。

![img](F:\github\oracle\test6\README.assets\clip_image048.jpg)

 

管理物理备用数据库。

开始应用重做。

命令:

```sql
sql> alter database recover managed standby  

database disconnect from session;

取消重做应用。

Sql> alter database recover managed standby database

cancel;

口以只读方式打开物理备用数据库。

Sql>alter database open [read only]

打开前必须取消重做应用。激活物理备用数据库。

Sql> alter database activate standby database;
```





### 10.1 过程图

**![58](F:\github\oracle\test6\README.assets\clip_image050.jpg)

<img src=".\README.assets\clip_image050.jpg" />
<img src=".\README.assets\clip_image052.jpg" />
<img src=".\README.assets\clip_image054.jpg" />
<img src=".\README.assets\clip_image056.jpg" />
<img src=".\README.assets\clip_image058.jpg" />
<img src=".\README.assets\clip_image060.jpg" />
<img src=".\README.assets\clip_image062.jpg" />
<img src=".\README.assets\clip_image064.jpg" />
<img src=".\README.assets\clip_image066.jpg" />
<img src=".\README.assets\clip_image068.jpg" />
<img src=".\README.assets\clip_image070.jpg" />
<img src=".\README.assets\clip_image072.jpg" />
<img src=".\README.assets\clip_image074.jpg" />
<img src=".\README.assets\clip_image076.jpg" />
<img src=".\README.assets\clip_image078.jpg" />
<img src=".\README.assets\clip_image080.jpg" />
<img src=".\README.assets\clip_image082.jpg" />
<img src=".\README.assets\clip_image084.jpg" />

 

## 第11章 总结

通过此次数据库的课程设计，真正达到了学与用的结合，增强了对数据库方面应用的理解，对自己今后参与开发数据库系统积累了不少经验，在实验过程中，从建立数据开始，对灵据库设计理念及思想_上有更高的认识，从需求分析,到概念设计和逻辑设计，E-R图的表示，数据字典的创建，懂得了不少有关数据库开发过程中的知识，在实验中建表，及其关系模式，关系代数的建立及理解，将查询语句用得淋漓尽致，增强了自己在数据库中应用的灵活性，其中包括，插入、删除、修改、查询,牵涉表和表之间的联系，主建与外主键的定义，约束项的设置，使逻辑更严密，在学习过程中，我也能过上网查了不少资料，也看了一些别人设计的图书馆管理信息系统的设计报告,学以致用，自我创新，独立完成了这份自己的报告，从中在学到用，从用又到学，不断修改，系统更新。虽然不能达到完善系统，但也做到了尽善尽美，加强理论学习对完善系统会有很多帮助。

 