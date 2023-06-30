# DarkVege

## Étape 0 : "kékésé cette app"

DarkVege est une petite web app vous permettant de choisir vos favoris parmi 6 légumes révolutionnaires. Bon 6 légumes quoi :D

Une base de code express _fonctionnelle_ est fournie.
Par contre, on a que les images du livrable pour voir le résultat attendu. Le code lui, il est en mode foetus. Il faut le prendre en compte.

Les vues EJS / les pages, tout cela est déjà implémenté. Libre à vous de customiser à votre goût (création d'une page 404 par exemple ?).

## Étape 1 : Mise en place

Utiliser npm pour:
- Initialiser le projet.
- Installer les dépendances nécessaires : `express`, `ejs`, `pg`, et `dotenv` et `express-session`. Un simple `npm i` fera l'affaire (voir le package.json). Attention au script de démarrage dans le package.json.

## Étape 2 :  C'est parti pour la base de données

- On crée une base de données en local sur sa machine ; pour cela on crée un user, un password, une DB... enfin bref. Tout est sur Kourou :  [Cette fiche récap](https://kourou.oclock.io/ressources/fiche-recap/postgresql/) peut être utile :wink:. 

- Ensuite, on populate cette database avec le fichier `.sql` fourni (même fiche Kourou) :) 

## Étape 3 :  Allez, on gère les fonctionnalitées unes à unes

1) Dynamisation des vues `ejs` en prenant en compte les données 
2) Ajout de vegetable aux favoris (sessions)
3) Suppression de vegetable des favoris (sessions)

> Attention : il faut éviter la répétition de code et rester DRY. Par exemple, gérer les sessions vides au lancement de l'application par un middleware.   

<br/>
4) BONUS N°1 >> On ajoute le bouton de suppression des favoris d'une carte de vegetable non seulement sur la page favoris, mais aussi sur la page d'accueil. Chaque carte, si elle est dans les favoris, doit pouvoir être supprimée également depuis la page d'accueil. Le tout en étant DRY :)

<br/>
5) BONUS N°2 >> La suppression d'une carte des favoris depuis la page d'accueil, doit rediriger vers la page d'accueil. La suppression d'une carte des favoris depuis la page favoris, doit rediriger vers la page des favoris. Autrement dit, en une seule route de suppression de type `/favoris/delete/:id`, la redirection doit être dynamique selon de quelle page nous venons... TMTC : stay DRY.

<br/>
6) BONUS N°3 >> Sur la page des favoris, on ajoute une fonctionnalité des trie des cartes par ordre de prix croissant ou décroissant. Le tout si possible avec une seule route et un seul controller qui gère les deux liens (Yes we DRY). 