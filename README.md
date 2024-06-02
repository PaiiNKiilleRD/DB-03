# DB-03



## create database MyGame

use MyGame
create table users (
	userId int primary key,
	userName varchar(25),
	age int
)

create table users2 (
	userId int primary key auto_increment,
	userName varchar(25),
	age int
)

create table userInfo (
	firstName varchar(25),
	lastName varchar(25),
	userInfoKey int,
	foreign key (userInfoKey) references users(userId)
)
