
# Détection de Diabète - INF8245AE (Automne 2024)

Ce projet a été réalisé dans le cadre du cours **INF8245AE - Machine Learning** à l'École Polytechnique de Montréal. 
Il s'inscrit dans une compétition Kaggle portant sur la détection du diabète à partir de données cliniques.

## Architecture du répertoire

- ./
- ./data/train.csv
- ./data/labels.csv
- ./data/test.csv
- ./final.ipynb
- ./README.md
- ./requirements.txt

## Description du projet

L'objectif est de construire un modèle performant pour prédire la présence de diabète en s'appuyant sur des données déséquilibrées. 
Plusieurs algorithmes d'apprentissage automatique ont été testés et comparés pour optimiser la précision des prédictions tout en tenant compte du déséquilibre des classes. Les données se trouvent dans le lien suivant : [kaggle.com/competitions/inf-8245-e-fall-2024](https://www.kaggle.com/competitions/inf-8245-e-fall-2024).

## Contenu du notebook

- **Présentation du projet** : Contexte et objectifs.
- **Importation des bibliothèques** : Chargement des outils nécessaires comme `pandas`, `numpy`, `matplotlib`, ainsi que des bibliothèques de modèles (`LightGBM`, `XGBoost`, `CatBoost`, etc.).
- **Exploration des données** : Analyse préliminaire des caractéristiques des données.
- **Pré-traitement des données** : Utilisation d'approches comme le standard scaling et le sous-échantillonnage avec `RandomUnderSampler`.
- **Modélisation** : 
  - Test de plusieurs algorithmes (LightGBM, XGBoost, CatBoost, HistGradientBoosting et ExtraTrees).
  - Évaluation des modèles à l'aide de métriques telles que le score F1.
  - Ajustement des hyperparamètres pour améliorer les performances.
- **Analyse des résultats** : Comparaison des modèles et interprétation des résultats.

## Instructions pour exécuter le notebook

1. **Prérequis** : 
   - Python 3.11.5
   - Installez les dépendances en utilisant :
     ```pip install -r requirements.txt```
     - ou sinon par conda : ``` conda create -n "myenv" -f requirements.txt python=3.11.5 ipython ```
2. **Exécutez le notebook** :
   - Lancez Jupyter Notebook avec l'environnement "myenv" ou tout autre environnement compatible.
   - Ouvrez et exécutez le fichier `final.ipynb`.

## Technologies utilisées

- **Langage** : Python
- **Bibliothèques principales** :
  - `pandas`, `numpy`, `matplotlib` pour le traitement et la visualisation des données.
  - `sklearn` pour les étapes de pré-traitement et d'évaluation, ainsi que l'instanciation des modèles `HistGradientBoosting` et `ExtraTrees`.
  - `LightGBM`, `XGBoost`, `CatBoost` pour la modélisation.

## Auteurs

Projet réalisé par les étudiants du cours **INF8245AE** à l'École Polytechnique de Montréal : 
- Membres de l’´equipe: Adrien Wils, Augustin Cucchi et Elie Saleh
- E-mails: adrien.wils@polymtl.ca, augustin.cucchi@polymtl.ca et elie.saleh@polymtl.ca
- Matricules: 2403911, 2403527 et 240331

## Remarque importante

Les performances des modèles reportées dans le notebook reflètent des tests indépendants des caractéristiques de chaque algorithme. 
Ces résultats peuvent légèrement différer de ceux obtenus en utilisant une recherche exhaustive des hyperparamètres (GridSearch).