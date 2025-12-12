# Multi-Armed Bandit for Personalized Drug-Dosage Optimization  
(Individual Academic Project – 2025)

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1DYvu5cqAxcIRbTrPBQBU09vqvcSKsX4B)  
A complete, reproducible proof-of-concept that uses classical multi-armed bandit (MAB) algorithms to recommend optimal drug-dosage combinations from historical patient data.

### Project Overview
- **Goal**: Identify the best drug + dosage pair for three major patient groups (mental health, chronic pain, metabolic/chronic disorders) while minimizing cumulative regret.
- **Action space**: 5 clinically relevant drugs × 3 standardized dosages (0.5, 1.0, 1.5) → 15 arms per group.
- **Algorithms implemented from scratch**:
  - ε-greedy
  - UCB1 (tunable confidence parameter)
  - Thompson Sampling (Beta-Bernoulli / Gaussian version)
- **Evaluation**: 100 independent Monte Carlo runs × 1000 pulls per algorithm and patient group.
- **Key result**: Thompson Sampling consistently outperforms the others, reducing regret by 12–27 % depending on the clinical group.

### Features
- Single, fully executable Google Colab notebook (runs in < 4 minutes on the free tier)
- No external dependencies beyond standard Python data-science libraries
- Fixed random seed (42) → 100 % reproducibility
- Publication-ready plots (cumulative regret curves, boxplots, optimal-arm heatmaps)
- Clean, heavily commented code suitable for teaching or collaboration

### Repository Contents
```
├── main.ipynb                  ← Complete Colab notebook (open the badge above)
├── historical_patient_data.csv ← Sample synthetic dataset (real data redacted)
├── requirements.txt            ← pip install -r requirements.txt
├── README.md                   ← This file
└── figures/                    ← Exported plots (optional)
```

### How to Run
1. Click the “Open in Colab” badge above, or
2. Clone the repo and open `main.ipynb` in Jupyter/Colab locally.

```bash
git clone https://github.com/yourusername/multi-armed-bandit-drug-optimization.git
cd multi-armed-bandit-drug-optimization
jupyter notebook main.ipynb
```

### Requirements
```txt
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
scipy>=1.10
scikit-learn>=1.3
```

Install with:
```bash
pip install -r requirements.txt
```

### Future Collaboration (Open Invitation)
This prototype is deliberately lightweight and interpretable so it can be handed directly to clinical or pharmacological research groups for:
- Validation on real, richly phenotyped patient cohorts
- Extension to narrow disease clusters (e.g., treatment-resistant depression, fibromyalgia, diabetic nephropathy)
- Integration of safety constraints and prospective testing

I am actively seeking medical collaborators for the next phase.

### License
MIT License – feel free to use, modify, and cite in academic work (please reference this repository).

### Author
[Your Full Name]  
Independent Academic Project (approx. 60 hours, 2025)  
Supervised by: [Mentor Name] (one consultation)

⭐ Star this repo if you find it useful for teaching reinforcement learning in healthcare!