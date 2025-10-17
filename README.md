
# Prédiction des Pannes d'Éclairage Public

## Contexte

L'éclairage public est un élément clé du confort, de la sécurité et de la durabilité des villes. Cependant, la maintenance repose souvent sur des signalements manuels ou des interventions tardives, entraînant des pannes non détectées, des coûts élevés et une surconsommation d'énergie.

Ce projet utilise l'analyse des données issues de capteurs (température, tension, luminosité, consommation, etc.) et des historiques de maintenance pour concevoir un modèle de Machine Learning. Ce modèle prédit les pannes et optimise la maintenance de l'éclairage public.

## Public concerné

* **Collectivités locales** chargées de la maintenance des infrastructures.
* **Citoyens** impactés par des zones non éclairées et l'insécurité.
* **Entreprises de maintenance** recherchant un gain économique et logistique.
* **Acteurs de la transition énergétique** cherchant à promouvoir un éclairage plus durable.

## Problématique

L'absence d'un système prédictif entraîne une gestion réactive et coûteuse :

* Délais d'intervention allongés
* Surcoûts de maintenance
* Diminution de la sécurité publique
* Surconsommation d'énergie
* Perte de confiance des citoyens

L'objectif de ce projet est de répondre à la question suivante :

**Comment anticiper les pannes des lampadaires grâce à l’analyse et la modélisation de données, afin d’optimiser la maintenance et garantir un éclairage fiable et durable ?**

## Fonctionnalités

* **Prédiction des pannes** : Utilisation de modèles de Machine Learning pour prédire les défaillances des équipements.
* **Optimisation de la maintenance** : En fonction des prédictions, ajustement des plannings de maintenance pour minimiser les coûts.
* **Suivi en temps réel** : Collecte et analyse des données des capteurs (température, tension, luminosité, etc.) pour anticiper les problèmes.
* **Rapports et alertes** : Génération de rapports détaillés et alertes automatiques en cas de panne détectée.

## Installation

### Prérequis

Assurez-vous que vous avez **Python 3.7+** installé sur votre machine. Vous pouvez vérifier cela en exécutant :

```bash
python --version
```

### Étapes d'installation

1. Clonez ce dépôt sur votre machine locale :

   ```bash
   git clone https://github.com/tonutilisateur/Hackathon-October.git
   ```

2. Accédez au répertoire du projet :

   ```bash
   cd Hackathon-October
   ```

3. Créez et activez un environnement virtuel (optionnel mais recommandé) :

   * Sur macOS/Linux :

     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```
   * Sur Windows :

     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```

4. Installez les dépendances requises via `pip` :

   ```bash
   pip install -r requirements.txt
   ```

### Dépendances

Le projet utilise les bibliothèques suivantes :

* **pandas** : pour le traitement des données.
* **numpy** : pour les calculs numériques.
* **matplotlib** : pour la visualisation des données.
* **scikit-learn** : pour l'implémentation du modèle de Machine Learning.
* **tensorflow** (si vous utilisez des réseaux neuronaux) ou toute autre bibliothèque de ML comme **XGBoost**, **LightGBM**, etc.

Vous pouvez installer toutes ces dépendances avec la commande ci-dessus, après avoir configuré votre environnement.

## Étapes du projet

### 1. Collecte des données

Les données collectées comprennent :

* Température
* Tension
* Luminosité
* Consommation d'énergie
* Historique des maintenances

### 2. Prétraitement des données

Les données sont nettoyées et mises en forme pour être utilisées dans le modèle de Machine Learning. Cela inclut :

* Le retrait des valeurs manquantes
* La normalisation des données
* La gestion des valeurs aberrantes

### 3. Construction du modèle prédictif

Nous utilisons un modèle de Machine Learning (par exemple, régression linéaire, forêt aléatoire ou réseaux neuronaux) pour prédire les pannes d'éclairage public à partir des données collectées.

### 4. Évaluation du modèle

Le modèle est évalué en utilisant des métriques classiques telles que l'exactitude (accuracy), la précision (precision), le rappel (recall) et la courbe ROC. Nous ajustons les hyperparamètres pour améliorer la performance.

### 5. Génération des alertes et rapports

Le modèle fournit des alertes automatiques lorsqu'une panne est probable et génère des rapports sur les prédictions et les recommandations de maintenance.

## Instructions d'exécution

1. **Entraîner le modèle** : Pour entraîner le modèle de prédiction des pannes, exécutez le script principal :

   ```bash
   python script/train_model.py
   ```

2. **Faire des prédictions** : Une fois le modèle entraîné, vous pouvez l'utiliser pour faire des prédictions sur les nouvelles données collectées en exécutant :

   ```bash
   python script/predict_failures.py
   ```

3. **Visualisation des résultats** : Vous pouvez également visualiser les résultats de l'analyse en exécutant le script suivant :

   ```bash
   python script/visualize_results.py
   ```

### Résultats attendus

Après l'exécution du code, vous obtiendrez :

* **Prédictions des pannes** : Le modèle renverra une estimation de la probabilité qu'un lampadaire tombe en panne dans un délai donné.
* **Optimisation de la maintenance** : Un plan de maintenance plus précis sera généré, permettant une allocation plus efficace des ressources.
* **Rapports et alertes** : Vous recevrez des alertes en temps réel et des rapports détaillant les pannes prédites et les actions recommandées.

## Visualisation des résultats

Voici quelques visualisations basées sur les données traitées et les résultats obtenus par les modèles de Machine Learning.

### 1. **Matrice de Corrélation**

Ce graphique montre la corrélation entre les différentes variables, y compris la corrélation avec le **type de panne**.

![Matrice de Corrélation](chemin/vers/image/correlation_matrix.png)

### 2. **Répartition des Types de Pannes**

Un graphique montrant la distribution des différents types de pannes dans les données collectées.

![Distribution des Types de Pannes](chemin/vers/image/fault_types_distribution.png)

### 3. **Fluctuations de Courant (Ampères) vs Type de Panne**

Ce graphique montre la relation entre les fluctuations de courant et les types de pannes. Il peut aider à identifier les caractéristiques électriques associées aux pannes.

![Fluctuations de Courant vs Type de Panne](chemin/vers/image/current_vs_fault.png)

### 4. **Température vs Type de Panne**

Graphique qui illustre la variation de la température en fonction des différents types de panne.

![Température vs Type de Panne](chemin/vers/image/temperature_vs_fault.png)

### 5. **Résultats des Modèles de Machine Learning**

#### Random Forest

Le modèle **Random Forest** a obtenu une **précision de 85%** sur les prédictions des pannes. Voici les résultats de l'évaluation :

```
Accuracy: 0.85
Confusion Matrix:
[[4841   0   0   0   2]
[  78 2535  20  0   0]
[ 160  0   93   1   0]
[ 570  0   0  939  0]
[ 220  0   0   0  488]]

Classification Report:
precision    recall  f1-score   support
0      0.82   1.00   0.90      4863
1      1.00   0.75   0.86       313
2      1.00   0.49   0.66       315
3      3.80   0.14   0.24       663
4      1.00   0.69   0.81       708
```

#### Régression Logistique

Le modèle de **régression logistique** a donné une **précision de 83%**, mais avec des résultats légèrement moins bons que le modèle Random Forest. Voici les résultats :

```
Accuracy: 0.83
Confusion Matrix:
[[4853   0   0   0   0]
[  23 2534   0   0   0]
[  78   0  315   0   0]
[ 575   0   0  663  0]]
```

### 6. **Prédictions Manuelles**

Voici des exemples de prédictions manuelles basées sur des valeurs spécifiques :

- **Exemple 1** :  
  `power_consumption (Watts) = 48.423`, `voltage_levels (Volts) = 218.93`, etc.  
  **Prédiction** : Panne de type 4.

- **Exemple 2** :  
  `power_consumption (Watts) = 157.14`, `voltage_levels (Volts) = 228.39`, etc.  
  **Prédiction** : Panne de type 1.

### 7. **Exportation des Résultats**

Les résultats ont été exportés dans un fichier CSV pour une utilisation future, notamment dans Power BI. Le fichier exporté contient les colonnes suivantes :  
- **power_consumption**  
- **voltage_levels**  
- **predicted_hours_remaining**  
- **predicted_failure_date**  
- **urgency**  

Exemple de sortie dans le fichier CSV :

```
bulb_number,timestamp,power_consumption (Watts),voltage_levels (Volts),current_fluctuations (Amperes),predicted_hours_remaining,predicted_failure_date,urgency
1,2023-12-27 06:32:12,98.65,219.99,3.35,65.666823,2023-12-30 00:12:08.963333333,Moyen
...
```

---

# Download the README file
readme_path = '/mnt/data/prediction_pannes_eclairage_public_README.txt'

# Write the content into a text file
with open(readme_path, 'w', encoding='utf-8') as f:
    f.write(readme_content)

readme_path
