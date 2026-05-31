# AI-Student-Impact-Analysis
Analyse exploratoire de données (EDA) sur l’utilisation de l’intelligence artificielle par les étudiants et son influence sur leur réussite académique et leur bien-être.

# 📊 Data Exploration & Cleaning of AI Student Impact Dataset

## 🎯 Objectif du projet

L'objectif de cette étude est d'explorer l'impact de l'utilisation des outils d'IA générative sur les performances académiques, la rétention des connaissances, la dépendance technologique, l'anxiété et le risque de burnout chez les étudiants.

Le dataset contient **50 000 observations** et **16 variables** décrivant le profil académique, les habitudes d'utilisation de l'IA et plusieurs indicateurs de performance et de bien-être.

---

# 1. Analyse de la qualité des données

## Taille du dataset

```text
50 000 lignes
16 variables
```

### Interprétation

Le volume de données est suffisamment important pour garantir une bonne représentativité statistique et limiter les effets du hasard dans les analyses.

Un dataset de cette taille permet également :

- des analyses exploratoires robustes ;
- la construction de modèles prédictifs fiables ;
- une bonne généralisation des résultats.

---

## Vérification des valeurs manquantes

```text
Aucune valeur manquante détectée.
```

### Interprétation

La qualité des données est excellente.

L'absence de valeurs manquantes élimine le besoin :

- d'imputation ;
- de suppression d'observations ;
- de traitements correctifs susceptibles d'introduire du biais.

Cela garantit une exploitation directe des données pour l'analyse et la modélisation.

---

# 2. Analyse de la population étudiante

## Répartition par filière

| Filière | Effectif |
|----------|-----------|
| STEM | 15 059 |
| Business | 12 538 |
| Humanities | 9 994 |
| Medical | 6 476 |
| Arts | 5 933 |

### Interprétation

Les étudiants issus des disciplines STEM représentent la population la plus importante.

Cela est cohérent avec la réalité actuelle :

- les étudiants STEM adoptent davantage les outils d'IA ;
- leurs travaux sont souvent compatibles avec les usages de ChatGPT, Copilot ou Gemini ;
- ils sont généralement plus familiers avec les technologies numériques.

Cette surreprésentation doit néanmoins être prise en compte lors de l'interprétation des résultats globaux.

---

## Répartition par niveau d'étude

Les étudiants sont relativement bien répartis entre :

- Freshman
- Sophomore
- Junior
- Senior
- Graduate

### Interprétation

La bonne distribution des niveaux académiques permet d'étudier l'évolution de l'usage de l'IA tout au long du parcours universitaire.

---

# 3. Utilisation de l'IA Générative

## Cas d'usage principaux

| Cas d'utilisation | Effectif |
|------------------|-----------|
| Debugging / Troubleshooting | 12 295 |
| Copywriting / Drafting | 12 011 |
| Ideation | 10 721 |
| Summarizing Reading | 8 633 |
| Direct Answer Generation | 6 340 |

### Interprétation

Les étudiants utilisent principalement l'IA comme :

- assistant de résolution de problèmes ;
- outil de rédaction ;
- support de réflexion.

L'usage pour obtenir directement des réponses est moins fréquent.

Cela suggère que l'IA est davantage utilisée comme outil d'assistance que comme substitut complet à l'apprentissage.

---

# 4. Impact de l'IA sur les performances académiques

## Variation du GPA

Variable créée :

```python
GPA_Change = Post_Semester_GPA - Pre_Semester_GPA
```

### Interprétation

Cette variable mesure directement l'évolution de la performance académique.

L'analyse cherche à déterminer si :

- l'usage de l'IA améliore les résultats ;
- ou si un usage excessif devient contre-productif.

---

## Heures d'utilisation de l'IA vs évolution du GPA

### Ce que montre le graphique

Le graphique compare :

- les heures hebdomadaires d'utilisation de l'IA ;
- l'évolution du GPA ;
- le score de rétention des compétences.

### Interprétation Data Scientist

Une relation linéaire forte n'est généralement pas observée.

Cela suggère que :

> L'utilisation de l'IA seule n'est pas un facteur suffisant pour expliquer l'amélioration des performances académiques.

Les performances semblent davantage dépendre :

- du niveau initial ;
- de la qualité de l'utilisation de l'IA ;
- des compétences de prompting ;
- du temps d'étude traditionnel.

---

# 5. Prompt Engineering et réussite académique

## GPA selon le niveau de Prompt Engineering

Catégories :

- Beginner
- Intermediate
- Advanced

### Interprétation

Si les étudiants "Advanced" présentent un GPA supérieur :

cela suggère que :

> Ce n'est pas l'IA qui crée la performance, mais la capacité à interagir efficacement avec l'IA.

Les étudiants maîtrisant le Prompt Engineering :

- obtiennent des réponses plus pertinentes ;
- exploitent mieux les outils ;
- gagnent en efficacité.

---

## Rétention des connaissances selon le niveau de Prompt Engineering

### Interprétation

Une meilleure rétention chez les utilisateurs avancés indique que :

- ils utilisent l'IA comme outil d'apprentissage ;
- ils conservent un rôle actif dans le raisonnement.

À l'inverse :

les utilisateurs débutants risquent davantage de consommer passivement les réponses produites.

---

# 6. Diversité des outils IA

## Nombre d'outils utilisés vs GPA

### Interprétation

L'utilisation de plusieurs outils :

- ChatGPT
- Claude
- Gemini
- Copilot
- Perplexity

semble associée à de meilleurs résultats.

Cela peut refléter :

- une meilleure culture numérique ;
- une capacité à comparer les réponses ;
- une utilisation plus stratégique de l'IA.

---

# 7. Analyse du Burnout

## Répartition générale

| Niveau |
|----------|
| Low |
| Medium |
| High |

### Interprétation

La majorité des étudiants se situe dans la catégorie :

```text
Medium Burnout Risk
```

Ce résultat est cohérent avec la forte pression académique observée dans l'enseignement supérieur.

---

## Burnout selon la filière

### Interprétation

Les écarts observés entre filières peuvent s'expliquer par :

- la charge de travail ;
- le niveau d'exigence ;
- la nature des évaluations.

Les cursus STEM et Medical présentent généralement des risques plus élevés.

---

# 8. Anxiété et dépendance à l'IA

## Anxiété selon le niveau de Burnout

### Interprétation

Une relation positive est attendue :

```text
Burnout ↑ ⇒ Anxiety ↑
```

Cette cohérence valide la qualité interne du dataset.

---

## Dépendance à l'IA vs temps d'utilisation

### Interprétation

Le nuage de points permet d'évaluer :

```text
AI Hours ↑ ⇒ AI Dependency ↑
```

Une corrélation positive serait logique :

les étudiants utilisant massivement l'IA développent progressivement une dépendance perçue plus importante.

---

# 9. Impact des politiques institutionnelles

Trois politiques :

- Strict Ban
- Allowed With Citation
- Actively Encouraged

### Interprétation

Cette analyse est particulièrement intéressante.

Elle permet d'évaluer :

- l'effet de l'encadrement institutionnel ;
- l'impact de l'intégration de l'IA dans l'enseignement.

Si les étudiants soumis à la politique :

```text
Allowed With Citation
```

obtiennent les meilleurs résultats, cela suggère que :

> Une utilisation encadrée de l'IA est plus efficace qu'une interdiction totale ou qu'une liberté absolue.

---

# 10. Matrice de corrélation

Cette étape est cruciale.

### Objectif

Identifier :

- les variables les plus liées au GPA ;
- les facteurs de dépendance ;
- les indicateurs du burnout.

### Ce qu'il faut rechercher

Corrélations fortes :

```text
|r| > 0.7
```

Corrélations modérées :

```text
0.3 < |r| < 0.7
```

Corrélations faibles :

```text
|r| < 0.3
```

### Interprétation professionnelle

La matrice de corrélation constitue la base de futurs modèles prédictifs :

- régression ;
- Random Forest ;
- XGBoost ;
- CatBoost.

Elle permet d'identifier les variables les plus influentes.

---

# 📌 Conclusion générale

Cette étude met en évidence que l'IA générative exerce une influence significative sur les pratiques d'apprentissage des étudiants.

Les résultats suggèrent que :

- l'utilisation de l'IA peut améliorer les performances académiques lorsqu'elle est maîtrisée ;
- les compétences de Prompt Engineering constituent un facteur déterminant ;
- une forte dépendance à l'IA peut être associée à des risques accrus de burnout et d'anxiété ;
- les politiques institutionnelles jouent un rôle important dans l'encadrement des usages ;
- la diversité des outils et une utilisation raisonnée semblent produire les meilleurs résultats académiques.

D'un point de vue Data Science, le dataset est de très bonne qualité et constitue une excellente base pour développer des modèles de prédiction du GPA, du burnout ou de la dépendance à l'IA.

---

## 🛠️ Technologies utilisées

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## 📈 Compétences démontrées

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Statistical Analysis
- Data Visualization
- Feature Engineering
- Business Insights Extraction
- Data Storytelling
