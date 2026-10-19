# Warmup Java

Exercices et essais en Java autour des structures de données, des algorithmes et des bases du langage. Le sujet principal est la percolation, étudiée sur une grille et simulée à l’aide d’une structure Union-Find.

## Sujet principal : percolation

`src/Percolation.java` modélise une grille carrée de 10 × 10 cases. Une case peut être ouverte ou bloquée. Le programme ouvre des cases choisies aléatoirement jusqu’à ce qu’un chemin de cases ouvertes relie le haut de la grille au bas.

Le fichier contient plusieurs approches de détection :

- un parcours récursif de la grille (`detectPath` et `isNaivePercolation`) ;
- une approche fondée sur Union-Find, avec des cases virtuelles reliées aux bords supérieur et inférieur ;
- une simulation Monte-Carlo, qui répète l’expérience et calcule une estimation du seuil de percolation.

La méthode `main` attend en argument le nombre de simulations à effectuer. Le programme est encore en cours de développement : certaines méthodes présentent des incohérences, et la version actuelle doit être corrigée avant de pouvoir être considérée comme exécutable.

## Structure du dépôt

```text
src/
	Percolation.java   Simulation de percolation et méthodes de détection
	UnionFind.java     Structure de regroupement utilisée par la percolation
	Bug1.java ...      Variantes d'un exercice de calcul de factorielle
	ExerciceUN.java    Premiers exercices sur les calculs et les types numériques
	ExerciceDeux.java  Fichier d'exercice encore vide
	App.java           Point d'entrée généré par le projet Java
	HelloProgram.java  Exemple minimal affichant « Hello »
	Empty.java         Classe vide

Percolation(n).java  Versions alternatives successives de Percolation
UnionFind*.java      Versions alternatives de UnionFind
lib/                 Emplacement prévu pour les dépendances
bin/                 Sorties compilées du projet
```

Les variantes numérotées à la racine sont des essais ou des versions antérieures ; les fichiers de `src/` constituent l’organisation principale du projet. Plusieurs variantes déclarent les mêmes classes (`Percolation` ou `UnionFind`) et ne sont donc pas destinées à être utilisées simultanément.

## Union-Find

`src/UnionFind.java` explore plusieurs opérations de recherche et d’union : versions naïves, versions dites rapides et méthodes de recherche avec compression de chemin. Dans la simulation, chaque case ouverte est reliée à ses voisines ouvertes ; la grille percole lorsque les deux cases virtuelles des bords sont dans le même ensemble.

## Exercices complémentaires

Les classes `Bug1.java` à `Bug8.java` reprennent un programme qui lit un entier et calcule sa factorielle. Elles servent à comparer différentes versions et à repérer des erreurs de signature ou de structure. `ExerciceUN.java` contient des essais sur la factorielle, la division entière et les constantes `Math.PI` et `Math.E`.

## Environnement

Le projet est organisé comme un projet Java simple dans VS Code. Les fichiers sources se trouvent principalement dans `src/`, les dépendances éventuelles dans `lib/` et les fichiers compilés dans `bin/`. Aucun framework de test ou système de construction dédié n’est présent dans le dépôt.
# percolation
