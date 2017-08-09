# spring-mysql-liquibase

This repo demonstrates how you can setup a Spring boot app and use liquibase to manage deployment of code.

### Note on tactics with pre-existing databases

1. install liquibase cli.
2. download mysql jdbc drivers.
3. use the liquibase cli to generate a changelog which you can then embed in your project.

example:
```
liquibase --driver=com.mysql.jdbc.Driver
  --classpath=mysql-connector-java-5.1.43-bin.jar
  --changeLogFile=db.changelog.yaml
  --url="jdbc:mysql://localhost:3306/demo_database"
  --username=demo_database_user
  --password=password
  generateChangeLog
```
