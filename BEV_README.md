# prerequisites
* docker <https://hub.docker.com/editions/community/docker-ce-desktop-windows>
* make
* git <https://git-scm.com/downloads>

# git
```bash
git clone https://github.com/codirk/TYPO3-docker-boilerplate.git
cd TYPO3-docker-boilerplate
git checkout bev
```

# prepare docker and run
```bash
cp docker-compose.development.yml docker-compose.yml
make create typo3
make up
```

# open 
Open <http://localhost:8000> and follow installation wizard.
Open <http://localhost:8001> for phpmyadmin.


## step 1: Select database

* User= dev 
* Password= dev
* Host= mysql
* Port= 3306

## step 2: Select database
* Use an existing empty database: typo3

## step 3: Select database
* Username: admin
* Password: admin1234 (changeit)

# back to start
```bash
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
docker volume rm $(docker volume ls -q)
```
