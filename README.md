# mysql-server-container
Use mysql server as a container

+ start:
```
sudo docker-compose -d mysql-server-db
```
+ setup mysql:
```
sudo docker exec -it mysql-server-db mysql -uroot -p
```
+ ROOT password = "password"
+ USER = hooman
+ hooman password = "password"

+ bash inside the container:
```
sudo docker exec -it mysql-server-db /bin/bash

```
+ first login in mySql
```
mysql> ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';
mysql> GRANT ALL PRIVILEGES ON db.* TO 'hooman'@'%';
mysql>  FLUSH PRIVILEGES;
```

[reference](https://hub.docker.com/r/mysql/mysql-server/)
