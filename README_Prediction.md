
# 📈 Analyse Prédictive - Ventes de Cigarettes

Ce projet présente une analyse prédictive basée sur un modèle de régression linéaire visant à estimer le **chiffre d'affaires** en fonction de :

- La région
- Le canal de vente
- Le produit
- La quantité vendue

## 📊 Données utilisées

Le modèle est entraîné sur un jeu de données synthétique contenant :
- 120 lignes de ventes
- 5 régions, 3 canaux, 3 produits
- Des ventes mensuelles

## 🔧 Modèle

Un pipeline sklearn a été utilisé :

- **Encodage** des variables catégorielles (`Région`, `Canal`, `Produit`)
- **Régression linéaire** pour la prédiction
- **Score R² sur données test** : 0.44

## 📂 Fichiers

- `modele_pred_ventes.joblib` : modèle entraîné à réutiliser
- `ventes_cigarettes_modifie.xlsx` : base de données utilisée

## ▶️ Exemple d'utilisation

```python
import joblib
import pandas as pd

modele = joblib.load("modele_pred_ventes.joblib")

exemple = pd.DataFrame({
    'Région': ['Nord'],
    'Canal': ['Revendeur'],
    'Produit': ['Cigarette A'],
    'Quantité_vendue': [300]
})

prediction = modele.predict(exemple)
print(f"Prévision du chiffre d'affaires : {prediction[0]:.2f} DA")
```
