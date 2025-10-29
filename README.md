# 🎓 Prédiction des Performances des Étudiants — Régression Multiple

## 📘 Description du Projet
Ce projet vise à **analyser les facteurs influençant la performance scolaire des étudiants** et à **prédire leurs résultats finaux** à l’aide de plusieurs modèles de régression supervisée.  
L’objectif est d’identifier les variables les plus déterminantes pour la réussite académique et d’utiliser ces informations pour anticiper les performances futures.

---

## 🎯 Objectifs du Projet
- Identifier les variables ayant le plus grand impact sur la réussite scolaire.  
- Construire et comparer plusieurs modèles de régression pour prédire la performance.  
- Visualiser et interpréter les résultats à l’aide de graphiques et d’analyses statistiques.

---

## 🧠 Problématique de Régression
**Question principale :**  
> Quels sont les facteurs clés influençant les performances scolaires des étudiants, et comment peuvent-ils être utilisés pour prédire leurs résultats finaux ?

---

## 📊 Jeu de Données
**Fichier :** `Student_Performance.csv`  
**Taille :** 9873 lignes × 6 colonnes  

| Variable | Description |
|-----------|-------------|
| Hours Studied | Nombre d'heures d’étude par jour |
| Previous Scores | Notes précédentes |
| Extracurricular Activities | Participation à des activités extrascolaires (Yes/No) |
| Sleep Hours | Heures de sommeil |
| Sample Question Papers Practiced | Nombre d’examens d’entraînement pratiqués |
| Performance Index | Note finale (variable cible) |

---

## ⚙️ Prétraitement des Données
- **Suppression des doublons** → 127 lignes supprimées  
- **Encodage des variables catégorielles** (`Extracurricular Activities` → `activities`)  
- **Détection et suppression des valeurs aberrantes** à l’aide du **Z-score**  
- **Analyse de la distribution** des variables et de leur **corrélation** avec la cible  

📊 **Exemples de visualisations :**
- Heatmap des corrélations  
- Boxplots et distributions  
- Pairplot entre les variables  

---

## 🧩 Modèles Utilisés

| Modèle | R² Score | MAE |
|--------|-----------|------|
| Linear Regression | 0.9880 | 1.66 |
| Ridge Regression | 0.9880 | 1.66 |
| Lasso Regression | 0.9860 | 1.80 |
| Decision Tree Regressor | 0.9739 | 2.46 |
| Random Forest Regressor | 0.9840 | 1.93 |
| Gradient Boosting Regressor | 0.9873 | 1.71 |
| SVR | 0.9847 | 1.87 |
| KNN Regressor | 0.9831 | 1.99 |
| XGBoost Regressor | 0.9857 | 1.81 |

📈 **Meilleur modèle : Random Forest Regressor**

---

## 🔍 Validation et Optimisation

### 🔸 Validation croisée (Cross-Validation)
| Modèle | R² moyen |
|---------|-----------|
| Ridge Regression | 0.9888 |
| Lasso Regression | 0.9887 |
| Random Forest | 0.9850 |

### 🔸 Optimisation via GridSearchCV
**Paramètres optimaux trouvés :**
```python
{'max_depth': 10, 'min_samples_split': 10, 'n_estimators': 150}
```

### 🔸 Résultats après optimisation :
- **R² optimisé :** 0.9859  
- **MAE optimisé :** 1.8166  

---

## 🧮 Réduction de Dimensionnalité (PCA)
| Composante | Variance expliquée |
|-------------|-------------------|
| PC1 | 94.34% |
| PC2 | 2.56% |
| PC3 | 2.11% |
| PC4 | 0.90% |
| PC5 | 0.07% |

📈 Le modèle **Random Forest + PCA** obtient :
- **R² :** 0.9847  
- **MAE :** 1.9006  

---

## 📉 Visualisations des Résultats
- **Comparaison des Modèles** (Barres des scores R² et MAE)  
- **Courbe d’Apprentissage** (Random Forest Regressor)  
- **Distribution des Résidus**  
- **Résidus vs Prédictions**

---

## 🧾 Bibliothèques Utilisées
- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn**
- **xgboost**

---

## 👨‍💻 Auteur

**Adam Serghini**  
Ingénieur passionné par la **Data Science** et l’**Intelligence Artificielle**.  
Titulaire d’un **Master 2 en Intelligence Artificielle (IA)**.  


📧 [LinkedIn](https://www.linkedin.com/in/adam-serghini-767b47273)

---

## 📚 Licence
Ce projet est sous **licence MIT** — libre à l’utilisation, la modification et la diffusion.
