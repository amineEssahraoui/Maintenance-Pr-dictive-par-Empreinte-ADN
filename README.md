# Système de Maintenance Prédictive Basé sur l'Empreinte ADN Temporelle des Machines Industrielles

## 0.1 Introduction

L'objectif de ce projet est de **développer un système de maintenance prédictive** pour les machines industrielles en utilisant une approche basée sur l'**empreinte ADN temporelle**. Cette méthode consiste à suivre le comportement d'une machine au fil du temps et à détecter les anomalies avant qu'elles ne provoquent des défaillances majeures.

Le projet se concentre sur la **simulation sous MATLAB**, en implémentant les **algorithmes nécessaires** pour générer les empreintes ADN temporelles et **valider les modèles prédictifs**.

## 0.2 Objectifs du Projet

Les principaux objectifs du projet sont les suivants :
- Développer un **environnement de simulation sous MATLAB** pour simuler le comportement des machines industrielles.
- Implémenter des **algorithmes** pour **générer les empreintes ADN temporelles** des machines.
- **Créer et valider deux modèles prédictifs** :
  - **Modèle complexe** : Une combinaison de **LSTM** (Long Short-Term Memory) et **CNN** (Convolutional Neural Network) pour capturer des dépendances temporelles complexes.
  - **Modèle simplifié** : Une approche **SARIMA-Boosting** (Seasonal AutoRegressive Integrated Moving Average) pour prédire les anomalies.
- Comparer les **résultats obtenus** avec les **méthodes traditionnelles de maintenance prédictive** pour évaluer la performance des modèles.

## Système Robotique - Robot à 6 Bras

Dans ce projet, nous avons choisi de travailler avec un **robot industriel à 6 bras** comme système cible. Ce robot est conçu pour effectuer des tâches complexes nécessitant une grande précision et une flexibilité. Il est utilisé ici comme un modèle pour simuler le comportement des machines industrielles dans un environnement de maintenance prédictive.

### Utilisation dans le Projet

Le robot à 6 bras est simulé dans l'environnement MATLAB afin de reproduire son comportement au fil du temps. Nous suivons l’évolution de plusieurs paramètres critiques, comme la vitesse de rotation, la force appliquée, et l'usure des composants, pour créer les empreintes ADN temporelles. Ces empreintes seront ensuite utilisées pour entraîner et valider nos modèles prédictifs de maintenance.

Nous avons également intégré des données de performance du robot dans le système de simulation afin de détecter des anomalies liées à des dysfonctionnements avant qu'ils ne causent des pannes majeures.
