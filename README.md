# Sigma‑RUL

**Sigma‑RUL** est un projet de maintenance prédictive industrielle conçu pour anticiper les défaillances des composants robotiques en analysant leurs signatures numériques en temps réel. Il exploite les technologies de **vision par ordinateur**, **deep learning**, et **détection d’anomalies**, et s’adresse aux ingénieurs, techniciens et opérateurs industriels.

## 🚀 Objectifs du projet

- 📥 **Collecter** des séries temporelles à partir de robots et capteurs simulés dans **RoboDK**
- 🧠 **Extraire** et **reconstruire** les signatures normales avec des autoencodeurs **LSTM**
- ⚠️ **Détecter** les anomalies à l’aide de **Isolation Forest**
- 🔮 **Prédire** l’évolution future des signatures pour anticiper les dégradations
- 📉 **Estimer** le **Remaining Useful Life (RUL)** via une approche probabiliste
- 🌐 **Déployer** une interface **Streamlit** pour la visualisation et l’interaction en temps réel

## 🔧 Pipeline du projet

1. **Ingestion des données**  
   - Récupération des positions, vitesses et charges via l’API RoboDK  
   - Stockage au format `.csv` ou `.parquet`

2. **Prétraitement et Feature Engineering**  
   - Nettoyage, normalisation, et glissement temporel (`rolling window`)  
   - Construction des signatures et extraction des caractéristiques

3. **Modélisation**  
   - Autoencodeur LSTM pour la reconstruction  
   - Détection des anomalies avec Isolation Forest  
   - Deuxième autoencodeur LSTM (sorties : reconstruction + prédiction)

4. **Estimation du RUL**  
   - Fusion des erreurs (reconstruction + prédiction)  
   - Estimation du RUL via un **Processus Gaussien**

5. **Déploiement**  
   - Interface **Streamlit** interactive  
   - Visualisation des scores d’anomalie et du RUL  
   - Contrôle des seuils et exportation des rapports

## 📸 Aperçu de l’interface

![Streamlit Sigma-RUL Interface](./_static/pipeline.svg)

## 📂 Structure du projet

```bash
Sigma-RUL/
├── data/               # Données simulées (séries temporelles)
├── models/             # Modèles entraînés (autoencodeurs, etc.)
├── app/                # Code de l'application Streamlit
├── notebooks/          # Explorations et visualisations
├── src/                # Modules Python (prétraitement, modélisation, etc.)
├── _static/            # Images et fichiers statiques
└── README.md           # Présentation du projet

⚙️ Technologies utilisées

🧠 Deep Learning : PyTorch, LSTM Autoencoders

📊 Time Series & Signal Processing

🤖 Simulation : RoboDK

🌐 Interface utilisateur : Streamlit
