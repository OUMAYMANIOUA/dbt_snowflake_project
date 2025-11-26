# 🚀 Projet Data Engineering de A à Z : dbt, Snowflake & Apache Airflow


### 📌 Présentation

Ce projet met en place un pipeline complet de data engineering utilisant :

dbt pour la transformation des données

Snowflake comme data warehouse cloud

Apache Airflow pour l’orchestration et la planification

Python pour l’automatisation

Il couvre l’ingestion, la transformation, les tests, la modélisation et la mise en production.

---

### 🧰 Technologies Utilisées

Snowflake – Cloud Data Warehouse

dbt Core – Transformation SQL & tests

Apache Airflow – Orchestration

Python – Scripts

Git – Version control

---

### 📁 Structure du Projet

snowflake_data_project/

│── models/

│     ├── staging/

│     ├── intermediate/

│     └── marts/

│── dags/

│── logs/

│── seeds/

│── macros/

│── dbt_project.yml

│── requirements.txt

│── README.md

---

### ⚙️ Installation & Configuration
1️⃣ Cloner le Dépôt
git clone https://github.com/OUMAYMANIOUA/dbt_snowflake_project.git

cd your-project

2️⃣ Créer un Environnement Virtuel
python -m venv venv


Activer l’environnement :

venv\Scripts\activate

3️⃣ Installer les Dépendances

pip install -r requirements.txt

4️⃣ Configurer dbt pour Snowflake

Ajouter ceci dans ~/.dbt/profiles.yml :

snowflake_project:
```yaml
  outputs:
    dev:
      type: snowflake
      account: votre_compte_snowflake
      user: dbt_user
      password: votre_mot_de_passe
      role: ACCOUNTADMIN
      database: finance_db
      warehouse: finance_wh
      schema: raw
  target: dev
```
---

### 🏗️ Exécution des Modèles dbt

Lancer les transformations

dbt run

Lancer les tests
dbt test

Générer la documentation
dbt docs generate
dbt docs serve

---

###⏱️ Démarrer Apache Airflow
airflow standalone


Interface Web :
👉 http://localhost:8080

Airflow détecte automatiquement les DAGs dans le dossier dags/.

---

🔄 Workflow Global

Ingestion des données vers Snowflake

Modèles staging

Modèles intermediate

Modèles marts (fact & dimension)

Tests dbt

Orchestration Airflow

---

### 📚 Commandes Utiles
dbt
dbt run
dbt test
dbt seed
dbt docs generate

Airflow
airflow webserver
airflow scheduler
airflow dags list
airflow tasks list <dag_id>
