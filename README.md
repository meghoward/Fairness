This repository contains two key files that explore the trade-offs between accuracy and fairness in machine learning models:

    Fairness Report (PDF) – A detailed report documenting the results of experiments conducted to compare standard machine learning models and fairness-aware models, focusing on balancing accuracy and fairness.
    Fairness Notebook (IPYNB) – A Jupyter notebook that includes the implementation of models, hyperparameter tuning, and fairness interventions using Python and machine learning libraries such as Scikit-learn.

Files

    Fairness cw.pdf: This report outlines the findings from a study on algorithmic fairness in machine learning models. It evaluates standard logistic regression models against fairness-aware models using metrics such as accuracy and Equality of Opportunity (EOP). The report introduces reweighing techniques to reduce bias and examines the trade-offs between fairness and performance.
        Key Sections:
            Introduction and Dataset Overview
            Analysis of Standard and Fairness-aware Models
            Model Selection based on Accuracy and Fairness
            Pareto Efficiency as a Model Selection Criterion
            Results Summary and Comparison of Models

    Fairness_notebook.ipynb: This Jupyter notebook implements the machine learning experiments described in the report. It includes the following:
        Data preprocessing and reweighing using Kamiran and Calders' 2012 method.
        Logistic regression model training and hyperparameter tuning.
        Fairness metrics calculation (Equality of Opportunity).
        Visualization of the trade-offs between accuracy and fairness.
        Final model selection using Pareto Efficiency.

Requirements

To run the Jupyter notebook, ensure that you have the following Python libraries installed:

    numpy
    pandas
    scikit-learn
    matplotlib

You can install these dependencies using pip:

bash

pip install numpy pandas scikit-learn matplotlib

How to Use

    Report: Read the Fairness cw.pdf to understand the motivation, methodology, and results of the study.
    Notebook: Open the Fairness_notebook.ipynb file in a Jupyter environment to explore the code, run the models, and visualize the results. The notebook provides a step-by-step guide for reproducing the experiments from the report.

Key Findings

    The experiments reveal that fairness-aware models, particularly those using reweighing techniques, can significantly reduce bias (as measured by EOP) without a substantial loss in accuracy.
    A Pareto Efficiency approach was used to select models that optimize both fairness and accuracy, providing a balanced solution to the trade-offs observed in earlier methods.

References

    Kamiran, F., Calders, T. Data preprocessing techniques for classification without discrimination. Knowl Inf Syst 33, 1–33 (2012). https://doi.org/10.1007/s10115-011-0463-8
    Corporate Finance Institute. "Pareto Efficiency," https://corporatefinanceinstitute.com/resources/economics/pareto-efficiency/
