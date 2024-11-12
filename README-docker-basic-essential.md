## Build Project with Docker
Purpose use docker when i want when delete container data stored in folder volumes

Use docker volume
```bash
docker run -v "$(pwd)":/app --workdir="/app" maven:3.9.9-eclipse-temurin-8-alpine mvn install -DskipTests=true
```

Running a MariaDB Database with Docker
``` bash
docker run -v /db/mariadb-1/:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root -p 3307:3306 --name mariadb-1 -d mariadb:10.6
```
connect to mysql server 
```bash
mysql -h 192.168.102.133 -P 3307 -u root -p
```

interactive to shoeshop
```bash
docker exec -it shoeshop-1 sh
```
inspect and check network
```bash
docker inspect mariadb-1
```