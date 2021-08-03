# product

This is a complete stack for running Symfony 5 into Docker containers using docker-compose tool.

It is composed by 3 containers:

nginx, acting as the webserver.
php, the PHP-FPM container with the 7.4 PHPversion.
db which is the MySQL database container with a MySQL 8.0 image.
Installation
😀 Clone this rep.

Run `docker-compose --env-file "./.env" up -d --build`

The 3 containers are deployed:

Starting mysql       ... done
Creating php_symfony ... done
Creating nginx       ... done
Use this value for the DATABASE_URL environment variable of Symfony:
`DATABASE_URL=mysql://root:root@db:3306/app_db?serverVersion=5.7`

Case the database wasn't create then execute this command: `php bin/console doctrine:database:create` after `php bin/console doctrine:migrations:migrate`
You could change the name, user and password of the database in the env file at the root of the project.


Now you can open your browser http://localhost/tag or http://localhost/product
