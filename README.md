# Diagnostic des maladies cardiaques – Analyse exploratoire des données

Analyse exploratoire du dataset Heart Disease – Cleveland (Kaggle, 303 patients, 14 variables cliniques) visant à identifier les facteurs associés aux maladies cardiaques et à préparer les données pour un modèle de prédiction.

## Outils et bibliothèques
- Python, Google Colab
- pandas, NumPy
- Matplotlib, Seaborn
- SciPy

## Démarche d'analyse

**1. Qualité et préparation des données**
- Vérification des valeurs manquantes et des types de variables
- Détection des valeurs aberrantes par la méthode IQR
- Choix du traitement selon la nature des données : transformation logarithmique pour la pression artérielle (9 outliers, mesures réelles conservées), suppression pour le cholestérol (5 outliers, écart-type réduit de 51,8 à 45,1)

**2. Analyse univariée**
- Statistiques descriptives et étude des distributions (histogrammes, boxplots)
- Vérification de la normalité par QQ-plots, avant et après traitement

**3. Analyse bivariée**
- Corrélations de Pearson entre variables explicatives, avec test de transformations (log, racine carrée, Box-Cox)
- Clustering hiérarchique pour détecter des groupes de variables liées
- Tests statistiques face au diagnostic : test de Student (variables quantitatives) et test du Chi² (sexe)

## Résultats

- Les patients atteints sont en moyenne plus âgés et présentent une pression artérielle plus élevée.
- Les hommes sont proportionnellement plus touchés que les femmes.
- Corrélation modérée entre l'âge et la pression artérielle (r ≈ 0,29).
- L'âge, le sexe et la pression artérielle sont retenus comme prédicteurs pertinents pour une régression logistique.

