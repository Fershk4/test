# test
Para hacer cualquier cosa que necesite testear

## Despliegue de Bahmni

El primer paso que se debe hacer es preparar tu sistema para el despligue de Bahmni, esto se hace como indica la rama principal del repositorio Bahmni SIMSADI https://github.com/Mitridato/BAHMNI-SIMSADI/tree/main?tab=readme-ov-file.


Para desplegar Bahmni estandar o lite se deben seguir los pasos de la rama backup del repositorio Bahmni SIMSADI, esta a su vez sigue los pasos del Wiki Bahmni en 
https://bahmni.atlassian.net/wiki/spaces/BAH/pages/3117744129/Getting+Started+Quickly+with+Bahmni+on+Docker#Running-Bahmni-Standard.


```
oli
```

## En caso de error quita los contenedores y vuelve a subir

quita docker
```
sudo apt-get purge -y docker-ce docker-ce-cli containerd.io
sudo apt-get autoremove -y --purge
sudo dnf remove -y docker-ce docker-ce-cli containerd.io
sudo dnf autoremove -y

sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
sudo rm -rf /etc/docker

sudo rm -rf /var/run/docker.sock
sudo rm -rf ~/.docker

sudo groupdel docker

sudo rm -rf /usr/local/bin/docker*

```
eliminar contenedores
```
docker-compose down --volumes --rmi all
docker volume prune -f
docker network prune -f
```
quita portainer y carpeta
```
docker stop portainer
docker rm portainer
rm -r snowstorm-10.3.1/
```

