
![bigDataimage](https://user-images.githubusercontent.com/43779857/202323288-ec72d648-30ab-425e-b9b4-aadce2242500.jpg)

# Description

A l'approche de la coupe du monde qui se déroulera au Qatar, nous avons fait le choix d'analyser les données des matchs de football. Le Football est un sport collectif très populaire. La coupe du monde est un championnat qui réuni les plus grandes équipes du monde.
Le but du projet est de collecter et d'analyser des données footballistiques afin d'extraire des informations de performance. 

# Etat de développement
Le projet est en stade de développement.

# Technologie
Haddop
Spark
Docker

# Installation

récupérer le projet :
git clone git@github.com:mehdisellami/Helpme-Backend.git

# Lancement des Docker

Docker-compose up


# Traitement Spark

Lancer jupyter à l'aide du localhost 8080 
éxectuer les traitement du fichier project

# Dépôt dans Haddop

Ouvrer un cmd positionner vous dans le bon dossier

Lancer les dockers :
Docker-compose up

Executé le namenode :
docker exec -it namenode bash

Créer un dossier DataFoot dans le namenode
mkdir DataFoot

Ouvrir un autre cmd et positionner vous dans le dossier all_data afin de copier le fichierSource dans le namenode :
Docker cp fichierSource.csv 8a6837821a4f:/DataFoot

Retourner dans l'autre cmd créer un dépôt distant dans hadoop
hdfs dfs -mkdir /DataFootHadoop
Envoyer le fichier dans le dépôt créer
hdfs dfs -put fichierSource.csv /DataFootHadoop












# Auteur

Alain Fosso
Lucas Constant
Chelson Suprême

