# SQL_homework


 drop database if exists school;
 create database school;
 use school;
 
  -- table student
  
 create table student(
 fname varchar(10),
 lname varchar(20),
 address varchar(20),
 sex char(1),
 am integer,
 primary key(am)
 );
 
 -- table lessons
 
 create table lessons(
 lesson_name varchar(10),
 hours integer,
 id integer,
 primary key(id));
 
 -- table attends
 
 create table attends(
 am integer,
 id integer,
 primary key(am,id),
 constraint foreign key (am) references student(am),
 constraint foreign key (id) references lessons(id));
 
 -- table student_phones
 
 create table student_phones(
 number integer,
 am integer,
 primary key(number, am),
 constraint foreign key (am) references student(am));
 
 insert into student values('Xrusa','Alexandraki','Kalokerinou 7','F',1);
 insert into student values('Maria','Ale','Xeimerinou 7','F',2);

 
 select * from student;
 
 insert into lessons values('Baseis',2,1);
 
 select * from lessons;
 
 insert into student_phones values(230,1);
 
select * from student_phones;
