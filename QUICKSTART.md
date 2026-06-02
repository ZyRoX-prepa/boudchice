# 🚀 Quick Start Guide - Jupyter Notebook Setup

## En 5 minutes

### 1. Installation
```bash
pip install -r requirements.txt
```

### 2. Lancer Jupyter
```bash
jupyter notebook
```

### 3. Ouvrir le notebook
Naviguez vers `TP_Statistique_Descriptive.ipynb` et cliquez sur celui-ci.

### 4. Exécuter les cellules
- Cliquez sur une cellule
- Pressez `Ctrl+Enter` pour exécuter

---

## Structure du Notebook

```
📚 TP: Introduction à l'analyse statistique bivariée
├── 1️⃣  Imports - Tous les packages nécessaires
├── 2️⃣  Données - Génération ou chargement
├── 3️⃣  Préparation - Nettoyage des données
├── ❓ Question 1 - Centralité et Dispersion
│   ├── Taux de Fertilité
│   ├── Espérance de vie
│   └── Boxplots
├── ❓ Question 2 - Nuage de Points
│   └── Avec point moyen
├── ❓ Question 3 - Corrélation
│   ├── Covariance
│   ├── Coefficient r
│   └── Matrice de corrélation
├── ❓ Question 4 - Régression
│   ├── Droite de régression
│   ├── Coefficient R²
│   └── Analyse des résidus
└── 📊 Résumé - Synthèse complète
```

---

## Exemples de Sortie

### Question 1 - Statistiques
```
Moyenne: 2.84
Médiane: 2.65
Mode: 2.31
Écart-type: 1.23
```

### Question 3 - Corrélation
```
r = -0.8932  (Corrélation négative très forte)
p-value = 0.000001
```

### Question 4 - Régression
```
Équation: Y = 8.52 - 0.045*X
R² = 0.7979 (79.79% expliqué)
```

---

## Commandes Utiles dans Jupyter

| Raccourci | Action |
|-----------|--------|
| `Ctrl+Enter` | Exécuter la cellule |
| `Shift+Enter` | Exécuter et passer à la suivante |
| `Alt+Enter` | Exécuter et insérer une cellule |
| `Ctrl+/` | Commenter/Décommenter |
| `Tab` | Autocomplétion |
| `Shift+Tab` | Afficher la documentation |

---

## Support Fichier CSV Personnel

Pour utiliser vos propres données:

1. Placez le fichier dans `data/stats_data_TP.csv`
2. Assurez-vous qu'il contient les colonnes:
   - `An` (année)
   - `taux fert` (taux de fertilité)
   - `esp vie` (espérance de vie)
3. Décommentez cette ligne dans le notebook:
   ```python
   # D1 = pd.read_csv('data/stats_data_TP.csv')
   ```

---

## Visualisations Générées

Le notebook crée automatiquement:

📊 **Boxplots** - Distribution des variables  
🔵 **Scatter plots** - Nuage de points  
📈 **Regression line** - Droite de régression  
🔴 **Residual plots** - Analyse des résidus  
🔗 **Correlation heatmap** - Matrice de corrélation  

---

## Paramètres Personnalisables

Vous pouvez modifier:

```python
# Nombre d'échantillons
n_samples = 50

# Seed pour reproductibilité
np.random.seed(42)

# Taille des figures
plt.rcParams['figure.figsize'] = (10, 6)

# Nombre de bins pour l'histogramme
plt.hist(residuals, bins=15)
```

---

## 📚 Ressources

- [Jupyter Shortcuts](https://jupyter-notebook.readthedocs.io/)
- [Pandas Cheatsheet](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)
- [Matplotlib Gallery](https://matplotlib.org/gallery.html)

---

**Besoin d'aide?** Consultez le README.md complet pour plus de détails! 📖
