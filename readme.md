Construire l'image Docker :

`docker build -t my-mariadb-image .`

Lancer le conteneur Docker :

`docker run --rm --name=my-mariadb --detach --publish 3306:3306 my-mariadb-image`

# Ouvrir une session shell dans le conteneur
docker exec -it my-mariadb bash

# Une fois dans le conteneur, accéder au client MariaDB
mariadb -u root -p

# Entrer le mot de passe root (dans ce cas "password")
Enter password: password

# Lister les bases de données
SHOW DATABASES;