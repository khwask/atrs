# Airline Ticket Reservation System (ATRS)

This is a reference application for developers to learn how to build applications with Macchinetta Framework.

## How to run the application

### Download source code

Download source code from [here](https://github.com/Macchinetta/atrs/releases "here").
Extract the zip file at any location of choice.

### Install PostgreSQL

Install and start PostgreSQL.
Select 'postgres' as password for postgres user.
If you'd like to use other password, some changes will be required in setting files.

### Insert test data

First of all, create database named 'atrs'.

After that, execute the command below at the directory where the downloaded source code is unzipped.

```console
$ mvn -f atrs-initdb/pom.xml sql:execute
```

It is assumed that maven is already installed.
If not, install it and try again.

### Install Tomcat

Install Tomcat.

### Build applicatoin

Execute the command below at the directory where the downloaded source code is unzipped.

```console
$ mvn -f atrs-parent/pom.xml clean install
$ mvn -f atrs-env/pom.xml clean install
$ mvn -f atrs-domain/pom.xml clean install
$ mvn -f atrs-web/pom.xml clean install
```

Deploy 'atrs-web/target/atrs.war' to tomcat and access [http://localhost:8080/atrs].

## Front-end refactoring

### npm
 
```console
$ cd atrs-web
$ npm init
$ npm install --save-dev webpack
$ npm install bootstrap@3.2.0
$ npm install bootstrap-datepicker@1.7.1
$ npm install jquery@1.11.1
$ npm install tablesorter@2.29.2
$ npm install lodash@2.4.1
$ npm install moment@2.8.3
$ npm install parsleyjs@2.0.6
```

