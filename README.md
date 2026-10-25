# AI4I Predictive Maintenance

> Ce projet vise à anticiper les pannes d'une machine d'usinage à partir de ses données capteurs (températures, vitesse de rotation, couple, usure outil). Au-delà de la performance du modèle, il évalue l'intérêt économique d'une maintenance prédictive par rapport à une maintenance corrective, en raisonnant en temps d'arrêt et en coûts.

![Status](https://img.shields.io/badge/status-in%20progress-orange)
![Python](https://img.shields.io/badge/python-3.x-blue)

## Business context

Unplanned machine failures are one of the main sources of lost capacity on a production line. This project uses the following cost assumptions (illustrative figures):

| Event | Downtime | Cost |
|---|---|---|
| Unplanned failure (reactive repair) | ~4 h | ~€5,000 |
| Planned intervention (preventive) | ~30 min | ~€500 |

The question is whether existing sensor data can flag failures early enough to intervene, and whether doing so pays off.

## Dataset

The project uses the [AI4I 2020 Predictive Maintenance Dataset](https://archive.ics.uci.edu/dataset/601/ai4i+2020+predictive+maintenance+dataset) from the UCI Machine Learning Repository. It contains 10,000 synthetic records designed to mimic real industrial conditions.

- Inputs: product quality type (L/M/H), air temperature, process temperature, rotational speed, torque, tool wear
- Target: machine failure (binary), broken down into 5 failure modes: tool wear (TWF), heat dissipation (HDF), power (PWF), overstrain (OSF) and random (RNF)

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
git clone https://github.com/<your-username>/ai4i-predictive-maintenance.git
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
[LinkedIn](https://www.linkedin.com/in/traore-abou) · [Email](aboubakr.traore01@gmail.com)
