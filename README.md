# DB-03

## 1.
create database MyGame

use MyGame

## 2.
create table users (
	userId int primary key,
	userName varchar(25),
	age int
)

## 3.
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


create database JavierCar

use JavierCar

drop table clientes
create table clientes (
	idCliente int unique auto_increment primary key,
	cedula int unique not null,
	nombre varchar(50),
	telefono int,
	direccion varchar(100)
	
)
drop table carros
create table carros (
	idCarro int primary key auto_increment,	
	marca varchar(50),
	modelo varchar(50),
	matricula varchar(50),
	ano date
)

drop table renta
create table renta (
	idRenta int primary key auto_increment,
	idCarroRenta int not null,
	idClienteRenta int not null,
	inicioAlquiler date not null,
	finAlquiler date not null,
	precioAlquiler int not null,
	foreign key (idCarroRenta) references carros(idCarro),
	foreign key (idClienteRenta) references clientes(idCliente)
)


insert into clientes (cedula, nombre, telefono, direccion) 
values ( 44660747, "Javier Peralta", 8474620, "Calle Primera, Sara Grabriela")

insert into clientes (cedula, nombre, telefono, direccion) 
values ( 40414747, "Ana Guzman", 809474620, "Calle Luna, Villa Mella"),
( 40214247, "Luis Perez", 809474620, "Calle Sol, Villa Mella")


select * from clientes

insert into carros (marca, modelo, matricula, ano) values ("Ferrari", "SF-99", "T00F4ST", "2024-02-10")

insert into carros (marca, modelo, matricula, ano) values
("McClaren", "Rocket", "JF3134", "2022-08-12"),
("Bugatti", "Spider", "SP33D", "2020-06-12")

select * from CARROS

insert into renta (idCarroRenta , idClienteRenta ,inicioAlquiler, finAlquiler, precioAlquiler) 
values (3, 3, "2023-01-10", "2023-02-02", 12000 )

insert into renta (idCarroRenta , idClienteRenta ,inicioAlquiler, finAlquiler, precioAlquiler) 
values (1, 1, "2023-01-12", "2023-03-02", 10000 ),
(3, 4, "2023-02-11", "2023-04-10", 14000 )


select  * from renta 	



