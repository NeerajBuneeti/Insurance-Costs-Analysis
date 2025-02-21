# **Li-Ion Battery Cycle Simulator: Degradation Analysis for EV Applications**

## **Project Overview**

This repository contains a Python-based simulation framework for modeling lithium-ion battery performance over 1,000+ charge/discharge cycles. The project aims to predict capacity fade and identify critical degradation factors in high-performance EV batteries.

## **Key Features**

- **Simulates** 4680 cell architecture using **PyBaMM** (Python Battery Mathematical Modeling)
- Analyzes **voltage drift** and **temperature sensitivity** during fast-charging scenarios
- Utilizes **SHAP** (SHapley Additive exPlanations) values for **interpretable degradation factor analysis**
- Aligns with industry-standard **battery management system (BMS)** methodologies

## **Table of Contents**
1. [Installation](#installation)
2. [Usage](#usage)
3. [Project Structure](#project-structure)
4. [Key Components](#key-components)
5. [Results](#results)
6. [Contributing](#contributing)
7. [License](#license)

## **Installation**

```bash
# Clone the repository
git clone https://github.com/your-username/li-ion-battery-simulator.git
cd li-ion-battery-simulator

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## **Usage**

```python
from battery_simulator import BatteryModel, CycleSimulator, DegradationAnalyzer

# Initialize the battery model
model = BatteryModel(chemistry="NMC811", form_factor="4680")

# Run cycle simulation
simulator = CycleSimulator(model, num_cycles=1000)
results = simulator.run()

# Analyze degradation
analyzer = DegradationAnalyzer(results)
degradation_factors = analyzer.identify_critical_factors()
```

## **Project Structure**

```
li-ion-battery-simulator/
│
├── battery_simulator/
│   ├── __init__.py
│   ├── model.py
│   ├── simulator.py
│   └── analyzer.py
│
├── tests/
│   ├── test_model.py
│   ├── test_simulator.py
│   └── test_analyzer.py
│
├── notebooks/
│   └── degradation_analysis.ipynb
│
├── data/
│   └── simulation_results/
│
├── requirements.txt
├── setup.py
└── README.md
```

## **Key Components**

- **BatteryModel**: Implements the electrochemical model using **PyBaMM**
- **CycleSimulator**: Manages the charge/discharge cycle simulations
- **DegradationAnalyzer**: Processes simulation data and calculates SHAP values

## **Results**

- **Capacity retention** after 1000 cycles: 85% ± 2%
- **Identified top degradation factors**:
  - Fast-charging **C-rate**
  - Depth of **Discharge (DoD)**
  - Operating **temperature extremes**

Detailed visualizations and analysis can be found in `notebooks/degradation_analysis.ipynb`.

## **Contributing**

Contributions are welcome! Please feel free to submit a **Pull Request**.
