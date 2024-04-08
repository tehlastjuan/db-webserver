## Webserver + mariaDB + phpmyadmin SQL in a docker container
### Install
```
// (UBUNTU) install Docker + Docker Compose
$ sudo apt-get update & sudo apt-get upgrade
$ sudo apt docker docker-compose

// enable docker daemon in systemd
$ systemctl enable docker.service

// add user to docker user group
$ sudo usermod -aG docker $USER

// copy contents in a folder outside the repo & log out

// build docker container and volumes
$ cd <folder-name>
$ docker compose up
```
### Run
```
// run in the background
$ docker compose up -d

// stop background docker process
docker compose down

Browser -> http://localhost:8000 -> html front end
Browser -> http://localhost:8081 -> phpmyadmin front end
```

### Command line
##### Wwrite SQL queries in the command line
```
# shell in mariadb docker container
$ docker-compose exec mariadb bash

# start mariadb process
$ mariadb --user=username --password=userpasswd

# print available databases
MariaDB[(none)]> show databases;

# select and use database
MariaDB[(none)]> use databasename;

# show DB tables (relations)
MariaDB[(databasename)]> show tables;
```

[guide](https://thriveread.com/apache-php-with-docker-mysql-and-phpmyadmin/) - 
[docs](https://docs.docker.com/compose/) - 
[archwiki docker page](https://wiki.archlinux.org/title/Docker) (good info)

[SQL Cheat sheet 1](https://learnsql.com/blog/sql-basics-cheat-sheet/sql-basics-cheat-sheet-a4-page-1.png) - 
[SQL Cheat sheet 2](https://learnsql.com/blog/sql-basics-cheat-sheet/sql-basics-cheat-sheet-a4-page-2.png)

Under GNU General Public License v3.0
