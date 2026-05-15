# 🚇 Prévision du trafic urbain — Analyse des événements réels (France 2024)

## 📌 Overview

Ce projet vise à **modéliser et prévoir le trafic urbain** (validations de transport) en intégrant l’impact des **événements réels** :

- 🏖 Vacances scolaires (Zone C — Île-de-France)
- 🎉 Jours fériés officiels
- ✊ Grèves (SNCF / RATP)
- 📅 Événements majeurs
- 📆 Effets calendaires (week-end, jour de la semaine)

👉 Objectif : améliorer la précision des modèles de séries temporelles en enrichissant les données avec du **contexte réel métier**.

---

## 🧠 Méthodologie

### 1. Data Cleaning & Préparation

- Suppression des doublons
- Interpolation des valeurs manquantes
- Détection des outliers (IQR)

---

### 2. Feature Engineering

- Jours fériés (`holidays`)
- Vacances scolaires Zone C
- Grèves
- Variables temporelles :
  - lag_1, lag_7
  - rolling mean 7 jours
  - jour semaine
  - week-end

---

### 3. Analyse d’impact

| Événement | Impact |
|----------|--------|
| Week-end | 🔻 baisse |
| Jour férié | 🔻 baisse |
| Grève | 🔻 forte baisse |
| Vacances | 🔻 baisse |

---

### 4. Modèles

- Naive
- Seasonal Naive
- SARIMA
- Régression Linéaire

---

### 5. Évaluation

- MAE
- RMSE
- MAPE

---

## 📈 Résultats

✔ Les données enrichies améliorent les performances  
✔ Les événements réels sont critiques pour la prédiction  

---

## 📊 Visualisations

- Série temporelle annotée
- Boxplots d’impact
- Comparaison réel vs prédiction
- Importance des variables

---

## ⚙️ Installation

```bash
pip install pandas numpy matplotlib scikit-learn statsmodels holidays