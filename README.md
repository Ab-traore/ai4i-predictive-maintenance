# Predictive Maintenance

> **Résumé (FR)** : A partir des données d'une fraiseuse (températures, vitesse de rotation, couple, usure outil), ce projet identifie les conditions de fonctionnement qui mènent à une panne. Les prédictions sont traduites en décisions de maintenance (continuer, surveiller, inspecter), avec un seuil d'alerte fixé en comparant le coût d'une panne manquée à celui d'une fausse alarme. Données synthétiques AI4I 2020 (UCI).

> **Summary**: using data from a milling machine (temperatures, rotational speed, torque, tool wear), this project identifies the operating conditions that lead to failure. Predictions are turned into maintenance decisions (continue, monitor, inspect), with an alert threshold set by weighing the cost of a missed failure against the cost of a false alarm. Synthetic data from AI4I 2020 (UCI).

![Status](https://img.shields.io/badge/status-in%20progress-orange)
![Python](https://img.shields.io/badge/python-3.x-blue)

## Business problem

- Unexpected machine failure interrupts production, increases maintenance costs and can damage equipment.
- Predictive maintenance turns sensor readings into a decision: **continue**, **monitor** or **inspect**.
- **Goal:** detect high-risk machines early while controlling false alarms.

## Dataset

The project uses the [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset) from the UCI Machine Learning Repository. It contains 10,000 synthetic records designed to mimic real industrial conditions.

- Inputs: product quality type (L/M/H), air temperature, process temperature, rotational speed, torque, tool wear
- Target: machine failure (binary), broken down into 5 failure modes: tool wear (TWF), heat dissipation (HDF), power (PWF), overstrain (OSF) and random (RNF)

### Failure outcomes and operating conditions 
| Category | Variables |
|---|---|
| **Product** | Type: L, M or H |
| **Thermal** | Air and process temperature |
| **Mechanical** | Rotational speed and torque |
| **Wear** | Accumulated tool-wear minutes |
| **Target** | Machine failure: 0 or 1 |

## Approach

The workflow loosely follows DMAIC:

1. Define: business problem, KPIs and cost assumptions
2. Measure: data quality, class imbalance, exploratory analysis
3. Analyze: feature engineering based on the physics of the machine, failure mode analysis
4. Improve: modeling, compared against a simple rule-based baseline
5. Control: what deployment would require (alert thresholds, monitoring, retraining)

## Key results

_To be completed._

## Project structure

```
ai4i-predictive-maintenance/
├── data/              # raw data (not versioned)
├── notebooks/         # analysis notebooks, numbered in order
├── src/               # reusable functions
├── reports/figures/   # exported charts
├── requirements.txt
└── README.md
```

## How to run

```bash
git clone https://github.com/<pseudo-name>/ai4i-predictive-maintenance.git
cd ai4i-predictive-maintenance
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

The notebooks download the dataset automatically with the `ucimlrepo` package.

## Limitations and next steps

_To be completed._

## Author

[Abou TRAORE], Industrial Engineer
[LinkedIn](https://www.linkedin.com/in/traore-abou) · [Email](mailto:aboubakr.traore01@gmail.com)
