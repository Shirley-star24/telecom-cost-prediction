# telecom-cost-prediction
"Predicting  telecomunication cell tower backup-power operational costs using Ridge Regression to handle severe multicollinearity across regional networks and environmental datasets under active load-shedding conditions. (Using simulated data)
## 📌 Project Overview
This repository addresses one of telecom's primary operational bottlenecks in South Africa: escalating backup power costs at cell towers driven by grid instability (load-shedding), regional network surges, and environmental conditions. 

Because regional telemetry datasets suffer from intense **multicollinearity** (e.g., ambient temperatures moving with cabinet temperatures, and user counts directly correlating with data throughput), standard Ordinary Least Squares (OLS) regression yields unstable, overfitted weights. 

This project implements an end-to-end Machine Learning pipeline utilizing **Ridge Regression ($L_2$ Regularization)** to stabilize predictive trends, handle messy missing telemetry data, and forecast daily operational costs across 30 unique South African regional nodes.

## 🚀 Key Features
* **Multi-Source Simulation:** Models synthetic telematics including weather, data throughput (TB), load-shedding intervals, contract structures, and high-cardinality regional nodes.
* **Automated Data Cleaning:** Employs a robust `scikit-learn` pipeline with `SimpleImputer` to handle random data dropouts/missing fields safely.
* **Feature Engineering:** Implements `OneHotEncoder` to safely handle low and high-cardinality categories without impacting column integrity.
* **Collinearity Mitigation:** Applies an $L_2$ penalty optimized via 5-Fold Grid Search Cross-Validation to shrink redundant weights and isolate authentic predictive signals.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Core Libraries:** Pandas, NumPy, Scikit-Learn,matplotlib
* **Model Evaluation:** Mean Squared Error (MSE),mean absolute_error, Coefficient of Determination ($R^2$)

## 📊 Business Impact
By producing stable cost-forecast metrics despite overlapping network datasets, this pipeline allows operations teams to proactively identify abnormal spending variations, prioritize battery replacements, and intelligently allocate maintenance budgets across active ZA nodes.
