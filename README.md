# CINF-MODELLO-DI-CLASSIFICAZIONE-
Modello di classificazione di 7 tipologie di oggetti astrofisici 
# Modello C∞ – Classificazione 7 tipologie di oggetti astrofisici incluso l'ambiente (Giugno 2025) - Usare pulsar, AXP e magnetar come sonde per materia oscura. 

Questo repository contiene:
* `Cinf_full.pdf` – articolo completo.
* `Cinf preferisce un profilo Burkert pdf
* MIT LICENSE
* Test Cinf 12 - 12 real Objects python code test ready to use

## Quick Start
To run the classification with cross-validation and generate plots:
```bash
python cinfty_classification_test.py --plot --cv

numpy>=1.26.4
pandas>=2.2.3
scikit-learn>=1.5.2
matplotlib>=3.9.2

# Use official Python 3.9 slim image as base
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Install system dependencies
RUN apt-get update && apt-get install -y \
    gcc \
    && rm -rf /var/lib/apt/lists/*

# Copy requirements file
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy Python script and data
COPY classify_objects.py .
COPY data.csv .

# Command to run the script
CMD ["python", "classify_objects.py"]

docker build -t astro-classifier .
docker run astro-classifier


⚠️  Lavoro in corso / proof-of-concept. Commenti e pull-request benvenuti!

- 📄 [Scarica il paper completo (`CINF_full.pdf`)](https://raw.githubusercontent.com/Mihart-web/CINF-MODELLO-DI-CLASSIFICAZIONE-/main/CINF_full.pdf)
- 📄 [Analisi profilo Burkert (`CINF_PREFERISCE_UN_PROFILO_BURKERT.pdf`)](https://raw.githubusercontent.com/Mihart-web/CINF-MODELLO-DI-CLASSIFICAZIONE-/main/CINF_PREFERISCE_UN_PROFILO_BURKERT.pdf)
Contatti: Mihaela Vengher ( Mia) – <mihart.creation@gmail.com>
