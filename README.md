# onlinenotes
Project for online note taking and sharing

In order to properly set up MySQL database following steps have to be done (docker installation is a prerequisite):

```
docker pull mysql
```
This allows to pull the most recent docker image that has a functioning MySQL database to connect to.

```
docker run --name onlinenotes-mysql -e MYSQL_ROOT_PASSWORD=root -d -p 3306:3306 mysql
```
Following command does the following:
- "name" is the name of our docker container that will have our database
- "-e" is setting a password needed for connecting to a database. It is hardcoded into this project, as this is not hosted online as of now.
- "-d" means that the container is ran in detached mode
- "-p" sets which port of a container is connected to a port on a host machine

When these steps are done with not obvious errors, User has to connect to a MySQL instance in a docker container with a tool such as MySQL Workbench.
Then, the schema and a table has to be created with these parameters:
- NOT YET IMPLEMENTED

Also, for people which are not familiar with maven, these command will be necessary in order to run the program:

```
mvn clean install
```
and 
```
mvn spring-boot:run
```

After all of this, the application should be functional and is modifiable as You wish.