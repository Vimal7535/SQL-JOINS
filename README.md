# SQL-JOINS


create database person go ------------------------------------------first table-------------------- create table tblEmploye(ID int primary key not null , Name varchar(50)not null , Gender varchar(20)not null,salary money not null,Departmentid int) insert into tblEmploye(ID,Name,Gender,salary ,Departmentid) values (1,'tom','m',20000,1), (2,'rom','m',2020,3), (3,'mohan','m',4504,1), (4,'love','m',75575,2), (5,'she','f',40000,2), (6,'aalu','m',5000,1), (7,'king','m',8802,3), (8,'queen','f',8500,1), (9,'reena','f',4500,null), (10,'singh','m',5500,null)

--------------------------------------second table-------------------------------

create table tblDepartment(id int not null,Departmentname varchar(20),location varchar(30),DepartmentHead varchar(50)) insert into tblDepartment(id,Departmentname,location,DepartmentHead) values (1,'IT','Londan','delhi'), (2,'Payroll','Uerop','Mumbai'), (3,'IT','Barlin','canada'), (4,'IT','Pak','Nioda')

select * from tblDepartment select * from tblEmploye

update tblDepartment set Departmentname = 'HR' where id=3 update tblDepartment set Departmentname='Other department' where id=4

------------------------------------Begain the joins performance----------------------------

-----------------------inner join----------------------------------

select * from tblEmploye join tblDepartment on tblEmploye.Departmentid = tblDepartment.id

---------------------------------left join-------------------------------

select * from tblEmploye left join tblDepartment on tblEmploye.Departmentid = tblDepartment.id

-------------------------------right join-----------------------------------

select * from tblEmploye right join tblDepartment on tblEmploye.Departmentid = tblDepartment.id

--------------------------full join--------------------------

select * from tblEmploye full join tblDepartment on tblEmploye.Departmentid = tblDepartment.id

------------------------------------cross join--------------------------------------

select * from tblEmploye cross join tblDepartment
