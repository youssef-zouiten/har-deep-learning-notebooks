# Human Activity Recognition (HAR) with Deep Learning

Final project of a module in the Master's program in Intelligent Systems, École Normale Supérieure de Meknès.
Human Activity Recognition on the **UCI HAR** dataset: exploratory data analysis, deep learning models, data leakage analysis, class imbalance handling and explainability.

## Authors and supervision

- Youssef Zouiten (@Youssef7creat) and Hassan Jaha (@Hassan-jaha)
- Supervisors: Prof. Abdellaoui and Prof. Ou-ssekou

## Repository contents

| Notebook | Content |
|---|---|
| `EDA+DeepMLP+BiLSTM+1DCNN.ipynb` | Exploratory analysis, Deep MLP, BiLSTM, 1D CNN |
| `CNN-LSTM Hybrid.ipynb` | Hybrid CNN-LSTM model |
| `Modèle 5 — Transformer Encoder.ipynb` | Transformer Encoder model |
| `Data Leakage Analysis.ipynb` | Data leakage analysis (random split vs. subject-aware split) |
| `DeepSMOTE V2 Ameliore.ipynb` | Experimental DeepSMOTE branch for class imbalance |
| `XAI (Explainable AI).ipynb` | Explainability: SHAP, 1D Grad-CAM, Attention |

## Key results

- **95.25%**: best accuracy (Deep MLP)
- **+3.33%**: artificial accuracy inflation caused by data leakage with a random split
- **9.5:1**: artificial imbalance ratio studied
- The three XAI methods (SHAP, 1D Grad-CAM, Attention) converge on timesteps 0 to 12

## Methodological choices

- 6 sensor channels (`body_acc` xyz + `body_gyro` xyz) instead of 9, for smartphone compatibility
- `StandardScaler` fitted on training data only, to prevent leakage
- 33×17 reshape of the 561 features using exact factorization, with no zero-padding
- DeepSMOTE treated as an experimental branch, outside the main five-model pipeline

## Data

The dataset is not included in this repository. Download the **UCI HAR Dataset** (*Human Activity Recognition Using Smartphones*) from the UCI Machine Learning Repository, then adjust the paths in the notebooks.

## Usage

1. Clone the repository
2. Install Python and Jupyter
3. Download the UCI HAR dataset and adjust the paths
4. Open the notebooks with Jupyter and run the cells in order

## License

Academic project. Please contact the authors before any reuse.
