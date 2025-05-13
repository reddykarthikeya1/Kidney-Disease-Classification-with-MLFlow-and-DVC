# 🩺 Kidney Disease Classification with Deep Learning, MLflow, DVC, and AWS CI/CD

## 🚀 Live Demo

**Our project is hosted at:**  
🌐 [http://54.226.246.2:8080/](http://54.226.246.2:8080/)

---

## 📚 Project Overview

This project is an end-to-end deep learning pipeline for **Kidney Disease Classification** using CT scan images. It leverages modern MLOps tools and best practices, including:

- **TensorFlow/Keras** for model development
- **MLflow** for experiment tracking
- **DVC** for data and pipeline versioning
- **AWS ECR & EC2** for containerized deployment
- **GitHub Actions** for CI/CD automation
- **Flask** for serving predictions via a web app

The entire workflow is automated, reproducible, and production-ready.

---

## 🏗️ Project Structure

```
.
├── config/                # Configuration files (YAML)
├── src/                   # Source code (pip installable package)
│   └── cnnClassifier/     # Main package
├── artifacts/             # Generated artifacts (models, data, etc.)
├── templates/             # Frontend (HTML)
├── research/              # Jupyter notebooks for experimentation
├── .github/workflows/     # GitHub Actions CI/CD workflows
├── Dockerfile             # Docker build instructions
├── dvc.yaml               # DVC pipeline stages
├── requirements.txt       # Python dependencies
├── app.py                 # Flask app for serving predictions
├── main.py                # Pipeline runner
└── README.md
```

---

## 🧑‍💻 Features

- **Data Ingestion:** Downloads and unzips kidney CT scan datasets.
- **Model Preparation:** Uses transfer learning (VGG16) for robust feature extraction.
- **Training:** Augments data, trains, and saves the best model.
- **Evaluation:** Evaluates model, logs metrics and artifacts to MLflow.
- **Experiment Tracking:** All hyperparameters, metrics, and models are tracked with MLflow.
- **Pipeline Versioning:** DVC orchestrates and versions the entire ML pipeline.
- **Web App:** Upload CT scan images and get predictions instantly.
- **CI/CD:** Automated build, test, Dockerization, and deployment to AWS EC2 via GitHub Actions.
- **Cloud Deployment:** Docker images are stored in AWS ECR and deployed on EC2.

---

## 🛠️ How to Run Locally

### 1. Clone the Repository

```bash
git clone https://github.com/reddykarthikeya1/Kidney-Disease-Classification-with-MLFlow-and-DVC.git
cd Kidney-Disease-Classification-with-MLFlow-and-DVC
```

### 2. Create and Activate a Conda Environment

```bash
conda create -n kidney python=3.8 -y
conda activate kidney
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python app.py
```

Visit [http://localhost:8080](http://localhost:8080) in your browser.

---

## ⚙️ MLOps & Deployment Workflow

### **MLflow Tracking**

- All experiments, parameters, and metrics are logged to MLflow.
- Easily compare runs and download models.

### **DVC Pipeline**

- Data and model artifacts are versioned and reproducible.
- Run the full pipeline with:

```bash
dvc repro
```

### **CI/CD with GitHub Actions & AWS**

- **CI:** Linting and unit tests on every push.
- **CD:** 
  - Docker image is built and pushed to AWS ECR.
  - EC2 (self-hosted runner) pulls the latest image and serves the app.
- **Secrets:** All AWS credentials are securely managed via GitHub Secrets.

---

## 🌐 Frontend

- Modern, responsive UI for uploading CT scan images.
- Animated background and professional layout.
- Displays prediction results and visualizations.

---

## 📦 Key Files

- `src/cnnClassifier/` - All pipeline and model code.
- `app.py` - Flask app for serving predictions.
- `main.py` - Runs the full ML pipeline.
- `dvc.yaml` - DVC pipeline definition.
- `Dockerfile` - Containerization instructions.
- `.github/workflows/main.yaml` - CI/CD pipeline.

---

## 📊 Example Results

- **Latest Model Accuracy:** 82% (see `scores.json`)
- **Loss:** 0.33

---

## 📝 References

- [MLflow Documentation](https://mlflow.org/docs/latest/index.html)
- [DVC Documentation](https://dvc.org/doc/)
- [AWS ECR](https://aws.amazon.com/ecr/)
- [AWS EC2](https://aws.amazon.com/ec2/)
- [Project GitHub Repo](https://github.com/reddykarthikeya1/Kidney-Disease-Classification-with-MLFlow-and-DVC)

---

## 👨‍💻 Author

**Karthikeya Reddy**  
[GitHub](https://github.com/reddykarthikeya1)

---

## 📢 License

This project is licensed under the [MIT License](LICENSE).

---
