# Déterminants des prix du transport aérien américain

Projet d'économétrie réalisé en groupe de 3 (Licence Économie et Gestion, Université Grenoble Alpes).

**Rapport : [Rapport_econometrie.pdf](Rapport_econometrie.pdf)**

## Question
Quels sont les déterminants microéconomiques de la formation des prix sur le marché intérieur américain du transport aérien ?

## Données
Base AIRFARE (Wooldridge, *Introductory Econometrics*, distribuée avec Gretl) : tarifs moyens sur des liaisons aériennes américaines. Coupe transversale de l'année 2000 : 1 149 liaisons.

## Méthode (Gretl)
- Modèle MCO log-log : log(prix) expliqué par log(distance), log(distance)², concentration du marché et log(passagers)
- Tests d'hétéroscédasticité de White et de Breusch-Pagan
- Erreurs robustes (HC1), tests de Student et de Fisher

## Résultats principaux
- Relation convexe entre distance et prix.
- +10 points de part de marché du transporteur dominant : environ +2,2 % sur le prix.
- +1 % de passagers : environ -0,08 % sur le prix.
- Toutes les variables sont significatives à 1 % ; R² = 0,40.

## Limites
Pas de date de réservation ni de classe de voyage, prix moyen par liaison, coûts aéroportuaires non pris en compte, multicolinéarité entre log(distance) et log(distance)².
