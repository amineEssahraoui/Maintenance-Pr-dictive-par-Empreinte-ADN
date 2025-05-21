---

# 🤖 Sigma – Maintenance Prédictive Assistée par IA

**Sigma** est une solution intelligente de maintenance prédictive conçue pour **surveiller l’état de santé des systèmes robotiques industriels** à partir de leurs **signatures numériques**.
En combinant **Deep Learning**, **séries temporelles** et **détection d’anomalies**, Sigma permet de **détecter les comportements anormaux** en temps réel, avant qu'une panne ne survienne.

🎯 Destiné aux **ingénieurs de maintenance**, **techniciens**, et **opérateurs industriels**, Sigma s’intègre facilement dans des environnements simulés via **RoboDK**.

---

## 🚀 Objectifs Clés

* 📡 **Collecter** des séries temporelles issues de robots, convoyeurs et rails simulés dans **RoboDK**
* 🧬 **Modéliser** le comportement normal à l’aide d’**autoencodeurs LSTM**
* 🚨 **Détecter** les anomalies de manière non supervisée avec **Isolation Forest**
* 📈 **Suivre** l’évolution de la signature d’un système en continu
* 🖥️ **Visualiser** dynamiquement les anomalies via une interface **Streamlit**

---

## 🔧 Pipeline Global

### 1. Ingestion des données

* Extraction en temps réel via **RoboDK API**
* Positions, vitesses, charges moteur, etc.
* Export au format `.csv` 

### 2. Prétraitement

* Nettoyage, normalisation
* Application de **fenêtres glissantes** (`rolling windows`)
* Construction des **signatures numériques**

### 3. Modélisation IA

* **Autoencodeur LSTM** pour apprendre la structure normale du comportement
* **Isolation Forest** pour détecter les écarts
* Reconstruction + scoring d’anomalies

### 4. Interface Utilisateur

* Application **Streamlit** pour :

  * Visualisation des anomalies dans le temps
  * Contrôle des seuils
  * Export des rapports

---

## 🖼️ Interface de Surveillance

![Streamlit Sigma Interface](./_static/pipeline.svg)

---

## 📂 Arborescence du projet

```bash
Sigma/
├── data/           # Données simulées (robots, convoyeurs, rails)
├── models/         # Modèles entraînés (LSTM, Isolation Forest)
├── app/            # Interface utilisateur Streamlit
├── notebooks/      # Analyses et visualisations
├── src/            # Modules IA (prétraitement, détection, etc.)
├── _static/        # Ressources visuelles
└── README.md       # Présentation du projet
```

---

## ⚙️ Technologies

| Domaine                 | Outils clés                   |
| ----------------------- | ----------------------------- |
| Deep Learning           | PyTorch, LSTM Autoencoders    |
| Anomalie non supervisée | Isolation Forest              |
| Time Series & Signal    | Pandas, NumPy, Rolling Window |
| Simulation              | RoboDK                        |
| Interface               | Streamlit                     |

---

## ▶️ Démarrage rapide

```bash
# Cloner le dépôt
git clone https://github.com/<votre-utilisateur>/Sigma.git
cd Sigma

# Installer les dépendances
pip install -r requirements.txt

# Lancer l’application
streamlit run app/main.py
```

---

## 🏁 Pourquoi choisir Sigma ?

* 🧠 **Intelligence embarquée** : modélisation du comportement sans supervision
* ⚠️ **Réactivité** : détection précoce de dérives
* 📊 **Visualisation claire** : interface intuitive en temps réel
* 🔧 **Facilité d’intégration** : simulation basée sur RoboDK, compatible avec d'autres plateformes

---


