# Projet MTCook - Template Cookiecutter pour le Machine Learning
📝 Présentation du projet
Dans le cadre de mon cours de Big Data et Infrastructure Machine Learning, j'ai réalisé ce projet qui consiste à créer un template Cookiecutter standardisé.

L'objectif est de fournir une structure de projet prête à l'emploi pour le Machine Learning, garantissant que chaque nouveau projet commence avec les bonnes pratiques : dossier de données organisé, tests unitaires, et formatage de code automatique.

---
## À propos du projet

Ce dépôt fait partie du cours **Big Data and Business Intelligence (BIDABI)**.  
Il a pour objectif d’initier les étudiants au travail avec du code open‑source et à l’adaptation de projets
existants dans une structure professionnelle.

🛠️ Structure du Projet
Mon template génère automatiquement l'arborescence suivante :

data/ : Stockage des données brutes (raw) et transformées (processed).

models/ : Emplacement pour les modèles entraînés.

notebooks/ : Pour l'exploration de données.

src/ : Le code source du pipeline (nettoyage, traduction, évaluation).

tests/ : Mes tests unitaires avec pytest.

pyproject.toml : Gestion des dépendances et configuration des outils.

---
## 🚀 Installation et Utilisation
1. Prérequis
J'utilise Python 3.10+. Il est recommandé de créer un environnement virtuel Bash :
python -m venv .venv
source .venv/Scripts/activate  # Sur Windows: .venv\Scripts\activate
2. Installation des dépendances
J'ai configuré le projet pour qu'il s'installe facilement avec les outils nécessaires :
pip install -r requirements.txt
# Ou si vous utilisez le pyproject.toml
pip install .
3. Lancer le pipeline
Le cœur de mon projet contient un pipeline de traitement de texte (traduction et évaluation). Pour exécuter la logique principale :
python src/main.py

---
## 🧪 Qualité et Tests
Pour garantir la fiabilité de mon code, j'ai intégré deux outils essentiels que j'utilise lors du développement :

Tests : Pour vérifier que mes fonctions de calcul de score (BLEU, chrF) fonctionnent :
pytest
Formatage : Pour garder un code propre et lisible selon la norme PEP8 :
black .


---

## 📁 Structure du projet
```
project/
│
├── data/                # Input data (CSV, JSON, etc.)
│   ├── sample.json
│   ├── sample02.json
│   └── big.csv
│
├── output/              # Generated outputs
│
├── src/
│   ├── loaders/         # Data loading modules
│   ├── translators/     # HuggingFace translation models
│   ├── processors/      # Optional text processing steps
│   ├── evaluators/      # Evaluation metrics (BLEU, etc.)
│   └── orchestrator/    # Main pipeline controller
│       └── orchestrator.py
│
├── tests/               # unit tests
└── main.py              # Entry point for running the pipeline
└── main01.py            # For test
└── main02.py            # For test
└── config.py 
```

---

## 🎓 Objectifs Pédagogiques
Ce projet m'a permis de valider plusieurs compétences :

Automatisation : Création de scripts de pré/post génération (hooks).

Modularité : Séparation de la logique de traitement et de la structure du projet.

CI/CD : Mise en place d'un workflow GitHub Actions pour tester automatiquement le code à chaque envoi.

Réalisé par : Fanny – Étudiante en Master Big Data