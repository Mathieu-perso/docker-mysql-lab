# Docker - MySql Lab

## Mathieu Boulot - M2 Connect

### 1. Structure du projet

1. .env : _Regroupe toutes les variables d'environnement._
2. Dockerfile : _Utilise l'image mysql 8, copie le fichier init.sql et expose le port 3306._
3. init.sql : _Crée une table formations et ajoute une table users._

### 2. Étapes

1. Docker build -t mysql-lab . : _Build l'image mysql_
2. Docker run -d --name mysql-lab-container --env-file .env mysql-lab : _Lance le conteneur en utilisant l'image mysql-lab et les variables d'environemment du fichier spécifié (.env)_
3. Docker ps : _Affiche la liste des conteneurs actifs_

### 3. "Purger" conteneurs et images

1. Docker stop mysql-lab-container : _Arrête le conteneur spécifié_
2. Docker rm mysql-lab-container : _Supprime le conteneur spécifié_
3. Docker rmi mysql-lab : _Supprime l'image spécifiée_

### 4. Vérifications à faire

1. S'assurer qu'il n'y a aucune erreur de syntaxe dans le(s) fichier(s) sql.
2. S'assurer que les variables utiles sont bien définies dans le .env et que le fichier est utilisé pour le lancement du conteneur.
3. S'assurer qu'on a bien exposé un port pour nos images.
