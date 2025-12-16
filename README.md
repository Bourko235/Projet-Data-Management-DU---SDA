# Projet Data Management & Visualisation - SDA(Sorbonne Data Analytics) 2025
**Analyse des données de la Pandémie COVID-19 (Données OWID)**

Ce projet a été réalisé dans le cadre du module Data Management, Data Visualisation & Text Mining (DU- SDA 2025-2026). Il s'agit d’un projet de data-management materialisé par application interactive Streamlit permettant l'exploration approfondie des données mondiales de la pandémie de COVID-19.

 ## Structure 
- data_management.ipynb : Notebook Jupyter dédié à l'Analyse Exploratoire des Données (EDA). Il contient le pipeline de nettoyage (gestion des NaNs, suppression des agrégats régionaux) et la création de variables.
- covid.py : L'application finale développée avec Streamlit. Elle offre une interface utilisateur pour explorer les données en temps réel.
- owid-covid-data.csv : Le jeu de données source (> 200 000 lignes) incluant cas, décès, vaccinations et indices de rigueur politique.
- requirements.txt : Liste des bibliothèques et versions spécifiques pour garantir la reproductibilité.
- article_medecine_sciences.txt : L'article de presse pour la partie Text Mining.

## Description 
L'objectif est de fournir une interface utilisateur intuitive pour visualiser l'évolution de la pandémie à travers le monde. L'application traite un jeu de données volumineux (> 200 000 observations) et propose des analyses statistiques, géographiques et textuelles.

### Jeu de Données (Dataset)
- Source : Our World in Data (OWID)
- Lien vers le dataset : https://github.com/owid/covid-19-data
- Fichier utilisé : owid-covid-data.csv
- Volume : Environ 400 000 lignes et 67 colonnes (avant nettoyage).
- Prétraitement : Suppression des agrégats régionaux (OWID_), imputation des valeurs nulles, création de la variable cases_per_million.
  
### Notebook Data Management (data_analysis.ipynb)
Ce notebook documente l'intégralité de la phase de Data Management en amont de l'application. Il détaille la méthodologie rigoureuse appliquée aux données brutes :
- Exploration (EDA) : Analyse de la structure, des types de variables et de la distribution des données .
- Nettoyage : Justification des suppressions (agrégats régionaux), traitement des valeurs manquantes et correction des incohérences .
- Feature Engineering : Création de nouvelles variables pertinentes (ex: ratios normalisés) pour enrichir l'analyse .
- 
### Fonctionnalités Principales de l’application :
- Exploration de Données : Présentation des métadonnées, nettoyage et identification des valeurs manquantes.
- Statistiques Descriptives : Tableaux récapitulatifs et matrices de corrélation dynamiques.
- Visualisation Temporelle : Graphiques interactifs (Courbes, Aires) avec échelle logarithmique optionnelle.
- Cartographie : Carte choroplèthe mondiale interactive (Cas, Décès, Vaccination, PIB).
- Text Mining : Analyse d'un article de presse scientifique (Nuage de mots, fréquences) via NLTK.

## Installation et Lancement

**1. Prérequis**
Assurez-vous d'avoir Python 3.8+ installé.

**2. Installation des dépendances**
Installez les librairies nécessaires listées dans requirements.txt :
pip install requirements.txt

**3. Structure des fichiers**

Assurez-vous que le dossier du projet contient les éléments suivants :
- covid.py : Le code principal de l'application Streamlit.
- owid-covid-data.csv : Le fichier de données (à télécharger si absent).
- article_medecine_sciences.txt : L'article de presse pour la partie Text Mining.

**4. Démarrage de l'application**
Exécutez la commande suivante dans votre terminal : streamlit run covid.py
L'application s'ouvrira automatiquement dans votre navigateur par défaut.

## Aperçu des Librairies utilisées
Librairies
- Pandas / Numpy : Manipulation et nettoyage des données
- Plotly Express : Graphiques interactifs et dynamiques
- Streamlit :Interface Web et Dashboarding
- NLTK / WordCloud : Traitement du texte et analyse sémantique
- Seaborn / Matplotlib : Analyses statistiques et graphiques


## Guide d'Utilisation de l’appli.
- Barre Latérale (Sidebar) - Filtres
- Période d'analyse : Utilisez le slider pour restreindre l'analyse à une plage de dates spécifique.
- Choix des pays : Sélectionnez un ou plusieurs pays pour comparer leurs courbes.
- Échelle Log : Cochez cette case pour mieux visualiser les courbes exponentielles (ex: début d'épidémie).
- Navigation par Onglets
   - 📋 Présentation : Vue d'ensemble technique du dataset (dimensions, types, manquants).
   - 🔢 Statistiques : Moyennes, écarts-types et corrélations sur la sélection actuelle.
   - 📈 Visualisations (Temps) : Évolution des cas, décès, indice de rigueur (Stringency Index) et vaccination.
   - 🌍 Visualisations (Carte) : Comparaison mondiale via une carte colorée et un Top 10 des pays.
   - 📰 Text Mining : Analyse NLP (WordCloud) sur un article médical lié au COVID-19.

## Auteurs
Ibrahima Ba
Mahamat Sultan Mahamat Nour
Moustapha Mendy

DU-SDA 2025-2026 - Projet Data Management.
