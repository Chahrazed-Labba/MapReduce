# Description du TP

Ce TP founi une implémentation de l'algorithme WordCount utilisant le paradigme MapReduce en Java. 
L'objectif principal de ce TP est de démontrer comment utiliser le modèle MapReduce de Hadoop pour traiter des données volumineuses stockées sur HDFS en effectuant des calculs distribués, notamment le comptage de mots dans un grand fichier texte.


## Qu'est-ce que MapReduce ?

MapReduce est un modèle de programmation distribué conçu pour le traitement de grandes quantités de données. Il divise les tâches en deux étapes principales :
### Map : 
Chaque enregistrement de données est transformé en une paire clé-valeur. Par exemple, chaque mot dans un texte peut être une clé associée à la valeur 1.
### Reduce : 
Les paires clé-valeur générées sont regroupées par clé, et une opération de réduction est appliquée (comme une somme ou une concaténation).
Cette approche est hautement scalable et permet de traiter des données massives en parallèle sur plusieurs machines.

## Hadoop ?

Apache Hadoop est un framework open source conçu pour le traitement distribué de grands ensembles de données à travers des clusters d'ordinateurs. Il offre :
### HDFS (Hadoop Distributed File System) : 
Un système de fichiers distribué conçu pour gérer des données massives avec une tolérance aux pannes.
### MapReduce : 
Un moteur de traitement qui exécute les tâches Map et Reduce sur des données stockées dans HDFS.
Hadoop est idéal pour des tâches comme le comptage de mots dans de grands fichiers, car il répartit efficacement le travail sur plusieurs machines.

## Fonctionnalités Principales

1. Lecture des Données : Le programme lit un fichier texte en entrée.
2. Étape Map :
- Chaque ligne du fichier est transformée en mots individuels.
- Chaque mot est émis sous la forme (mot, 1).
3. Étape Shuffle and Sort : Les paires (mot, 1) sont regroupées par mot.
4. Étape Reduce : Les occurrences de chaque mot sont agrégées pour obtenir un comptage total.
5. Sortie des Résultats : Les résultats sont enregistrés dans un fichier de sortie.
