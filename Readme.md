Kidney Disease Classification using Deep Learning, DVC, MLflow & Explainable AI

A production-grade deep learning system for automated kidney CT scan analysis that combines transfer learning, reproducible MLOps pipelines, experiment tracking, and Explainable AI. The project demonstrates how a medical imaging model can be trained, evaluated, versioned, and deployed through a modular pipeline while maintaining reproducibility and transparency.

Project Overview

Medical image analysis plays an increasingly important role in assisting clinicians with disease detection. This project develops a complete machine learning workflow for binary kidney CT scan classification (Normal vs. Tumor) using transfer learning.

Beyond model development, the project focuses on engineering practices required for deploying machine learning systems in production. The pipeline incorporates automated data validation, reproducible experimentation, model versioning, experiment tracking, explainability through Grad-CAM, and an interactive web interface for real-time inference.

The workflow includes:

Automated dataset acquisition and validation
Image preprocessing and dataset transformation
CNN-based transfer learning with EfficientNet-B0
Hyperparameter configuration using YAML
Experiment tracking with MLflow
Pipeline orchestration using DVC
Explainable predictions with Grad-CAM
Streamlit deployment for real-time inference
Core Features
Capability	Description
Automated Data Pipeline	Downloads, validates, and preprocesses CT scan images before training.
Transfer Learning	Fine-tunes EfficientNet-B0 using ImageNet pretrained weights for binary classification.
Reproducible Experiments	Entire workflow managed through DVC with dependency tracking and versioned artifacts.
Experiment Management	MLflow records parameters, metrics, models, confusion matrices, and Grad-CAM outputs.
Explainable AI	Generates Grad-CAM heatmaps to visualize image regions influencing model predictions.
Early Stopping	Prevents overfitting by monitoring validation performance.
Model Checkpointing	Automatically saves the highest-performing model.
Interactive Deployment	Streamlit interface for image upload, prediction, confidence score, and visual explanation.
Modular Codebase	Component-based architecture following MLOps best practices for scalability and maintenance.
MLOps Pipeline
Data Ingestion
      │
      ▼
Data Validation
      │
      ▼
Data Transformation
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Grad-CAM Generation
      │
      ▼
Streamlit Deployment

Execute the complete workflow with:

dvc repro
