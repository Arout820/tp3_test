# TP 3 Automatisation de tests - Lancez des tests avec docker

**GROUPE** : Vona, Osman, Aroutioun

Merci à Vona!

## Explication du dossier principal

A la racine se trouve le dossier **TP3** et à l'intérieur nous avons 5 dossiers et 1 fichier docker
compose :

- python-api-handle-it
- Pylint
- Radon
- Robot
- Selenium
- Unit
- **docker-compose.yml**

Il y a un **Dockerfile** dans chaque dossier ainsi qu'un fichier **requirements.txt** permettant
d'installer les paquets nécessaires dans leurs containers respectifs.

## Le fichier docker compose

Ce fichier permet de build et de relier toutes les images configurées de chacuns des dossiers et de les mettre dans le même réseau :

```bash
  docker compose up -d --build
```

Chacuns des services possèdent une ligne **"command"** permettant de lancer directement les commandes lors du build, et une ligne
**"working_dir"** ce qui permet de reçevoir tous les fichiers reports dans un dossier prédéfini.

On peut également lancer une commande qui permet de refaire les fichiers tests en startant les containers de nouveau :

```bash
  docker start -i "id_du_container_stoppé"
```

## Docker Hub

Sur le lien du dépôt dockerhub se trouve les images permettant de créer les containers:

https://hub.docker.com/repositories/caracruz

## Explication de l'application

Nous avons crée ici une application avec l'utilisation de containers
créant plusieurs reports (selon l'outil utilisé) du code se
trouvant dans **python-api-handle-it** :

- Pylint
- Radon
- Robot
- Unit

Le dossier **Reports** se trouve dans **python-api-handle-it/app/**

## Description des serveurs

Plusieurs containers tournent et chacun permet à sa façon de récupérer des données de qualité et ou de test du code.
