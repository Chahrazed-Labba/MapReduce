# README: Projet WordCount en Java avec Hadoop

## Description

Ce projet utilise le paradigme **MapReduce** et le framework **Hadoop** pour compter les occurrences de mots dans un fichier texte. Le programme est écrit en Java et s’appuie sur des composants comme le Mapper, le Reducer et le Driver pour exécuter des tâches distribuées.

## Fonctionnement

1. **Étape Map** : Transforme chaque mot d'un fichier texte en une paire `(mot, 1)`.
2. **Étape Reduce** : Agrège les occurrences pour chaque mot et génère le total.
3. **Sortie** : Résultats écrits dans un fichier texte.

## Prérequis

- **Java 8+**
- **Hadoop 3.3.6**
- Un IDE comme IntelliJ IDEA ou Eclipse.
- Fichiers Maven (pom.xml inclus).

## Instructions

1. Compiler le projet :
   ```bash
   mvn clean package
   ```
2. Exécuter le job Hadoop :
   ```bash
   hadoop jar target/WordCount-1.0-SNAPSHOT.jar com.example.hadoop.WordCount <input_path> <output_path>
   ```

## Exemple

### Entrée
```txt
Bonjour monde
Bonjour Hadoop
Hadoop est puissant
```

### Sortie
```txt
Bonjour	2
Hadoop	2
est	1
monde	1
puissant	1
```


