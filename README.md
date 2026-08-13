# Atelier Matplotlib — Capteurs IoT

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557C?logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

## Description

Ce projet propose une analyse exploratoire et une visualisation de données issues de capteurs IoT
installés dans plusieurs bâtiments d'une entreprise. Chaque capteur relève régulièrement la
température, l'humidité, la pression atmosphérique, la consommation énergétique et son propre état de
fonctionnement.

L'objectif est de mettre en pratique les principaux types de graphiques Matplotlib afin d'identifier
des tendances, de comparer les bâtiments entre eux et de détecter d'éventuelles anomalies dans les
mesures.

## Jeu de données

Le fichier `mesures_capteurs.csv` contient 605 mesures réparties sur 4 bâtiments (B001 à B004), avec
les colonnes suivantes :

| Colonne | Description |
|---|---|
| `id_mesure` | Identifiant unique de la mesure |
| `date_heure` | Horodatage de la mesure |
| `id_capteur` | Identifiant du capteur |
| `batiment` | Bâtiment concerné |
| `temperature` | Température relevée (°C) |
| `humidite` | Taux d'humidité (%) |
| `pression` | Pression atmosphérique (hPa) |
| `consommation` | Consommation énergétique |
| `etat` | État du capteur (OK, ALERTE, ERREUR) |

## Structure du projet

```
atelier_matplotlib_iot/
├── README.md
├── data/
│   └── mesures_capteurs.csv
├── notebooks/
│   └── atelier_matplotlib_iot.ipynb
└── exports/
    ├── temperature.png
    └── temperature.pdf
```

## Contenu du notebook

| Partie | Sujet |
|---|---|
| 1 | Graphique linéaire — évolution de la température dans le temps |
| 2 | Diagramme en barres — consommation moyenne par bâtiment (vertical et horizontal) |
| 3 | Histogrammes — distribution de la température et de la consommation |
| 4 | Nuage de points — relation entre température et consommation |
| 5 | Diagramme à moustaches — dispersion de la température et de la consommation |
| 6 | Diagramme circulaire — répartition des états des capteurs |
| 7 | Courbes multiples — évolution de la température par bâtiment |
| 8 | Export des graphiques au format PNG et PDF |
| 9 | Analyses complémentaires (heatmap de corrélation, moyenne horaire, comparaison par bâtiment) |

## Prérequis

- Python 3.10 ou supérieur
- pandas
- matplotlib
- jupyter

## Installation

```bash
git clone https://github.com/Massamba0809/atelier_matplotlib_iot.git
cd atelier_matplotlib_iot
pip install -r requirements.txt
```

## Utilisation

```bash
jupyter notebook notebooks/atelier_matplotlib_iot.ipynb
```

Exécuter les cellules dans l'ordre. Les graphiques exportés sont générés dans le dossier `exports/`.

## Résultats clés

- Détection de deux valeurs de température aberrantes, probablement liées à un dysfonctionnement de
  capteur sur le bâtiment B004.
- Le bâtiment B004 présente la consommation énergétique moyenne la plus élevée, le bâtiment B003 la
  plus faible.
- La corrélation entre température et consommation est positive mais faible.
- 94,3 % des capteurs sont en état OK, 4,8 % en ALERTE et 0,8 % en ERREUR.

## Auteur

**Massamba Fall Séne**
Développeur back-end — Dakar, Sénégal
Portfolio : [massamba-fall.vercel.app](https://massamba-fall.vercel.app)
GitHub : [@Massamba0809](https://github.com/Massamba0809)

## Licence

Ce projet est distribué sous licence MIT.
