## Problématique

Cherchez un programme qui ne manipule ni ne stocke de données... difficile de trouver un exemple ! La quasi-totalité des programmes existants (ça fait beaucoup) manipulent des données, et doivent les enregistrer pour un usage ultérieur. Pour cela, on peut :
 - enregistrer dans un fichier
 - enregistrer dans le contexte navigateur (localStorage, cookie, session)
 - utiliser une base de données

Les problèmes liés au stockage de données :
 - la persistence
 - la sécurité
 - la performance
 - les accès concurrents

Un serveur de bases de données relationnelles est un outil qui permet de répondre à toutes ces problématiques !

Vous rencontrerez aussi les termes Systèmes de Gestion de Bases de Données Relationnelles (SGBDR), Merise, modèle entités-associations... allez chercher les définitions de ces mots !


## Bases

 - Plusieurs tables
 - Des relations entre les tables


## Méthodologie

 - Dictionnaire des données (nom, type, NULL/NOT NULL)
 - Identification des tables
   - clés primaires
 - Identification des relations entre les tables
   - relation un à plusieurs
   - relation plusieurs à plusieurs (table de liaison)
   - clés étrangères


## Normalisation d'une base de données

Normaliser une BDD, c'est :
 - Garantir un niveau de qualité
 - Répondre aux bonnes pratiques de la profession
 - Travailler plus rapidement


# Conventions de nommage

Le premier niveau d'exigence que vous devez vous imposer, réside dans le nommage de vos tables et champs, tout comme le nommage des variable dans vos programmes :

 - les noms composés sont séparés par un _, ou la première lettre des mots suivants est une majuscule ?
 - Les noms sont-ils en français ou en anglais ?
 - Un s à la fin des noms de table ?
 - Comment je nomme mes clés primaires/étrangères ?


# 1NF : chaque champ est sémantiquement atomique

 - Exemple : champ adresse
 - Exception : champ date


# 2NF : tous les champs dépendent de la clé

 - Attention : clés composées
 - Exemple : LOG(IP,date,codeHTTP,url)


# 3NF : les champs non-clé d'une table n'ont pas de dépendance entre eux

 - Exemple : COMMANDE(ID,date,prix,FDP,reduc,nom_client,mail,rue,cp,ville,tel)


## Lecture

Etre un bon dev, c'est être curieux et exigant avec soi-même.
Si vous souhaitez aller plus loin, il existe d'autres formes normales :

https://fr.wikipedia.org/wiki/Forme_normale_(bases_de_donn%C3%A9es_relationnelles)#1FN_%E2%80%93_Premi%C3%A8re_forme_normale

https://sqlpro.developpez.com/cours/modelisation/merise/?page=base


## Entrainements

- [1. BLOG](1. BLOG.md)
- [1. ECOMMERCE](2. ECOMMERCE.md)
