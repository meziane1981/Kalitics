# Kalitics
Exercice de développement Symfony4Exercice de développement Symfony 4
## Table des matières
<!-- * [Informations générales](#informations-générales) -->
* [Technologies](#technologies)
* [Installation](#installation)
* [Démarrage](#démarrage)
* [Versions](#versions)
* [Auteur](#auteur)
## Technologies
Symfony 4.4.43
php 8.1.0

## Instalation 
* Versions de Symfony LTS 
1. par la commande 
```
symfony new --full Kalitics --version=4.4
```
2. Installer toutes les dépendances composer du projet : 
```
composer install
```
## paramétrage de la base de données
1. Les informations de connexion s'inscrivent dans le fichier .env situé à la racine du projet Voici la ligne de ce fichier qui correspond à cette connexion
```
DATABASE_URL="mysql://db_user:db_password@127.0.0.1:3306/db_name?serverVersion=5.7&charset=utf8mb4""
DATABASE_URL="mysql://root:@127.0.0.1:3306/kalitics"
```
2. Après avoir mis à jour le fichier .env, nous procédons à la création de la base de données en entrant la commande suivante
```
php bin/console doctrine:database:create
```

## Création des tables
1. Création de l'entité
       - Pour créer une entité, nous exécutons la commande suivante :
```
php bin/console make:entity
```