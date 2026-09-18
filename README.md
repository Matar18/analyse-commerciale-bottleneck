# Analyse Commerciale – Bottle-Neck (ERP × Web)

Projet d'analyse de données réalisé dans le cadre de ma formation M1 IA & Big Data (ISM).

## Contexte

Bottle-Neck est une cave à vin fictive qui vend à la fois en magasin (données ERP) et sur son site e-commerce (export web). L'objectif est de rapprocher ces deux sources, détecter les anomalies de données, puis produire une analyse commerciale complète.

## Données

- `erp.csv` / `erp.xlsx` : catalogue produit ERP (prix, stock, prix d'achat, statut)
- `liaison.csv` / `liaison.xlsx` : table de correspondance entre l'identifiant web et l'identifiant produit ERP
- `ventes.csv` / `web.xlsx` : export des ventes et fiches produit du site web

## Démarche (notebook `AnalyseCommerciale.ipynb`)

1. **Connexion et rapprochement des données** : jointure ERP ↔ web via la table de liaison, construction de la base de travail
2. **Détection des anomalies** : erreurs de saisie, références non appariées, doublons, valeurs manquantes, erreurs de calcul, incohérences de statut — avec recommandations d'amélioration du système d'information
3. **Analyse du chiffre d'affaires** : CA global, top 10 des produits, analyse de Pareto (règle des 20/80)
4. **Détection des valeurs aberrantes de prix** : Z-score, boxplots
5. **Stocks et rentabilité** : taux de marge par produit, valorisation du stock, rotation des stocks
6. **Corrélations** : matrice de corrélation (Pearson), heatmap, nuages de points

## Résultats clés

- Chiffre d'affaires global : **153 748,10 €**
- Valeur du stock immobilisé (au coût d'achat) : **277 305,77 €**
- Taux de marge moyen du catalogue : **47,40 %**

## Outils

Python, pandas, matplotlib/seaborn, SQLAlchemy/MySQL (jointure), Jupyter Notebook
