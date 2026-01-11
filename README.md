# Astar-Archive-Node
How to create an Archive Node with Docker compose.yml

# Astar Archive Node storage
sudo mkdir /var/lib/astar
sudo useradd --no-create-home --shell /usr/sbin/nologin astar
sudo chown astar:astar /var/lib/astar

# File structure for Archive Node container
/srv/astar
├── compose.yml
├── .env

mkdir /srv/astar
sudo chown $USER:$USER /srv/astar
cd /srv/astar

# Create .env file
# Create compose.yml file

# Create a Docker network for Astar
docker network create astar

# check config
docker compose config
# If everything is good, start Astar container
docker compose up -d
# check logs
docker logs -f --tail 50 -t astar-container
