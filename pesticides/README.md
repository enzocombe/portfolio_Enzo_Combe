# L'influence des pesticides sur le chiffre d'affaires des agriculteurs

Projet d'économétrie réalisé en groupe de 4 (Licence Économie et Gestion, Université Grenoble Alpes, 2025).

**Rapport en ligne : https://enzocombe.github.io/portfolio_Enzo_Combe/pesticides/**

## Question
Comment les dépenses en produits phytosanitaires influencent-elles le chiffre d'affaires des exploitations agricoles françaises ?

## Données
- **RICA 2023** : 7 220 exploitations, 986 variables.
- **BNV-D** : ventes de substances phytosanitaires par région, 2013-2023.
- Les données ne sont pas incluses (licence d'accès). Pour relancer le code, placer les deux CSV dans un dossier `data/`.

## Méthode (R)
- Nettoyage et fusion des deux bases (tidyverse)
- Régressions MCO log-log : sans région, avec effets fixes régionaux, CA par hectare, terme quadratique
- Test de Breusch-Pagan et erreurs robustes de White (HC3)
- Analyse du biais de sélection et de l'endogénéité

## Résultats principaux
- Élasticité du chiffre d'affaires aux achats de produits phytosanitaires d'environ **0,3** (significative) : +1 % d'achats est associé à environ +0,3 % de CA.
- Le travail est le facteur le plus élastique (environ 1,1).
- R² de 0,37 sans effets régionaux, 0,44 avec.

## Limites
- Résultats à lire comme des **associations**, pas des effets causaux (endogénéité non corrigée).
- Seules 27 % des exploitations sont appariées avec les données régionales (échantillon commun de 1 617), et les exploitations sans achat de pesticides sont exclues.
- Variables omises : prix, météo, rendements physiques.

## Fichiers
- `Pesticide_corrige.Rmd` : code et rapport (R Markdown)
- `index.html` : rapport compilé
