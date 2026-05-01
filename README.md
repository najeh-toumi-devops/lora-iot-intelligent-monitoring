# 🚀 LoRa IoT Intelligent Monitoring & RL Optimization

## 📌 Description

Ce projet implémente une **plateforme intelligente de monitoring et d’optimisation pour réseaux IoT LoRaWAN**, combinant :

* 📡 Supervision des métriques réseau
* 🤖 Machine Learning & Reinforcement Learning
* ⚡ Optimisation dynamique des paramètres radio (SF, TP)
* 📊 Simulation réaliste et validation sans matériel

L’objectif est de dépasser les limites de l’algorithme ADR standard en utilisant un agent RL adaptatif.

---

## 🎯 Objectifs du projet

* Monitorer les performances d’un réseau LoRaWAN
* Simuler un canal radio réaliste
* Développer un agent RL pour optimiser :

  * Spreading Factor (SF)
  * Transmission Power (TP)
* Comparer les performances avec ADR
* Exposer une API de prédiction en temps réel

---

## 🧠 Architecture du projet

```
lora-iot-intelligent-monitoring/
│
├── env/              # Environnement de simulation LoRa
├── rl/               # Agent RL (Q-learning / DQN)
├── baseline/         # Implémentation ADR
├── data/             # Datasets simulés
├── scenarios/        # Scénarios de test
├── api/              # API FastAPI
├── monitoring/       # Scripts collecte métriques
├── results/          # Résultats & visualisations
├── docs/             # Documentation
├── tests/            # Tests unitaires
│
├── requirements.txt
├── docker-compose.yml
└── README.md
```

---

## ⚙️ Stack technique

* Python 3.10+
* Gymnasium (simulation RL)
* Stable-Baselines3 (DQN)
* FastAPI (API REST)
* NumPy / Pandas / Matplotlib
* Docker & Docker Compose

---

## 🧪 Fonctionnalités principales

### 🔹 Simulation LoRa

* Canal radio réaliste (RSSI, SNR, bruit)
* Modélisation pertes de paquets
* Scénarios dynamiques (mobilité, congestion)

### 🔹 Agent Reinforcement Learning

* Q-Learning ou DQN
* Optimisation dynamique des paramètres radio
* Fonction de récompense multi-critères :

  * fiabilité
  * consommation
  * performance

### 🔹 Baseline ADR

* Implémentation simplifiée ADR LoRaWAN
* Comparaison directe avec RL

### 🔹 Évaluation

* Packet Delivery Ratio (PDR)
* Consommation énergétique
* Stabilité du réseau

### 🔹 API REST

* Endpoint `/predict`
* Prédiction de l’action optimale en temps réel

---

## 🚀 Installation

### 1. Cloner le projet

```bash
git clone https://github.com/najeh-toumi-devops/lora-iot-intelligent-monitoring
cd lora-iot-intelligent-monitoring
```

### 2. Installer les dépendances

```bash
pip install -r requirements.txt
```

---

## ▶️ Utilisation

### 🔹 Lancer l’entraînement RL

```bash
python rl/train.py
```

### 🔹 Évaluer le modèle

```bash
python rl/evaluate.py
```

### 🔹 Générer dataset

```bash
python scripts/generate_dataset.py
```

### 🔹 Lancer l’API

```bash
uvicorn api.main:app --reload
```

---

## 🌐 API

### Endpoint

```
POST /predict
```

### Input

```json
{
  "snr": -10,
  "rssi": -120,
  "sf": 9,
  "tp": 14
}
```

### Output

```json
{
  "action": "increase_sf"
}
```

## 📊 Résultats attendus

* 📈 Amélioration du PDR
* 🔋 Réduction de la consommation énergétique
* ⚡ Adaptation dynamique aux conditions réseau


## 🆚 Comparaison RL vs ADR

| Critère              | ADR Standard | RL        |
| -------------------- | ------------ | --------- |
| Adaptabilité         | Faible       | Élevée    |
| Performance réseau   | Moyenne      | Optimisée |
| Consommation énergie | Moyenne      | Réduite   |

---

## 🧪 Tests

```bash
pytest tests/
```

## 🔁 Workflow Git

### Branches

* `main`
* `dev`
* `feature/rl-agent`
* `feature/simulator`
* `feature/evaluation`

### Bonnes pratiques

* Pull Request obligatoire
* Code review
* Commits clairs :

  * `feat: add RL agent`
  * `fix: reward function tuning`

## 📦 Livrables

* Code source complet
* Modèle RL entraîné
* Graphiques de performance
* API fonctionnelle
* Documentation technique


## 📚 Perspectives

* Intégration avec réseau LoRa réel
* Dashboard Grafana temps réel
* Publication scientifique
* Déploiement cloud (AWS / Azure)

---

## 📜 Licence

MIT License

---

## 💬 Contact

Projet encadré par Najeh Toumi
GitHub : https://github.com/najeh-toumi-devops
