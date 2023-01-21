# TP 3 Automatisation de tests - Lancez des tests avec docker

*GROUPE* : Vona, Osman, Aroutioun

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

## Explication de l'application

Nous avons crée ici une application avec l'utilisation de containers
créant plusieurs reports selon l'outil utilisé du code se
trouvant dans **python-api-handle-it** :

- Pylint
- Radon
- Robot
- Unit

Le dossier **Reports** se trouve dans **python-api-handle-it/app/**

## Description des serveurs
