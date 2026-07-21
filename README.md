<div align="center">

# Student Depression Insights

### Analyse exploratoire des facteurs associés à la dépression chez les étudiants

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557C)
![Excel](https://img.shields.io/badge/Excel-Power%20Pivot-217346?logo=microsoftexcel&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

</div>

---

## Présentation du projet

**Student Depression Insights** est un projet d’analyse de données consacré à l’étude des facteurs associés à la dépression chez les étudiants.

L’objectif est d’examiner les relations entre la variable de dépression et plusieurs dimensions du parcours étudiant :

- pression académique ;
- satisfaction vis-à-vis des études ;
- durée du sommeil ;
- habitudes alimentaires ;
- stress financier ;
- charge de travail et d’études ;
- pensées suicidaires ;
- antécédents familiaux de maladie mentale ;
- âge, sexe et diplôme.

Le projet repose sur une démarche complète de préparation, d’exploration et de visualisation des données avec **Python**, puis sur l’exportation d’un fichier enrichi destiné à **Excel et Power Pivot**.

> Les résultats présentés décrivent des associations statistiques observées dans le dataset. Ils ne permettent ni d’établir une relation de causalité ni de poser un diagnostic médical.

---

## Problématique

> **Quels facteurs académiques, financiers, comportementaux et personnels sont associés aux taux de dépression les plus élevés chez les étudiants de l’échantillon ?**

L’analyse cherche également à identifier les profils et combinaisons de facteurs qui semblent concentrer les niveaux de risque les plus importants.

---

## Source des données

Le projet utilise le **Student Depression Dataset**, disponible sur Kaggle :

[Student Depression Dataset – Kaggle](https://www.kaggle.com/datasets/hopesb/student-depression-dataset)

### Dimensions initiales

| Indicateur | Valeur |
|---|---:|
| Nombre d’observations | 27 901 |
| Nombre de variables | 18 |
| Étudiants conservés après filtrage | 27 870 |
| Observations non étudiantes exclues | 31 |
| Valeurs manquantes initiales | 3 |
| Doublons complets | 0 |

Chaque ligne représente une personne et chaque colonne décrit une caractéristique sociodémographique, académique, comportementale ou liée à la santé mentale.

---

## Démarche analytique

### 1. Chargement et compréhension des données

- importation du fichier CSV avec `pandas` ;
- inspection des dimensions et des types ;
- analyse des modalités des variables qualitatives ;
- production de statistiques descriptives.

### 2. Harmonisation des variables

Les noms de colonnes et les principales modalités ont été traduits et standardisés en français afin d’améliorer la lisibilité du notebook.

Exemples :

| Variable originale | Variable utilisée |
|---|---|
| `Gender` | `sexe` |
| `Academic Pressure` | `pression_academique` |
| `CGPA` | `moyenne_academique` |
| `Study Satisfaction` | `satisfaction_etudes` |
| `Financial Stress` | `stress_financier` |
| `Depression` | `depression` |

### 3. Nettoyage des données

- conversion des variables vers des types adaptés ;
- remplacement des trois valeurs manquantes de `stress_financier` par la médiane ;
- vérification de l’absence de doublons ;
- conservation exclusive des étudiants ;
- suppression de `pression_travail` et `satisfaction_travail`, devenues non pertinentes après le filtrage.

### 4. Création de variables analytiques

Plusieurs variables ont été construites pour faciliter les analyses :

- `depression_num` : codage numérique de la dépression ;
- `tranche_age` ;
- `niveau_pression_academique` ;
- `niveau_satisfaction_etudes` ;
- `niveau_stress_financier` ;
- `classe_moyenne_academique` ;
- variables textuelles simplifiées pour les croisements ;
- `statut_depression` pour Power Pivot ;
- `score_risque`, indicateur exploratoire destiné à la segmentation.

### 5. Analyses descriptives et croisées

Le notebook calcule les effectifs et les taux de dépression selon :

- le sexe ;
- les tranches d’âge ;
- la durée du sommeil ;
- les habitudes alimentaires ;
- la pression académique ;
- la moyenne académique ;
- la satisfaction dans les études ;
- le diplôme ;
- les pensées suicidaires ;
- le stress financier ;
- les antécédents familiaux de maladie mentale.

Des analyses croisées sont également réalisées sur :

- la durée du sommeil et les habitudes alimentaires ;
- les pensées suicidaires et les antécédents familiaux ;
- les pensées suicidaires, le stress financier et la pression académique.

---

## Principaux résultats

Le taux global de dépression observé dans l’échantillon étudiant est de **58,51 %**, soit **16 308 étudiants sur 27 870**.

| Facteur étudié | Groupe présentant le taux le plus élevé | Taux observé |
|---|---|---:|
| Pression académique | Niveau élevé | **86,06 %** |
| Stress financier | Niveau élevé | **81,25 %** |
| Pensées suicidaires | Présence de pensées suicidaires | **79,03 %** |
| Âge | 18–20 ans | **72,34 %** |
| Habitudes alimentaires | Habitudes malsaines | **70,71 %** |
| Satisfaction des études | Niveau faible | **67,51 %** |
| Sommeil | Moins de 5 heures | **64,48 %** |
| Antécédents familiaux | Présence d’antécédents | **61,23 %** |

### Enseignements majeurs

**La pression académique constitue l’un des marqueurs les plus discriminants.**  
Le taux de dépression passe de **27,82 %** lorsque la pression est faible à **86,06 %** lorsqu’elle est élevée.

**Le stress financier est fortement associé à la dépression.**  
Le taux observé atteint **81,25 %** chez les étudiants déclarant un niveau élevé de stress financier, contre **37,35 %** lorsque ce stress est faible.

**Les pensées suicidaires sont associées à l’écart le plus important.**  
Le taux de dépression s’élève à **79,03 %** chez les étudiants concernés, contre **23,19 %** chez les autres.

**Les habitudes de vie semblent également jouer un rôle important.**  
Les étudiants dormant moins de cinq heures ou déclarant des habitudes alimentaires malsaines présentent des taux de dépression plus élevés.

**Le sexe différencie très peu les résultats.**  
Les taux observés sont proches chez les hommes (**58,60 %**) et les femmes (**58,41 %**). Dans cet échantillon, les facteurs académiques, financiers et comportementaux apparaissent donc plus discriminants que le sexe.

---

## Visualisations produites

Le notebook contient notamment :

- une vue globale de la répartition de la dépression ;
- des diagrammes en barres empilées avec effectifs et pourcentages ;
- des graphiques combinant effectifs et taux de dépression ;
- une comparaison des diplômes avec le taux global ;
- des graphiques croisés pour analyser plusieurs facteurs simultanément ;
- des visualisations adaptées à une lecture décisionnelle.

---

## Export Excel et Power Pivot

Le notebook génère le fichier :

```text
student_depression_powerpivot.xlsx
```

La feuille exportée est nommée :

```text
donnees_nettoyees
```

Ce fichier contient les données nettoyées et les variables enrichies nécessaires à la construction :

- de tableaux croisés dynamiques ;
- de mesures DAX ;
- d’indicateurs synthétiques ;
- de graphiques interactifs ;
- d’un tableau de bord sous Excel et Power Pivot.

Le `score_risque` est un indicateur exploratoire construit pour segmenter les observations. Il ne constitue pas un score médical ou clinique validé.

---

## Structure actuelle du dépôt

```text
student-depression-insights/
│
├── student_depression_analysis.ipynb
├── student_depression_raw.csv
├── student_depression_powerpivot.xlsx
├── README.md
├── LICENSE
└── .gitignore
```

Une organisation en sous-dossiers pourra ensuite être mise en place :

```text
student-depression-insights/
│
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── excel/
├── sas/
├── reports/
├── figures/
├── README.md
├── LICENSE
└── .gitignore
```

---

## Technologies utilisées

| Technologie | Utilisation |
|---|---|
| Python | traitement et analyse des données |
| Pandas | manipulation, nettoyage et agrégation |
| NumPy | calcul numérique |
| Matplotlib | création des graphiques |
| Seaborn | outils complémentaires de visualisation |
| Jupyter Notebook | développement et documentation de l’analyse |
| Excel | exploitation du fichier enrichi |
| Power Pivot | modélisation, mesures et tableaux de bord |

---

## Exécuter le projet

### 1. Cloner le dépôt

```bash
git clone https://github.com/mehtiyevanar/student-depression-insights.git
cd student-depression-insights
```

### 2. Installer les dépendances

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

### 3. Vérifier la présence du dataset

Le fichier suivant doit se trouver dans le même dossier que le notebook :

```text
student_depression_raw.csv
```

### 4. Lancer Jupyter Notebook

```bash
jupyter notebook
```

Ouvrir ensuite :

```text
student_depression_analysis.ipynb
```

Puis exécuter les cellules dans leur ordre d’apparition.

---

## Limites de l’analyse

- Les résultats sont propres à l’échantillon étudié et ne peuvent pas être généralisés automatiquement à l’ensemble des étudiants.
- L’analyse est principalement descriptive et exploratoire.
- Les associations observées ne démontrent pas de lien causal.
- Certaines catégories comportent des effectifs plus faibles et doivent être interprétées avec prudence.
- La variable de dépression du dataset ne remplace pas une évaluation clinique.
- Les pensées suicidaires constituent un indicateur sensible qui doit être interprété avec une vigilance particulière.

---

## Améliorations prévues

- ajout d’analyses statistiques inférentielles ;
- mesure de la force des associations entre variables ;
- développement d’un tableau de bord Power BI ;
- adaptation de l’analyse sous SAS ;
- structuration du dépôt en dossiers ;
- ajout d’un dictionnaire complet des variables ;
- export automatique des graphiques dans un dossier `figures/`.

---

## Auteur

**Anar MEHTIYEV**  
Étudiant en **Diplôme d’Université Data Analyst – Informatique et statistiques pour la décision**  
Université de Montpellier

---

## Licence

Ce projet est distribué sous licence **MIT**. Consultez le fichier [`LICENSE`](LICENSE) pour plus d’informations.

---

## Avertissement

Ce projet est réalisé dans un objectif pédagogique et analytique. Il ne fournit aucun diagnostic, conseil médical ou outil de décision clinique. Toute personne confrontée à une souffrance psychologique ou à des pensées suicidaires doit se rapprocher rapidement d’un professionnel de santé ou d’un service d’urgence adapté.
