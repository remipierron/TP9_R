# TP 8 : Visualiser des données avec ggplot2

Introduction au langage R · Cnam · USSI6B-1

## Démarrer

1. Décompressez l'archive `tp8.zip`, puis ouvrez le projet en double-cliquant sur `tp8.Rproj`.
2. L'énoncé est en PDF sur Moodle.
3. Installez si besoin les packages dans la **console** (pas dans le document) : `install.packages(c("patchwork", "ggrepel", "Hmisc"))`.
4. Créez votre document R Markdown **`tp8_nom_prenom.Rmd`** (format HTML) **à la racine du dossier**, pour que les chemins `data/…` fonctionnent.
5. Son premier chunk charge les packages :

   ````
   ```{r setup, include = FALSE}
   library(tidyverse)
   library(patchwork)
   ```
   ````

   Si les noms de mois et de jours s'affichent en anglais, ajoutez `Sys.setlocale("LC_TIME", "fr_FR.UTF-8")` dans ce chunk (sous Windows : `Sys.setlocale("LC_TIME", "French")`).

6. Structure : `# Partie A`, puis `## A1`, `## A2`… comme dans l'énoncé.

## Contenu du dossier

| Fichier | Contenu |
|---|---|
| `data/ble_anova2.csv` | rendements de quatre variétés de blé, avec ou sans traitement (séparateur `;`) |
| `data/paysniv3.RData` | indicateurs de 173 pays en 1987 (à charger avec `load()`) |
| `data/ventes_2025.csv` | ventes quotidiennes de trois magasins en 2025 (fictives, août manquant) |

Le jeu `economics` est livré avec `ggplot2`. **Ne modifiez pas** les fichiers de `data/`.

## Rendu

- Déposez sur Moodle **deux fichiers** : votre `.Rmd` et le `.html` knitté sans erreur.
- Seul ce qui est déposé à la date limite (voir Moodle) est pris en compte.
