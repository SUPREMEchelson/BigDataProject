
# BigDataProject

![bigDataimage](https://user-images.githubusercontent.com/43779857/202323288-ec72d648-30ab-425e-b9b4-aadce2242500.jpg)

# Description

A l'approche de la coupe du monde qui se déroulera au Qatar, nous avons fait le choix d'analyser les données des matchs de football. Le Football est un sport collectif très populaire. La coupe du monde est un championnat qui réuni les plus grandes équipes du monde.
Le but du projet est de collecter et d'analyser des données footballistiques afin d'extraire des informations de performance. 

# Architecture

![SchemaProjetBigData](https://user-images.githubusercontent.com/43779857/202323405-14ed0ecb-ed66-4882-a7c9-b6fcfca8e287.jpg)

# Etat de développement
Le projet est en stade de développement.

# Technologie
Haddop
Spark
Docker

# Installation

récupérer le projet :
git clone https://github.com/SUPREMEchelson/BigDataProject.git

# Dockerisation de Hadoop et Spark

Nous avons configurer un Docker compose  qui contient les dependances de Hadoop et de Spark. Pour lancer le docker compose il faut utiliser cette commande :
Docker-compose up

# Traitement Spark

Lancer jupyter à l'aide du localhost 8080 
éxectuer les traitement du fichier project

# Dépôt dans Haddop

Ouvrer un cmd positionner vous dans le bon dossier

Executé le namenode :
docker exec -it namenode bash

Créer un dossier DataFoot dans le namenode
mkdir DataFoot

Ouvrir un autre cmd et positionner vous dans le dossier all_data afin de copier le fichierSource dans le namenode :
Docker cp fichierSource.csv 8a6837821a4f:/DataFoot (ceci est un exemple)

Retourner dans l'autre cmd créer un dépôt distant dans hadoop
hdfs dfs -mkdir /DataFootHadoop
Envoyer le fichier dans le dépôt créer
hdfs dfs -put fichierSource.csv /DataFootHadoop

# Traitement Spark

Ouvrez jupyter à l'aide du localhost:8888

Afin de faire les traitements depuis hadoop il faut spécifier le chemin

path="hdfs://namenode:9000/DataFootHadoop/fichierSource.csv" 

Nous pouvons traiter les données depuis hadoop avec spark

BallonDOr=spark.read.format("csv").options(header=True).load(path)

# Visualisation

La visualisation des données est faites avec l'application microsoft powerBi

# Auteur

Alain Fosso
Lucas Constant
Chelson Suprême

