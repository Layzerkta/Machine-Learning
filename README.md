# Prédiction des Indicateurs de Vie et des Prix Immobiliers

## Description du Projet

Ce projet vise à exploiter des données provenant de multiples sources pour prédire des indicateurs clés liés à la qualité de vie et aux prix immobiliers. En combinant plusieurs algorithmes de machine learning, nous avons cherché à extraire des informations utiles permettant de mieux comprendre les dynamiques socio-économiques dans différentes communes.

### Objectifs
1. **Étape 1** : Explorer le lien entre les données disponibles et l'indicateur "MED14" (revenu moyen par habitant en 2014). 
2. **Étape 2** : Identifier des cibles plus prédictibles, telles que la croissance de la population, le taux de propriété ou le prix de l'immobilier au m².
3. **Étape 3** : Améliorer les prédictions à l'aide de techniques avancées telles que le réglage des hyperparamètres et les méthodes de mixage de données.

---

## Résultats

### Modèles explorés
Nous avons évalué plusieurs algorithmes de machine learning, notamment :
- Gradient Boosting Regressor
- Random Forest Regressor
- Support Vector Regressor
- K-Nearest Neighbors Regressor
- XGBoost Regressor

### Comparaison des performances
Le tableau ci-dessous résume les performances des modèles pour différentes approches et cibles.

![Tableau récapitulatif](Machine-Learning/Capture.png)

- Les meilleurs résultats ont été obtenus avec **XGBoost**, notamment pour prédire le prix au m² des biens immobiliers.
- Le modèle **Random Forest** a également montré de bonnes performances dans plusieurs scénarios.

---

## Phases du Projet

### Étape 1 : Exploration initiale
- **But** : Prévoir "MED14", une mesure de la qualité de vie.
- **Résultat** : Les modèles n'ont pas donné des résultats satisfaisants (faible R² et erreur élevée).

### Étape 2 : Réorientation de l'objectif
- Nous avons testé d'autres cibles, telles que :
  - Croissance de la population
  - Taux de propriété
  - Prix immobilier au m²
- **Décision** : Focalisation sur le prix au m², qui a montré une forte corrélation avec les autres indicateurs.

### Étape 3 : Amélioration des prédictions
- **Optimisation des hyperparamètres** : Peu d'améliorations observées.
- **RegMixup** : Résultats mitigés.
- **Pondération des modèles** : Légère amélioration du RMSE, mais pas significative.

---

## Méthodologie Scientifique

### Pourquoi XGBoost ?
Nous nous sommes inspirés de l'article scientifique "[An Optimal House Price Prediction Algorithm: XGBoost](https://arxiv.org/pdf/2402.04082)" de Hemlata Sharma. Cet article montre que XGBoost est particulièrement efficace pour prédire les prix immobiliers grâce à sa capacité à capturer des relations complexes entre les variables.

Bien que cette étude soit basée sur des données des États-Unis, ses conclusions sont applicables à notre projet en France.

---

## Données

### Sources
Les données ont été collectées à partir de 14 jeux de données distincts, fusionnés en une base unifiée après un nettoyage rigoureux.

### Principales Colonnes
- Revenu moyen par habitant ("MED14")
- Croissance de la population
- Prix immobilier au m²
- Taux de propriété

---
