数据库三大数据类型: 1. 字符串 2. 数字 3. 时间

创建表格时,必须先写字段名和字段数据类型,后面的约束无顺序要求

数据库引擎决定了数据结构

增添字段时 最好设置一个默认值

模糊查询和正则查询 (针对字符串)

datatime 和 timestamp 表现形式相同 但是消耗的空间是不一样的 因为储存格式不同

在mysql中 字符串,数字和时间 均可排序.

子查询及联合查询, 都可以同时查不同表中的数据

常用高级查询语句:
  as / order by / union

where 子句当中无法直接使用聚合函数,
having 子句通常使用聚合函数进行筛选

聚合函数的重点: 分组

mysql使用的是B+树的索引结构(书籍:<<算法导论>>)

面试的挑战: 如何理清表之间关系,进而正确建表. 
		(通过正确添加字段的联系,建立合理的表关系能节省空间,增加信息存储量,并防止数据冗余)

foreign key 会影响查询效率, 只有在必要的时候才会建立这种约束. foreign key(外键)是在从表中建立
并不是有表关联就一定要创建外界约束, 要视情形而定.

一对多的情况下,一叫主表,多叫从表

多对多的情况下, 用复合主键非常合适, 因为两个主键不可能同时重复.	



create table 3_Kingdoms (id int primary key auto_increment, name varchar(6) not null, gender enum('f','m') not null, country char(2), attack smallint, defence tinyint);

insert into 3_kingdoms values (1, '曹操', 'm', '魏',105,80)



cookie:
	文件存储数据库方法?
	
	方法一: 存路径
		
		eg: 小泽图片	"/home/tarena/老师们/小泽/xxx.jpg"

		优点: 节省数据库空间,提取使用方便
		缺点: 一旦路径移动,数据库就要修改
	
	方法二: 存文件本身

		优点: 数据库在,文件就在
		缺点: 占数据库空间大,读写效率低





























