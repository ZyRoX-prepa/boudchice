# TP: Introduction à l'analyse statistique bivariée sous Python

**ESI Rabat - 1ème A CI - 2025/2026**  
**Statistique Descriptive**  
**Professeur: F. Boudchich**

---

## Description du Projet

Ce projet contient un **Jupyter Notebook complet** qui reproduit et exécute tous les exercices pratiques du cours de statistique descriptive. Le notebook couvre l'analyse statistique bivariée avec Python.

## Fichiers du Projet

- **`TP_Statistique_Descriptive.ipynb`** - Notebook Jupyter contenant tous les exercices (22 KB)
- **`TPstatistiqueDescriptive.pdf`** - Document original avec les consignes
- **`README.md`** - Ce fichier

## Installation et Configuration

### Prérequis

- Python 3.7 ou supérieur
- pip (gestionnaire de paquets Python)

### Installation des dépendances

```bash
pip install jupyter pandas numpy scipy matplotlib seaborn scikit-learn
```

Ou pour installer tous les packages en une commande:

```bash
pip install -r requirements.txt
```

### Lancer le Notebook

```bash
cd /tmp/workspace/ZyRoX-prepa/boudchice
jupyter notebook TP_Statistique_Descriptive.ipynb
```

## Contenu du Notebook

Le notebook est organisé en sections correspondant aux questions du TP:

### 1. **Importation des Modules**
   - Configuration de tous les packages nécessaires

### 2. **Chargement des Données**
   - Option 1: Données d'exemple générées automatiquement
   - Option 2: Charger depuis un fichier CSV

### 3. **Question 1: Centralité et Dispersion**
   - Calcul du mode, médiane, moyenne
   - Écart-type, variance, quartiles
   - Boîtes à moustaches (boxplots)
   - Pour les deux variables: Taux de Fertilité et Espérance de vie

### 4. **Question 2: Affichage des Données**
   - Nuage de points (scatter plot)
   - Ajout du point moyen du nuage

### 5. **Question 3: Corrélation Linéaire**
   - Covariance entre X et Y
   - Coefficient de corrélation de Pearson (r)
   - Matrice de corrélation
   - Interprétation statistique

### 6. **Question 4: Régression Linéaire**
   - Calcul de la droite de régression
   - Coefficient de détermination (R²)
   - Visualisation de la droite sur le nuage de points
   - Analyse des résidus

### 7. **Résumé et Conclusions**
   - Synthèse complète de l'analyse

## Packages Utilisés

| Package | Utilisation |
|---------|-------------|
| **numpy** | Calculs numériques et tableaux |
| **pandas** | Manipulation de DataFrames |
| **scipy** | Fonctions statistiques avancées |
| **matplotlib** | Graphiques et visualisations |
| **seaborn** | Visualisations statistiques |
| **scikit-learn** | Régression linéaire |

## Commandes Python Principales

### Charger les données
```python
import pandas as pd
D1 = pd.read_csv('data/stats_data_TP.csv')
```

### Statistiques descriptives
```python
table1['Taux de Fertilité'].mean()      # Moyenne
table1['Taux de Fertilité'].median()    # Médiane
table1['Taux de Fertilité'].std()       # Écart-type
table1['Taux de Fertilité'].describe()  # Résumé complet
```

### Visualisations
```python
import matplotlib.pyplot as plt

# Boxplot
table1.boxplot(column='Taux de Fertilité')

# Scatter plot avec point moyen
plt.scatter(X, Y, marker='+')
plt.scatter(X_mean, Y_mean, marker='o', color='red')
```

### Corrélation
```python
X.corr(Y)                          # Coefficient de corrélation
np.cov(X, Y)                       # Covariance
table1.corr()                      # Matrice de corrélation
```

### Régression Linéaire
```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X.reshape(-1,1), Y)
Y_pred = model.predict(X.reshape(-1,1))
R_squared = model.score(X.reshape(-1,1), Y)
```

## Notes Importantes

1. **Données d'exemple**: Par défaut, le notebook génère des données d'exemple avec une corrélation négative (Espérance de vie vs Taux de Fertilité).

2. **Fichier CSV personnel**: Pour utiliser vos propres données, placez le fichier `stats_data_TP.csv` dans un dossier `data/` et décommentez la ligne appropriée.

3. **Exécution**: Vous pouvez exécuter les cellules dans l'ordre ou individuellement. Les données sont générées une fois et réutilisées.

4. **Modifications**: Vous pouvez modifier les données, les paramètres et les visualisations selon vos besoins.

## Résultats Attendus

Après exécution complète du notebook, vous obtiendrez:

✓ Statistiques descriptives pour chaque variable  
✓ Visualisations (histogrammes, boxplots, scatter plots)  
✓ Coefficient de corrélation et interprétation  
✓ Équation de régression linéaire  
✓ Coefficient R² et analyse des résidus  
✓ Graphique complet avec droite de régression  

## Interprétation des Résultats

### Coefficient de Corrélation (r)
- **r ∈ [-1, -0.8]**: Corrélation négative très forte
- **r ∈ [-0.8, -0.6]**: Corrélation négative forte
- **r ∈ [-0.6, -0.2]**: Corrélation négative modérée
- **r ∈ [-0.2, 0.2]**: Pas de corrélation (ou très faible)
- **r ∈ [0.2, 0.6]**: Corrélation positive modérée
- **r ∈ [0.6, 0.8]**: Corrélation positive forte
- **r ∈ [0.8, 1]**: Corrélation positive très forte

### Coefficient de Détermination (R²)
R² indique le pourcentage de la variance de Y expliquée par X.
- R² = 0.8 → 80% de la variance expliquée (excellent)
- R² = 0.5 → 50% de la variance expliquée (bon)
- R² = 0.2 → 20% de la variance expliquée (faible)

## Troubleshooting

**Problème**: ModuleNotFoundError
```bash
pip install <package_name>
```

**Problème**: Fichier CSV non trouvé
- Assurez-vous que le fichier existe et se trouve dans le chemin `data/stats_data_TP.csv`

**Problème**: Jupyter notebook ne s'ouvre pas
```bash
pip install --upgrade jupyter
jupyter notebook
```

## Auteur du Notebook

Créé pour le cours de Statistique Descriptive - ESI Rabat 2025/2026

## Ressources Supplémentaires

- [Documentation Pandas](https://pandas.pydata.org/docs/)
- [Documentation NumPy](https://numpy.org/doc/)
- [Documentation SciPy](https://docs.scipy.org/)
- [Matplotlib Tutorials](https://matplotlib.org/stable/tutorials/index.html)
- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)

---

**Bon courage! 📊📈**
