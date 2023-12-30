# servlet-app



To run this application you must

1. Make a Fork of this project (priority) or clone repository

```bash
git clone https://github.com/OKaluzny/servletApp.git
```

2. Build this application using maven 

```bash
mvn clean install -Dmaven.plugin.validation=VERBOSE
```
3. Download and install WildFly https://www.wildfly.org/. Запустить WildFly. Go to the /bin directory and call standalone.bat
   then deploy the application using the command

```bash
mvn org.wildfly.plugins:wildfly-maven-plugin:2.0.2.Final:deploy
```
4. Download and install the Postman request client
   
5. Download and install DBMS PostgreSQL, create DB - Employee
```bash

DROP DATABASE Employee;

CREATE DATABASE Employee;

USE Employee;
CREATE TABLE if not exists public.users
(
    id      serial 
            primary key,
    name    varchar(255),
    email   varchar(255),
    country varchar(255)
);
```
