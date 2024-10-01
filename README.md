# Objectif : Exécuter une requête asynchrone  ajax à un serveur web #
L'environnement de travail est constitué :
-De plusieurs dossiers contenant des fichiers index.html et script.js.
-D'un conteneur nginx  possédant une image à exécuter pour pouvoir exécuter les fichiers dans un environnement sur le serveur.

## 1) Cloner le répot 
Vous devez cloner ce répot dans un système d'exploitation  ubuntu (par vmware ou via un invité de commande avec wsl sur windows) en utilisant la commande suivante :
```bash
git clone https://github.com/atifiAmine/ajax-amine-.git
```
## 2) Installer docker et docker-compose avec les commandes suivantes (si vous ne les possédez pas dans votre machine) :
-Veillez à bien mettre à jour les paquets :
```bash
sudo apt update 
```
-Commande pour installer docker 
 ```bash
sudo apt install docker.io
```
-Commandes pour installer docker-compose 

On télécharge docker-compose :
```bash
curl -L “https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
On change les autorisations : 
```bash
chmod +x /usr/local/bin/docker-compose
```
On crée un lien symbolique
```bash
ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```
On vérifie 
```bash
docker-compose -v
```

## 2) Exécuter le conteneur nginx : 
On exécute le conteneur avec la commande suivante :
```bash
sudo docker run --name my-nginx -p 8092:80 -v $(pwd)/app1:/usr/share/nginx/html -d mtobji/custom-ngin
```
## On vérifie en tapant l'url sur un navigateur web
L'url sera différente en fonction de l'activité. 


