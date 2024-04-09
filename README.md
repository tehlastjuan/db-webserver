# The Docker Container Series:
### apache webserver + mariaDB + phpmyadmin -> SQL in a bottle
#### Install
```
// install Docker + Docker Compose
$ sudo apt docker docker-compose
$ sudo pacman -S docker docker-compose

// enable docker daemon in systemd
$ systemctl enable docker.service

// add user to docker user group and log out
$ sudo usermod -aG docker $USER

// build docker containers and volumes
$ docker compose up
```
#### Run
```
// run in the background
$ docker compose up -d

// stop docker background process
docker compose down

// web access
Browser -> http://localhost:8000 -> html front end
Browser -> http://localhost:8081 -> phpmyadmin front end
```

#### Command line
```
# access the shell in mariadb docker container
$ docker-compose exec mariadb bash

# run mariadb
$ mariadb --user=username --password=userpasswd

# print available databases
MariaDB[(none)]> show databases;

# select and use database
MariaDB[(none)]> use databasename;

# show DB tables (relations)
MariaDB[(databasename)]> show tables;

# Start writing SQL queries in the confort of the command line!
```

[guide](https://thriveread.com/apache-php-with-docker-mysql-and-phpmyadmin/) - 
[docker compose docs](https://docs.docker.com/compose/) - 
[archwiki docker page](https://wiki.archlinux.org/title/Docker) (good info)

[SQL Cheat sheet 1](https://learnsql.com/blog/sql-basics-cheat-sheet/sql-basics-cheat-sheet-a4-page-1.png) - 
[SQL Cheat sheet 2](https://learnsql.com/blog/sql-basics-cheat-sheet/sql-basics-cheat-sheet-a4-page-2.png)

Under GNU General Public License v3.0
