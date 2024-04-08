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

[guide](https://thriveread.com/apache-php-with-docker-mysql-and-phpmyadmin/) - 
[docs](https://docs.docker.com/compose/) - 
[archwiki docker page](https://wiki.archlinux.org/title/Docker) (good info)
