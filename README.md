---MYSQL SETUP---
"You just need to have docker installed and run the following commands below in order to set up the MYSQL DB
may need to wait a couple of minutes for the database to be created and docker to install mysql 
as well as giving the create database command time as well to finish completeing before moving onto next steps"



docker container run -d --name mysqldb -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password mysql:latest

docker exec -it mysqldb bash

mysql -u root -ppassword

create database altr;

use altr;

CREATE TABLE persons (id int NOT NULL AUTO_INCREMENT, last_name varchar(60) NOT NULL, first_name varchar(60) NOT NULL, PRIMARY KEY (id));

INSERT INTO persons (first_name,last_name) Values ("Steven","Cheswick");
INSERT INTO persons (first_name,last_name) Values ("John","Smith");
INSERT INTO persons (first_name,last_name) Values ("Jack","Brown");
INSERT INTO persons (first_name,last_name) Values ("Tyler","Jones");
INSERT INTO persons (first_name,last_name) Values ("Mike","Strat");
INSERT INTO persons (first_name,last_name) Values ("Austin","Washington");
INSERT INTO persons (first_name,last_name) Values ("Hunter","Placks");
INSERT INTO persons (first_name,last_name) Values ("Chance","Thomas");
INSERT INTO persons (first_name,last_name) Values ("Mark","Ruffalo");
INSERT INTO persons (first_name,last_name) Values ("Scooby","Doo");
INSERT INTO persons (first_name,last_name) Values ("Shaggy","Doo");
INSERT INTO persons (first_name,last_name) Values ("Fred","Flinstone");

select * from persons;

---Future Additions---
I would have liked to use MockMVC and Mockito frameworks to use Mock Objects simulate the behaviour of the real objects,
however I ran into maven and Springboot issues setting up the dependencies and was not able to get the frameworks
into my project.
