# Projet-Data-Management-DU---SDA
📊 Projet Data Management & Visualisation - SDA 2025
Analyse des données de la Pandémie COVID-19 (Données OWID)
Ce projet propose une exploration complète du dataset mondial Our World in Data (OWID). Il combine des techniques de Data Engineering, de Visualisation interactive et de Natural Language Processing (NLP) pour comprendre les dynamiques entre politiques sanitaires et vaccination.

📂 Structure
data_management.ipynb : Notebook Jupyter dédié à l'Analyse Exploratoire des Données (EDA). Il contient le pipeline de nettoyage (gestion des NaNs, suppression des agrégats régionaux) et la création de variables.
covid.py : L'application finale développée avec Streamlit. Elle offre une interface utilisateur pour explorer les données en temps réel.
owid-covid-data.csv : Le jeu de données source (> 200 000 lignes) incluant cas, décès, vaccinations et indices de rigueur.
requirements2.txt : Liste des bibliothèques et versions spécifiques pour garantir la reproductibilité.

🛠️ Fonctionnalités Techniques
1. Data Management & Feature Engineering
Nettoyage rigoureux : Filtrage des iso_code et continent pour exclure les données agrégées (Monde, Afrique, etc.) et ne garder que les pays.
Imputation intelligente : Remplacement des valeurs manquantes par 0 pour les statistiques quotidiennes de vaccination et de cas.
Création de variables :
vax_status : Classification des pays selon leur taux de vaccination.
policy_level : Catégorisation de l'indice de rigueur (Basse, Modérée, Élevée).
2. Dashboard Interactif (Streamlit)
Vue d'ensemble (KPIs) : Affichage dynamique du total des cas et des décès selon le filtre géographique.
Analyses Temporelles : Courbes de progression des cas vs décès via Plotly.
Corrélation : Étude de la relation entre l'indice de rigueur gouvernementale et l'occupation des lits en soins intensifs (ICU).
3. Analyse Textuelle (NLP)
Intégration d'un module de traitement du langage naturel pour analyser des articles de santé.
Tokenisation & Nettoyage : Utilisation de NLTK pour filtrer les stopwords français.
Nuage de Mots : Génération visuelle des thématiques prédominantes (ex: ARN messager, variants, confinement).

🚀 Installation et Lancement
Installation des dépendances
Utilisez le fichier de configuration fourni pour installer l'environnement exact :
Bash
pip install -r requirements2.txt

Exécution de l'application
Bash
streamlit run covid.py


📈 Aperçu des Librairies utilisées
Librairie
Usage
Pandas / Numpy
Manipulation et nettoyage des données
Plotly Express
Graphiques interactifs et dynamiques
Streamlit
Interface Web et Dashboarding
NLTK / WordCloud
Traitement du texte et analyse sémantique
Seaborn / Matplotlib
Analyses statistiques dans le notebook

👥 Auteurs
Ibrahima Ba
Mahamat Sultan Mahamat Nour
Moustapha Mendy
