# Intelligent Skill Gap Analysis and Training Recommendation System

## 📌 Project Overview

The **Intelligent Skill Gap Analysis and Training Recommendation System** is a machine learning and Natural Language Processing (NLP) project designed to analyze the skills of interns and compare them with skills required by industry job roles.

The system uses **TF-IDF, K-Means clustering, and Cosine Similarity** to identify skill gaps, measure job readiness, recommend suitable job roles, and suggest training programs for missing skills.

---

## 🎯 Project Objective

The main objective of this project is to:

* Analyze intern skill profiles.
* Analyze industry job descriptions.
* Identify groups of interns with similar skills.
* Compare intern skills with industry requirements.
* Identify missing or deficient skills.
* Calculate an approximate job-readiness score.
* Recommend suitable job roles.
* Suggest training programs based on identified skill gaps.

---

## 🧠 Technologies Used

| Technology        | Purpose                        |
| ----------------- | ------------------------------ |
| Python            | Main programming language      |
| Pandas            | Data manipulation and analysis |
| NumPy             | Numerical operations           |
| Scikit-learn      | Machine learning and NLP       |
| TF-IDF            | Text feature extraction        |
| K-Means           | Intern skill clustering        |
| Cosine Similarity | Job-skill matching             |
| Matplotlib        | Data visualization             |
| Jupyter Notebook  | Development environment        |
| VS Code           | Development environment        |

---

## 📊 Machine Learning Methodology

The system follows these steps:

```text
Intern Skill Data
       ↓
Data Preprocessing
       ↓
Text Cleaning
       ↓
TF-IDF Vectorization
       ↓
K-Means Clustering
       ↓
Intern Skill Groups
       ↓
Cosine Similarity
       ↓
Job Matching
       ↓
Skill Gap Identification
       ↓
Readiness Score
       ↓
Training Recommendation
```

---

## 📁 Project Structure

```text
skill_gap_analysis/
│
├── skill_gap_analysis.ipynb
├── requirements.txt
├── README.md
├── interns.csv
├── jobs.csv
│
└── output/
    ├── skill_gap_analysis_results.csv
    ├── training_priorities.csv
    └── job_recommendations.csv
```

---

## 📂 Dataset Description

### `interns.csv`

Contains information about interns and their skills.

Example:

```text
intern_id,intern_name,skills
1,Ali,"Python, Pandas, NumPy, Machine Learning"
2,Sara,"Java, SQL, Spring, Git"
3,Ahmed,"HTML, CSS, JavaScript, React"
```

### `jobs.csv`

Contains industry job roles and their required skills.

Example:

```text
job_id,job_title,job_description
1,Data Scientist,"Python, SQL, Pandas, Machine Learning, Statistics"
2,NLP Engineer,"Python, NLP, Transformers, BERT, PyTorch"
3,Frontend Developer,"HTML, CSS, JavaScript, React, TypeScript"
```

---

## ⚙️ Installation

### 1. Clone or download the project

Open the project folder in VS Code.

### 2. Create a virtual environment

Windows:

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

Run:

```bash
pip install -r requirements.txt
```

### 4. Start Jupyter

Run:

```bash
jupyter notebook
```

Or open:

```text
skill_gap_analysis.ipynb
```

directly in VS Code.

---

## 🔍 Main Features

### 1. Skill Clustering

K-Means groups interns according to similar skill profiles.

For example:

```text
Cluster 0 → Web Development Skills
Cluster 1 → Java / Backend Skills
Cluster 2 → Data Science / AI Skills
```

The actual clusters are determined by the data.

---

### 2. Job Matching

Cosine similarity is used to compare intern skills with industry job descriptions.

The system identifies job roles whose requirements are most similar to an intern's current skills.

---

### 3. Skill Gap Detection

The system calculates:

```text
Skill Gap =
Required Industry Skills - Intern's Existing Skills
```

For example:

```text
Intern Skills:
Python
Pandas
NumPy

Required Skills:
Python
Pandas
NumPy
SQL
Statistics
Machine Learning

Missing Skills:
SQL
Statistics
Machine Learning
```

---

### 4. Job Readiness Score

The system calculates an approximate readiness percentage:

```text
Readiness Score =
Matched Required Skills / Total Required Skills × 100
```

For example:

```text
Matched Skills = 4
Required Skills = 6

Readiness = 4 / 6 × 100
          = 66.67%
```

---

### 5. Training Recommendation

Based on missing skills, the system recommends relevant training.

Example:

```text
Missing Skill:
Docker

Recommendation:
Complete Docker Fundamentals Training
```

---

### 6. Training Priority Analysis

The system also identifies the skills that are missing among the largest number of interns.

This can help an organization decide which training programs should be prioritized.

---

## 📈 Visualizations

The project generates visualizations such as:

* Number of interns in each skill cluster
* Most common skill gaps
* Intern readiness scores
* Skill distribution

These visualizations help HR teams understand the results more easily.

---

## 🧪 Example Analysis

A report for an intern may look like:

```text
==================================================
SKILL GAP ANALYSIS REPORT
==================================================

Intern: Ali

Recommended Job:
Data Scientist

Readiness Score:
66.67%

Existing Skills:
- Python
- Pandas
- NumPy
- Machine Learning

Missing Skills:
- SQL
- Statistics
- Data Visualization

Recommended Training:
- SQL and Database Fundamentals
- Statistics for Data Science
- Data Visualization
```

---

## 📤 Output Files

After running the notebook, the system generates:

### `skill_gap_analysis_results.csv`

Contains:

* Intern name
* Recommended job
* Existing skills
* Required skills
* Missing skills
* Readiness score
* Training recommendations

### `training_priorities.csv`

Contains:

* Missing skill
* Number of interns missing that skill
* Recommended training

### `job_recommendations.csv`

Contains:

* Intern name
* Recommended job
* Similarity score

---

## 👩‍💻 Development Environment

**IDE:** Visual Studio Code

**Notebook:** Jupyter Notebook

**Language:** Python

**Project Type:** NLP + Machine Learning + Clustering
