À propos de MoneyMind : 

MoneyMind est une application web moderne de gestion financière personnelle développée avec Laravel. Elle permet aux utilisateurs de prendre le contrôle de leurs finances en suivant leurs revenus, dépenses, objectifs d'épargne mensuel et annuel, liste des souhaits d'achat futur. L'application automatise également toutes les transactions récurrentes que ce soit la déduction des dépenses ou la réception du revenu mensuel, ainsi qu'elle propose des conseils personnalisés grâce à l'intégration de l'IA Gemini pour une meilleure gestion budgétaire, avec aussi un système d'alertes (par envoi d'un rapport par email) et de notifications en temps réel et une liste d'historique de toutes les transactions.

Fonctionnalités principales : 

Pour les utilisateurs

Tableau de bord personnalisé : Vue d'ensemble de votre situation financière avec statistiques détaillées
Gestion des revenus : Configuration du salaire mensuel avec date de crédit automatique
Suivi des dépenses : Catégorisation et analyse des dépenses quotidiennes
Dépenses récurrentes : Automatisation des paiements réguliers (loyer, abonnements, etc.)
Objectifs d'épargne : Définition et suivi des objectifs financiers mensuels et annuels
Liste de souhaits : Planification des achats futurs avec suivi de progression
Alertes budgétaires : Envoi d'un rapport sur sa situation par mail lorsque les dépenses dépassent un seuil défini
Notification en temps réel : Envoi des notifications pour les alertes budgétaires, les réceptions des salaires et les déductions des dépenses mensuelles
Historique des transactions : Journal complet avec filtrage avancé (par mois, année, type de transaction)
Conseils IA : Recommandations personnalisées basées sur vos habitudes financières

Pour les administrateurs

Tableau de bord administratif : Statistiques globales sur les utilisateurs et leurs finances
Gestion des utilisateurs : Suivi et suppression des comptes inactifs depuis plus de 2 mois
Gestion des catégories : Création et modification des catégories de dépenses
Notifications système : Alertes sur les nouveaux utilisateurs et les comptes inactifs
Technologies utilisées
Backend : Laravel 11 (PHP 8.2.12)
Frontend : Blade, TailwindCSS, JavaScript
Base de données : MySQL
Authentification : Laravel Breeze
Visualisation de données : Chart.js
Animations : AOS (Animate On Scroll)

Prérequis

PHP 8.1 ou supérieur
Composer
Node.js et NPM
MySQL ou MariaDB
Serveur web (Apache, Nginx)
Installation
Clonez le dépôt

git clone https://github.com/Mo7amed-Boukab/MoneyMind.git
cd MoneyMind
Installez les dépendances

composer install
npm install
Configurez l'environnement

cp .env.example .env
Configurez la base de données dans le fichier .env

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=moneymind
DB_USERNAME=root
DB_PASSWORD=
Exécutez les migrations et les seeders

php artisan migrate --seed
Compilez les assets

npm run dev
Lancez le serveur

php artisan serve
Configuration des tâches planifiées
L'application utilise plusieurs tâches planifiées pour automatiser certaines fonctionnalités :

AddSalaire : Ajoute automatiquement le salaire mensuel aux dates définies par l'utilisateur
SubDepense : Déduit automatiquement les dépenses récurrentes
AlertBudget : Envoie des alertes lorsque les dépenses dépassent un certain seuil
CheckInactiveUsers : Vérifie les utilisateurs inactifs depuis plus de 2 mois
Pour configurer ces tâches, exécutez la commande suivante :

php artisan schedule:work
