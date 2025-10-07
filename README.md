# 📊 Revenue Analytics Project

## 🧩 Présentation

Ce projet a été conçu pour construire un modèle de données analytique à partir des données brutes présentes dans le schéma `L1_LANDING` de Snowflake, afin de permettre une visualisation intuitive des revenus par client via **Power BI**.

Les étapes clés comprennent :

- La transformation des données brutes à l’aide de **dbt Cloud**
- La modélisation de vues et de tables intermédiaires et finales
- La création d’un modèle de revenus par client
- La visualisation de ces données via un **dashboard Power BI** orienté métier

---

## 🏗️ Architecture technique

### Données sources :
- Stockées dans **Snowflake**, schéma `L1_LANDING`
- Composées de données brutes issues des systèmes transactionnels

### Transformation :
- Réalisée avec **dbt Cloud**
- Modèles créés :
  - `stg_...` : staging des tables brutes avec faible transformation
  - `orders_fact` : table intermédiaire pour nettoyage et enrichissement
  - `customerrevenue` : table sur les revenus par client

### Visualisation :
- Réalisée avec **Power BI**
- Connexion via ODBC à Snowflake
- Dashboard interactif pour les utilisateurs métier (revenu, tendances, comparaison client, etc.)

---
📈 Dashboard Power BI

Le dashboard Power BI permet aux utilisateurs non techniques de :
- Visualiser les revenus par client
- Identifier les clients à forte valeur
- Suivre les évolutions de revenu dans le temps
- Comparer les performances par segment de client

🧠 À retenir

- dbt permet une gestion versionnée et testée des transformations de données
- Snowflake joue le rôle de Data Warehouse central
- Power BI fournit une interface intuitive pour l’exploration des données

✍️ Auteur

Projet réalisé par : BENFLS
Date : Octobre 2025
