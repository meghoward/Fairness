# Algorithmic Fairness in Machine Learning

This repository explores the trade-offs between accuracy and fairness in machine learning models, focusing on standard and fairness-aware logistic regression models. The project implements and evaluates methods for improving model fairness, using Pareto Efficiency to balance accuracy and fairness.

## Key Results

- **Best Standard Model:** Achieved an accuracy of **0.75309** with an Equal Opportunity Difference (EOP) of **-0.61785**.
- **Best Fairness-Aware Model:** Using reweighting, achieved an accuracy of **0.72029** with an EOP of **-0.03176**, demonstrating a significant reduction in bias.
- **Pareto Efficiency Selection:** Identified models that optimized both accuracy and fairness:
  - **Standard Model:** Accuracy **0.75239**, EOP **-0.65693**
  - **Fairness-Aware Model:** Accuracy **0.72029**, EOP **-0.03176**

## Repository Contents

### Files

- **`Fairness cw.pdf`**: A comprehensive report detailing:
  - **Introduction**: Overview of algorithmic fairness and the problem statement.
  - **Standard Models**: Evaluation of standard logistic regression models across hyperparameters (C and solver types).
  - **Fairness-Aware Models**: Analysis using reweighing techniques by Kamiran and Calders (2012).
  - **Model Selection**: Application of Pareto Efficiency to select optimal models.
  - **Key Findings**: Trade-offs between fairness and accuracy and the effectiveness of fairness-aware approaches.
  - **Figures**: Visualizations of accuracy and fairness metrics.

- **`Fairness_notebook.ipynb`**: Jupyter notebook implementing:
  - Data preprocessing and reweighing.
  - Logistic regression model training and hyperparameter tuning.
  - Calculation of fairness metrics (e.g., Equality of Opportunity).
  - Visualization of accuracy and fairness trade-offs.
  - Pareto Efficiency-based model selection.

## Results Highlights

### Standard Models

- **Highest Accuracy:**  
  - **C:** 100, **Solver:** `saga`  
  - **Accuracy:** 0.75309, **EOP:** -0.61785  
- **Best Fairness:**  
  - **C:** 1.0, **Solver:** `liblinear`  
  - **Accuracy:** 0.75309, **EOP:** -0.61789  

### Fairness-Aware Models (Reweighed)

- **Highest Accuracy:**  
  - **C:** 0.01, **Solver:** `sag`  
  - **Accuracy:** 0.71903, **EOP:** -0.00144  
- **Best Fairness:**  
  - **C:** 0.0001, **Solver:** `saga`  
  - **Accuracy:** 0.72029, **EOP:** -0.03176  

### Pareto Efficiency

- **Standard Model:**  
  - **C:** 0.001, **Solver:** `liblinear`  
  - **Accuracy:** 0.75239, **EOP:** -0.65693  
- **Fairness-Aware Model:**  
  - **C:** 0.0001, **Solver:** `saga`  
  - **Accuracy:** 0.72029, **EOP:** -0.03176  

## Usage

### Prerequisites

Install the required Python libraries:

```bash
pip install numpy pandas scikit-learn matplotlib
```
### Running the Notebook

    Open the Fairness_notebook.ipynb file in Jupyter Notebook.
    Follow the step-by-step implementation to preprocess data, train models, and evaluate results.
    Modify hyperparameters to experiment with different trade-offs between accuracy and fairness.

### Report

Refer to Fairness cw.pdf for a detailed discussion of methods, results, and insights.

## Key Findings
  - The experiments reveal that fairness-aware models, particularly those using reweighing techniques, can significantly reduce bias (as measured by EOP) without a substantial loss in accuracy.
  - A Pareto Efficiency approach was used to select models that optimize both fairness and accuracy, providing a balanced solution to the trade-offs observed in earlier methods.

References

  - Kamiran, F., Calders, T. Data preprocessing techniques for classification without discrimination. Knowl Inf Syst 33, 1–33 (2012). https://doi.org/10.1007/s10115-011-0463-8
  - Corporate Finance Institute. "Pareto Efficiency," https://corporatefinanceinstitute.com/resources/economics/pareto-efficiency/
