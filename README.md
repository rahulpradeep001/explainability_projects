# Explainability Projects

A collection of machine learning projects demonstrating various explainability techniques for model interpretability. This repository showcases how to make complex ML models more transparent and understandable using state-of-the-art explainability frameworks.

## Overview

This repository contains two main projects that demonstrate different explainability techniques applied to healthcare-related machine learning tasks:

1. **Heart Disease Prediction with SHAP + LLM Explanations**
2. **X-ray Classification with LIME Visualization**

## Projects

### 1. Heart Disease Prediction (`heart_disease_llm.ipynb`)

A heart disease prediction system using XGBoost classifier with SHAP (SHapley Additive exPlanations) for model interpretability, enhanced with Large Language Model (LLM) integration for natural language explanations.

**Key Features:**
- XGBoost classifier for binary heart disease prediction
- Hyperparameter tuning using GridSearchCV
- SHAP values for feature importance analysis
- Integration with HuggingFace LLM for human-readable explanations
- Visualization of feature contributions using waterfall and summary plots

**Dataset:**
- 1,025 patient records with 13 clinical features
- Features include age, sex, chest pain type, blood pressure, cholesterol, etc.
- Target: presence or absence of heart disease

**Model Performance:**
- Training accuracy: 99.86%
- Testing accuracy: 95.78%
- Cross-validation accuracy: 95.25%

**Explainability Techniques:**
- SHAP waterfall plots for individual predictions
- SHAP summary plots for global feature importance
- LLM-generated explanations based on feature importance scores

### 2. X-ray Classification with LIME (`lime_xrayclassification-pg.ipynb`)

A deep learning-based X-ray image classifier using transfer learning with VGG16, featuring LIME (Local Interpretable Model-agnostic Explanations) for visual explainability.

**Key Features:**
- Transfer learning with pre-trained VGG16 on ImageNet
- Multi-class classification: COVID-19, Pneumonia, Normal
- LIME explanations showing influential image regions
- Heatmap visualizations of superpixel importance

**Dataset:**
- X-ray images categorized into three classes
- Images preprocessed to 224x224 resolution
- 80-20 train-test split with stratification

**Model Performance:**
- Test accuracy: 96.34%
- Trained for 30 epochs with early convergence

**Explainability Techniques:**
- LIME image segmentation and superpixel analysis
- Positive/negative feature highlighting
- Heatmap visualization with importance weights
- Boundary marking on influential regions

## Technologies Used

### Machine Learning Frameworks
- TensorFlow/Keras
- XGBoost
- scikit-learn

### Explainability Libraries
- SHAP (SHapley Additive exPlanations)
- LIME (Local Interpretable Model-agnostic Explanations)

### Deep Learning
- VGG16 (Transfer Learning)
- Keras Applications

### LLM Integration
- LangChain
- HuggingFace Hub

### Data Processing & Visualization
- NumPy
- Pandas
- Matplotlib
- Seaborn
- scikit-image

## Installation

```bash
# Clone the repository
git clone <repository-url>
cd explainability_projects

# Install required packages
pip install xgboost numpy pandas scikit-learn matplotlib seaborn shap
pip install tensorflow keras
pip install lime
pip install langchain-huggingface
pip install pillow scikit-image
```

## Usage

### Heart Disease Prediction

1. Open `heart_disease_llm.ipynb` in Jupyter Notebook or Google Colab
2. Ensure you have the `heart.csv` dataset
3. Configure your HuggingFace API token in the notebook
4. Run all cells to train the model and generate explanations

### X-ray Classification

1. Open `lime_xrayclassification-pg.ipynb` in Jupyter Notebook or Google Colab
2. Mount your Google Drive (if using Colab) or update the data path
3. Ensure your X-ray images are organized in folders by class
4. Run all cells to train the model and visualize LIME explanations

## Explainability Techniques Explained

### SHAP (SHapley Additive exPlanations)
SHAP values provide a unified measure of feature importance based on game theory. They show how much each feature contributes to pushing the model output from the base value to the actual prediction.

**Use Cases:**
- Understanding which patient features most influence heart disease predictions
- Ranking features by their impact on individual predictions
- Generating actionable insights for clinical decision-making

### LIME (Local Interpretable Model-agnostic Explanations)
LIME explains individual predictions by approximating the model locally with an interpretable model. For images, it segments the image into superpixels and determines which regions are most important.

**Use Cases:**
- Visualizing which parts of an X-ray image led to a diagnosis
- Validating that the model focuses on medically relevant regions
- Building trust with medical practitioners by showing reasoning

## Model Outputs

### Heart Disease Project
- Trained XGBoost model saved as `heart_model1.pkl`
- SHAP visualizations (waterfall, summary, bar plots)
- LLM-generated natural language explanations

### X-ray Classification Project
- Trained VGG16 model saved as `VGG16_LIME.keras`
- LIME segmentation masks
- Heatmaps showing positive/negative contributions
- Boundary-marked images highlighting influential regions

## Future Enhancements

- Add more explainability techniques (GradCAM, Integrated Gradients)
- Expand to additional healthcare datasets
- Create interactive dashboards for real-time explanations
- Implement model comparison studies
- Add adversarial robustness testing

## License

This project is available for educational and research purposes.

## Acknowledgments

- SHAP library by Scott Lundberg
- LIME library by Marco Tulio Ribeiro
- VGG16 model from Keras Applications
- Heart disease dataset from UCI Machine Learning Repository

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests to improve the explainability techniques or add new projects.
