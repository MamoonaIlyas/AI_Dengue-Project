# AI_Dengue-Project
This project uses AI and unsupervised learning techniques like K-Means, DBSCAN, and Autoencoders to predict and cluster global dengue cases (1924–2023). A Django-based web app allows users to input symptoms and receive real-time dengue risk predictions.

🦟 AI-Based Dengue Prediction & Surveillance
Project: Global Dengue Surveillance Dataset (1924–2023)
Developed During: Final Year Project / AI Capstone

📌 Objective
This project leverages Artificial Intelligence and Machine Learning techniques to analyze and predict dengue outbreaks using the OpenDengue Dataset, a comprehensive global dataset covering dengue cases from 1924 to 2023. The goal is to support early detection and health intervention using both supervised and unsupervised learning techniques.

🗂️ Dataset
Source: OpenDengue

Size: ~383,000 records

Location: Covers multiple countries (e.g., Afghanistan)

Key Features: S_res, T_res, dengue_total, adm_0_name, calendar_start_date, FAO_GAUL_code

Challenges: Missing values, class imbalance, noise in geographical codes

⚙️ Project Modules
✅ 1. Data Preprocessing
Converted date fields to datetime

Filled missing values with "Unknown"

Dropped irrelevant columns like UUID

Scaled and normalized numeric features (S_res, T_res)

✅ 2. Feature Selection & Extraction
Genetic Algorithms: Used for selecting top predictive features

PCA (Principal Component Analysis): Applied for dimensionality reduction

✅ 3. Machine Learning Models
🔸 Unsupervised Learning:
K-Means Clustering

Hierarchical Clustering

DBSCAN (Density-Based Clustering)

Autoencoders: Dimensionality reduction + DBSCAN

Association Rules using Apriori (pattern mining)

🔸 Evaluation Metrics:
Silhouette Score

Adjusted Rand Index (ARI)

Homogeneity Score

Reconstruction Error / MSE (for Autoencoder)

Confusion Matrix

✅ 4. Model Comparison
Technique	Silhouette Score	ARI	Notes
K-Means	Moderate	0.0791	Fast, but sensitive to outliers
Hierarchical	Higher than K-Means	0.1775	Better label alignment
DBSCAN	Highest (1.0)	N/A	Best for handling noise & shape

✅ 5. Web-Based Prediction App (Django)
A Django-based frontend allows users to enter S_res and T_res values and receive:

Predicted cluster label

A user-friendly diagnosis message (e.g., "You do not have dengue" or "Critical condition detected")

🔧 Technologies:
Django 5.1.4

HTML, CSS (custom UI)

Python backend integrated with pre-trained models

📌 Key Features
Multiple clustering techniques implemented and evaluated

Real-time prediction through a web interface

Scalable AI system for public health surveillance

Applied both AI theory and practice to a critical real-world problem

📂 File Structure
bash
Copy
Edit
/dengue_project
│
├── models/                  # Saved ML models (.pkl, .h5)
├── app/                    # Django app
│   ├── views.py
│   ├── forms.py
│   ├── templates/
│   └── static/
├── processed_dataset.csv   # Cleaned and prepared dataset
├── notebooks/              # Python scripts & experiments
├── README.md

🚀 Future Scope
Integration with time-series forecasting (LSTM models)

Real-time outbreak dashboard

Incorporate more countries and climatic indicators

Enhance frontend with interactive maps using Leaflet.js or Plotly

