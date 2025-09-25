>  ### Ubuntu - Debian
{.is-info}


## Mise à jour de l'OS
```
sudo apt -q update && sudo apt upgrade -y
```

## Installation de GO 


`wget https://go.dev/dl/go1.20.14.linux-amd64.tar.gz`
`sudo tar -xvf go1.20.14.linux-amd64.tar.gz `
`sudo mv go /usr/local`
`sudo rm go1.20.14.linux-amd64.tar.gz`
`sudo nano ~/.bashrc`

**Ajoutez** :
    GOROOT=/usr/local/go
    GOPATH=$HOME/go
    PATH=$GOPATH/bin:$GOROOT/bin:$PATH*
    
## Installation de GlibC

```
echo "deb http://cz.archive.ubuntu.com/ubuntu jammy main" >> /etc/apt/sources.list
apt update
sudo apt install libc6
```

## Vérifier les port d'écoute
```
ss -napult
```

## Changer le hostname de la machine

```
sudo nano /etc/hostname
sudo nano /etc/hosts
sudo reboot
```

## Commandes screen
```
pkill screen    # pour fermer tout les screens actifs
screen - ls     # pour lister les screens
```

## Editer service

```
sudo nano /lib/systemd/system/nom_du_service.service
sudo nano /etc/systemd/system/nom_du_service.service

sudo systemctl daemon-reload
sudo systemctl restart nom_du_service
```


## Installation de Docker

```
#Add Docker's official GPG key:

sudo apt-get update && sudo apt upgrade -y
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

#Add the repository to Apt sources:

echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \ $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \ sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Test docker installation
sudo docker run hello-world

```
