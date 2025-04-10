# mario
This is for testing purpose....

## Set up EC2-machine
```bash
#user-data
sudo apt-get update
sudo apt install git -y

git config --global credential.helper cache

# Install Docker
sudo apt-get update
sudo apt install docker.io -y

sudo usermod -aG docker $USER
sudo newgrp docker

# Mario part
docker pull sevenajay/mario
docker run -it --rm -p 80:80 sevenajay/mario
# Access via EC2-public IP or DNS
```
