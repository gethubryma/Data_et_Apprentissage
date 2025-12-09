# Data et Apprentissage

Ce projet regroupe une série de travaux pratiques autour de l’**apprentissage automatique**, de la **statistique**, de la **détection d’anomalies** et du **clustering** .

## Structure du projet

* **data_et_apprentissage_1.ipynb**
  Contient :

  * la régression robuste,
  * la malédiction de la dimension,
  * l’évaluation des modèles,
  * l’apprentissage en ligne,
  * la régularisation.

* **data_et_apprentissage_2.ipynb**
  Contient :

  * les modèles probabilistes,
  * la détection d’anomalies,
  * le clustering incrémental,
  * la repondération des distances,
  * les approches avancées de clustering.

## Notebook 1 — `data_et_apprentissage_1.ipynb`

### RANSAC et estimation robuste

* Implémentation **from scratch** de l’algorithme **RANSAC** pour la **régression linéaire robuste**.
* Comparaison avec :

  * la **régression linéaire classique**,
  * l’implémentation **RANSAC de scikit-learn**.
* Étude de plusieurs scénarios de **bruit et d’outliers** :

  * outliers symétriques,
  * bruit uniquement positif,
  * outliers localisés dans une zone spécifique.
* Analyse qualitative et graphique de la **robustesse des modèles**.
* Implémentation d’une **variante RANSAC basée sur le vote des modèles**.
* Extension du principe RANSAC à :

  * l’estimation robuste du **centre d’un nuage de points**,
  * le **clustering robuste** (type RANSAC-k-means).
* Rédaction d’un **pseudo-code généralisé** pour RANSAC.

### Malédiction de la dimension

* Étude empirique de la **curse of dimensionality** à partir du livre
  *The Elements of Statistical Learning* (Section 2.5).
* Reproduction expérimentale des résultats illustrés dans les figures :

  * 2.6, 2.7, 2.8 et 2.9.
* Analyse de l’impact de la **dimensionnalité** sur :

  * les distances,
  * la densité des données,
  * le comportement des méthodes d’apprentissage.

### Évaluation des modèles et validation

* Étude empirique du **ratio train/test** en classification.
* Analyse de l’évolution des performances en fonction du ratio.
* Justification théorique via le **compromis biais–variance**.
* Mise en place d’un schéma **train / validation / test**.
* Optimisation des **hyperparamètres**.
* Étude de la **cross-validation** dans le cadre des **séries temporelles**, avec respect de l’ordre temporel.

### Apprentissage en ligne (stream processing)

* Classification linéaire dans un contexte de **flux de données**.
* Données reçues séquentiellement, sans stockage global.
* Développement d’un modèle **frugal**, mis à jour à chaque instant.
* Génération de données synthétiques via **distributions gaussiennes 2D**.
* Suivi des performances du modèle au cours du temps.
* Comparaison avec un classifieur entraîné en **batch**.

---

### Régression Ridge et Lasso

* Application de la **régression Ridge** et de la **régression Lasso**.
* Optimisation du paramètre de régularisation **α** par **validation croisée**.
* Analyse de :

  * l’évolution des **coefficients** en fonction de α,
  * les **résidus**,
  * le score de performance **R²**.
* Discussion sur l’effet de la régularisation sur la **généralisation**.
* 
## Notebook 2 — `data_et_apprentissage_2.ipynb`

### Modèle probabiliste – Système de sécurité

* Modélisation probabiliste d’un système composé de :

  * une batterie,
  * deux capteurs,
  * une alarme.
* Construction du **modèle graphique**.
* Calcul des **probabilités conjointes et marginales**.
* Étude de l’**indépendance conditionnelle** des variables.
* Inférences bayésiennes (posteriors).
* Validation empirique via **simulations Monte Carlo**.

---

### Détection d’anomalies : IF et LOF

* Implémentation **from scratch** de **Local Outlier Factor (LOF)**.
* Comparaison avec l’implémentation **scikit-learn**.
* Étude de **Isolation Forest (IF)** pour les outliers globaux.
* Proposition d’une méthode **hybride LOF + IF**.
* Comparaison expérimentale entre :

  * LOF,
  * IF,
  * LOF+IF.
* Analyse des forces et limites de chaque approche.

### Clustering top-down incrémental

* Étude des méthodes de **clustering hiérarchique top-down**.
* Implémentation de :

  * **bisecting k-means**,
  * **global k-means (greedy)**,
  * **fast global k-means**,
  * **global++**.
* Analyse théorique des propriétés des solutions obtenues.
* Expérimentations sur :

  * le clustering de couleurs,
  * des données synthétiques organisées en **grille 2D**.
* Extension des méthodes au cas des **GMM**, avec l’algorithme **EM**.
* Discussion des difficultés du **bisecting** en contexte probabiliste.

### Repondération des distances

* Définition de distances pondérées **$dist′(xi, xj)$**.
* Approches basées sur :

  * **noyaux (RBF)**,
  * **clustering plat**,
  * **clustering hiérarchique**,
  * **clustering incrémental**.
* Construction de mesures de poids **wij** exploitant la structure des données.
* Expérimentations sur données synthétiques.
* Analyse de l’impact sur la structure des distances.

---

## Technologies utilisées

* **Python**
* **NumPy**, **SciPy**
* **scikit-learn**
* **Matplotlib / Seaborn**
* **Jupyter Notebook**

## Objectifs 

* Comprendre les **fondements théoriques** de l’apprentissage automatique.
* Implémenter des algorithmes **from scratch**.
* Comparer des approches classiques et avancées.
* Analyser empiriquement les comportements des modèles.
* Développer un raisonnement critique sur les méthodes de **data science**.

