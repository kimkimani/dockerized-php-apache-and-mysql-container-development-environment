# dockerized-php-apache-and-mysql-container-development-environment
PHP Websites using Docker Containers with PHP Apache and MySQL

Run `docker-compose up` to download the Apache server, build the image, and run the container.

Open http://localhost:8080/ on the browser to access the PHPMyAdmin.

To login to the Phpmyadmin panel, use username as `root` and password as `MYSQL_ROOT_PASSWORD`. The password was already set in the MySQL environment variables (MYSQL_ROOT_PASSWORD: MYSQL_ROOT_PASSWORD)

Select `MYSQL_DATABASE` database and execute the following query.

```sql
drop table if exists `users`;
create table `users` (
    id int not null auto_increment,
    username text not null,
    password text not null,
    primary key (id)
);
insert into `users` (username, password) values
    ("admin","password"),
    ("Alice","this is my password"),
    ("Job","12345678");
```

Open  http://localhost:8000/ to view the results.

We have only used the Read operation to demonstrate this. Go ahead and try other CRUD operations with the dockerized PHP application.

Check the step by step guide [here](https://www.section.io/engineering-education/dockerized-php-apache-and-mysql-container-development-environment/)
