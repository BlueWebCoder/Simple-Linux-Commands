>  ### Ubuntu - Debian
{.is-info}


## Mise à jour de l'OS
```
sudo apt update && sudo apt upgrade
```

    
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


## Utilisation  de Docker
```
# Reset docker
docker system prune -a
```
