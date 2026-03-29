# Projet d'Analyse des Ventes Restaurant (2022-2023)

Ce projet documente le cycle complet de traitement et d'analyse des données d'un restaurant : du nettoyage d'un dataset brut jusqu'à l'analyse stratégique des performances commerciales.

---

##  Objectifs

- Nettoyer et fiabiliser les données de ventes brutes.  
- Identifier les tendances de consommation sur deux ans.  
- Comprendre les causes des variations du chiffre d'affaires pour proposer des recommandations stratégiques.

---

##  Structure des Fichiers

### 1. Données (Datasets)
- `restaurant_data.csv` : Dataset brut contenant 17 534 transactions avec des valeurs manquantes, des colonnes en anglais et des dates non standardisées.  
- `restaurant_data_clean.csv` : Dataset final après nettoyage. Colonnes renommées en français, types corrigés et colonnes temporelles ajoutées.

### 2. Notebooks (Code)
- `nettoyage.ipynb` : Pipeline de préparation des données  
  - Traduction des variables (`Order ID → ID Commande`)  
  - Gestion des valeurs nulles (remplissage ou suppression)  
  - Extraction de caractéristiques : Année, Mois, Jour de la semaine, Numéro de semaine  

- `Analyse_complete.ipynb` : Analyse exploratoire et visuelle  
  - Analyse de la saisonnalité  
  - Performance par catégorie de produits  
  - Focus sur les produits spécifiques (Top performeurs vs produits en baisse)  

---

##  Aperçu du Dataset Final

Le fichier `restaurant_data_clean.csv` contient les informations suivantes :  

- **Temporel** : Date, Année, Mois, Jour, Numéro de Semaine  
- **Produits** : Catégorie (Plats, Entrées, Boissons…), Type (Nom du produit), Prix, Quantité  
- **Transaction** : Total Commande, Méthode de Paiement (Cash, Carte, Digital)  

---

##  Principaux Enseignements

- **Stabilité des Plats Végétariens** : Le *Vegetarian Platter* reste constant, voire en hausse en 2023.  
- **Produits à surveiller** : Les *Onion Rings* et *Nachos Grande* montrent une instabilité, possiblement due à la saisonnalité ou à des ruptures de stock (notamment mai et octobre).  
- **Répartition du chiffre d'affaires** : Le CA est bien réparti entre les catégories, évitant la dépendance à un seul produit "star".  
- **Périodes critiques** : Certaines périodes comme janvier, juin et octobre ont contribué à la baisse du CA, suggérant des variations saisonnières ou des événements particuliers.

---

##  Installation et Reproduction

1. Installer les dépendances :  
```bash
pip install pandas matplotlib seaborn