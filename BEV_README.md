# prerequisites for windows
* enter Windows-Features in your search bar 
* select Windows-Subsystem für Linux
* Open the microsoft store
* search for linux
* install Ubuntu
```bash
sudo apt install make
sudo apt install git
```
* docker <https://hub.docker.com/editions/community/docker-ce-desktop-windows>

# git
```bash
git clone https://github.com/codirk/TYPO3-docker-boilerplate.git
cd TYPO3-docker-boilerplate
```

# prepare docker and run
```bash
make create typo3
make up
```

# open 
Open <http://localhost:8000> and follow installation wizard.


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
