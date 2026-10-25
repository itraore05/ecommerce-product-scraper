# 🕷️ Scraper E-commerce — Collecte automatisée de données produits (Python)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Requests](https://img.shields.io/badge/Requests-HTTP-2CA5E0?style=flat)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-HTML%20parsing-4B8BBE?style=flat)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

> Système de **web scraping** qui collecte automatiquement les fiches produits d'une **plateforme e-commerce en Côte d'Ivoire** (smartphones et accessoires) et les structure en jeu de données exploitable pour l'analyse et l'IA.
> Réalisé pendant mon stage de Data Analyst (2025), comme première brique d'un projet de solutions d'IA basées sur les tendances du marché e-commerce ivoirien.

---

## 🎯 Objectifs

- Créer un **scraper automatique** pour extraire les données produits d'une plateforme e-commerce ivoirienne
- **Structurer et stocker** les données extraites dans un format exploitable (CSV)
- **Explorer** les données collectées dans des notebooks interactifs
- Constituer une **base de données d'apprentissage** pour un futur projet d'IA

## 🧭 Fonctionnement

```
categories.json  ──▶  Requêtes HTTP + parsing (BeautifulSoup)  ──▶  Structuration (Pandas)  ──▶  smartphones.csv
```

1. **Configuration** : les catégories de produits à collecter sont définies dans `config/categories.json`.
2. **Récupération** : `requests` télécharge les pages catalogue, avec en-têtes navigateur, délais aléatoires et nouvelles tentatives en cas d'erreur.
3. **Extraction** : BeautifulSoup analyse le HTML et récupère pour chaque produit : nom, marque, prix, ancien prix, lien et note.
4. **Structuration** : Pandas nettoie et organise les données, puis les exporte en CSV.
5. **Exploration** : un notebook dédié analyse le jeu de données obtenu.

## 🛠️ Technologies

| Rôle | Outils |
|---|---|
| Langage | Python |
| Requêtes HTTP | requests |
| Parsing HTML | BeautifulSoup, lxml |
| Manipulation de données | pandas |
| Utilitaires | json, os, time |
| Exploration | Jupyter Notebook |

## 📁 Structure du projet

```
ecommerce-product-scraper/
├── config/
│   └── categories.json          # Catégories de produits à collecter
├── data/
│   └── smartphones.csv          # Échantillon de données extraites (106 produits)
├── notebooks/
│   ├── scraping_code.ipynb         # Code du scraper
│   └── extraction_donnees.ipynb    # Extraction et exploration des données
├── documentation/
│   └── Description du Projet.docx  # Présentation détaillée du projet
├── requirements.txt
└── README.md
```

## ▶️ Installation et utilisation

```bash
git clone https://github.com/itraore05/ecommerce-product-scraper.git
cd ecommerce-product-scraper
pip install -r requirements.txt
```

1. Adapter si besoin les catégories dans `config/categories.json`.
2. Ouvrir et exécuter les notebooks du dossier `notebooks/`.

> ⚠️ Projet réalisé à des fins d'analyse et d'apprentissage. Toute collecte doit respecter les conditions d'utilisation du site concerné et rester raisonnable en nombre de requêtes.

## 💡 Compétences démontrées

- Développement de scripts de collecte web robustes (gestion des erreurs, nouvelles tentatives, délais)
- Structuration d'un projet Python reproductible (configuration, données, notebooks, dépendances)
- Manipulation et préparation de données avec pandas
- Compréhension des enjeux de la collecte de données pour l'IA

## 👤 Auteur

**Ismaël Traoré** — Développeur Data & IA
📧 contact.traoreimael@gmail.com · 💼 [LinkedIn](https://www.linkedin.com/in/ismael-traor%C3%A9-m-4007a2225/)
