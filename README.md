# analyse-ventes-cigarettes
Projet d’analyse de données de ventes de cigarettes (Python)
Analyse des ventes de cigarettes par région et canal

Ce projet présente une analyse descriptive des ventes d’une marque de cigarettes.
L’objectif est de mieux comprendre les tendances commerciales selon la région, le canal de distribution et le type de produit.

🎯 Objectifs du projet

Explorer et nettoyer les données de ventes

Analyser les performances par :

Région (Nord, Sud, Est, Ouest, Centre)

Canal de vente (Revendeur, Boutique, En ligne)

Type de cigarette (Produit A, B, C, etc.)

Fusionner les données de ventes avec les objectifs

Visualiser les résultats à l’aide de graphiques interactifs

📁 Contenu du projet
Fichier	Description
ventes_cigarettes_modifie.xlsx	Base de données avec deux feuilles : Ventes et Objectifs
analyse_ventes.ipynb	Notebook Jupyter contenant tout le code d’analyse
README.md	Ce fichier de présentation du projet
🧹 Étapes principales de l’analyse

Chargement des données

Importation des fichiers Excel avec pandas.read_excel()

Nettoyage

Vérification et traitement des valeurs manquantes

Conversion des dates et calcul du chiffre d’affaires

Fusion

Jointure entre Ventes et Objectifs sur les colonnes communes

Analyse

Calculs par région, produit et canal

Évolution mensuelle du chiffre d’affaires

Visualisations

Diagrammes à barres, camemberts et courbes avec matplotlib et plotly

📈 Exemple de graphique
import plotly.express as px

fig = px.bar(df_grouped,
             x='Région',
             y='Chiffre_affaires',
             color='Canal',
             barmode='group',
             title='Chiffre d’affaires par région et canal de distribution')
fig.show()

🧰 Outils utilisés

Python 3

Pandas (manipulation de données)

Matplotlib & Plotly (visualisation)

Jupyter Notebook

Excel (source de données)

💡 Résultats attendus

Identifier les régions les plus performantes

Comprendre la répartition des ventes selon les canaux

Repérer les produits les plus vendus

Comparer les ventes réelles aux objectifs fixés

👩‍💻 Auteur

Projet réalisé dans le cadre d’un apprentissage en analyse de données avec Python.
L’objectif est de développer les compétences en nettoyage, transformation et visualisation de données.
