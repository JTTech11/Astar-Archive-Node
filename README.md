# Astar Archive Node
## How to create an Archive Node with Docker compose.yml

### Archive Node storage

```
sudo mkdir /var/lib/astar
sudo useradd --no-create-home --shell /usr/sbin/nologin astar
sudo chown astar:astar /var/lib/astar
```
### File structure for Archive Node container
```
/srv/astar
├── compose.yml
├── .env
```
```
mkdir /srv/astar
sudo chown $USER:$USER /srv/astar
cd /srv/astar
```

Edit .env and compose.yml files\
Rename node in .env

### Create a Docker network for Astar
`docker network create astar`

### Some basic docker commands
check compose.yml for any errors\
`docker compose config`\
If everything looks good, start Astar container\
`docker compose up -d`\
check logs\
`docker logs -f --tail 50 -t astar-container`
