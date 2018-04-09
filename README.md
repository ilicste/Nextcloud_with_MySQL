# Nextcloud_with_MySQL setup
Run Docker and create a new container with MySQL DB with the name "db" username "admin" and the password "admin123"
```
docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d -e MYSQL_DATABASE=db -e MYSQL_USER=admin -e MYSQL_PASSWORD=admin123 mysql
```
Create a new container with Nextcloud and connect to the created MySQL DB
```
docker run -d -p 8080:80 -e MYSQL_DATABASE=db -e MYSQL_USER=admin -e MYSQL_PASSWORD=admin123 --link some-mysql:mysql nextcloud
Create a new container with Nextcloud and connect to the created MySQL DB
```
