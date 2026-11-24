# Student depression insights

À partir du [Student Depression Dataset](https://www.kaggle.com/datasets/hopesb/student-depression-dataset), cette analyse étudie les variations du taux de dépression déclarée selon les caractéristiques sociodémographiques, territoriales et académiques, les habitudes de vie ainsi que les facteurs psychosociaux, financiers et familiaux des étudiants en Inde.

L'examen systématique des variables précède leur **traitement sous Python** : contrôle des distributions, exclusion des observations appartenant à des modalités faiblement représentées, recodage des catégories, regroupement des diplômes par niveau d'études, puis vérification des valeurs manquantes, des doublons et des types de données. Le jeu initial de **27 901 observations et 18 variables** est ainsi ramené à **27 715 observations et 16 variables**.

Dans **Power Query**, les types numériques et l'interprétation des décimales sont fiabilisés. Des **mesures DAX** permettent ensuite de calculer les effectifs, le taux de dépression déclarée, les écarts au taux global en points de pourcentage et les indices relatifs. L'ensemble est restitué dans un **rapport Microsoft Power BI de sept pages**.

![Vue d'ensemble du rapport Power BI](Screenshot/1.%20Vue%20d%27ensemble.png)


**Ressources :** [Notebook Jupyter](Notebook/student-depression-insights.ipynb) · [Rapport Microsoft Power BI](Microsoft%20Power%20BI/student-depression-insights.pbix) · [Captures d'écran du rapport](Screenshot/)
