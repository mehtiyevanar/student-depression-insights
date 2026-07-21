<div align="center">

# Student Depression Insights

Analyse exploratoire des facteurs associés à la dépression chez les étudiants à partir d’un jeu de données public.

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-Power%20Pivot-217346?logo=microsoftexcel&logoColor=white)

</div>

## Présentation

Ce projet étudie les relations entre la dépression étudiante et plusieurs facteurs académiques, financiers et personnels : pression académique, satisfaction dans les études, sommeil, habitudes alimentaires, stress financier, pensées suicidaires et antécédents familiaux.

Le notebook couvre la préparation des données, l’analyse descriptive, la création de variables, les visualisations et l’export d’un fichier structuré pour Excel Power Pivot.

## Objectifs

- nettoyer et structurer le dataset ;
- identifier les facteurs associés aux taux de dépression les plus élevés ;
- produire des visualisations claires et interprétables ;
- préparer les données pour une analyse complémentaire dans Power Pivot.

## Contenu du dépôt

```text
student-depression-insights/
├── student_depression.ipynb
├── student_depression_raw.csv
├── student_depression_powerpivot.xlsx
├── README.md
├── LICENSE
└── .gitignore
```

| Fichier | Description |
|---|---|
| `student_depression.ipynb` | Nettoyage, analyses et visualisations Python |
| `student_depression_raw.csv` | Dataset original |
| `student_depression_powerpivot.xlsx` | Données nettoyées et enrichies pour Power Pivot |

## Méthodologie

1. Exploration de la structure et de la qualité des données  
2. Harmonisation des noms de variables et des modalités  
3. Traitement des valeurs manquantes et filtrage des étudiants  
4. Création de variables analytiques et de classes  
5. Calcul des taux de dépression par facteur  
6. Visualisation des principaux résultats  
7. Export des données vers Excel Power Pivot  

## Technologies

- **Python**
- **Pandas** et **NumPy**
- **Matplotlib** et **Seaborn**
- **Jupyter Notebook**
- **Excel Power Pivot**

## Exécution

Clonez le dépôt :

```bash
git clone https://github.com/mehtiyevanar/student-depression-insights.git
cd student-depression-insights
```

Installez les dépendances :

```bash
pip install pandas numpy matplotlib seaborn openpyxl jupyter
```

Lancez ensuite :

```bash
jupyter notebook student_depression.ipynb
```

Le fichier `student_depression_raw.csv` doit rester dans le même dossier que le notebook.

## Source des données

Dataset utilisé : [Student Depression Dataset – Kaggle](https://www.kaggle.com/datasets/hopesb/student-depression-dataset)

## Limites

Cette analyse est descriptive et exploratoire. Les associations observées ne démontrent pas de relation causale et ne constituent ni un diagnostic médical ni un outil clinique.

## Licence

Ce projet est distribué sous licence [MIT](LICENSE).
