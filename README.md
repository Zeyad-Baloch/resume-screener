## Resume Screener with Bias Detection

This project implements a ** resume screening system** that combines **traditional NLP techniques** with **machine learning models** and **bias detection algorithms** to fairly evaluate candidates. It features an intuitive interface for HR professionals and recruiters.

---

## Project Overview

The Resume Screener addresses critical challenges in modern recruitment:
- **Automated candidate evaluation** using advanced NLP and ML techniques
- **Bias detection and mitigation** to ensure fair hiring practices  
- **Comprehensive skill matching** across multiple domains

**Key Features:**
-  **Machine Learning Scoring** with Random Forest regression
-  **Bias Detection** for gender, age, and demographic fairness
-  **Real-time Analytics** and visualization dashboards
-  **Professional UI** with custom Streamlit theming


---

## System Architecture

### Core Components

1. **ResumeScreener** (`resume.py`)
   - Text extraction and preprocessing
   - Skill, experience, and education parsing
   - Semantic similarity using Sentence Transformers
   - Basic scoring algorithms

2. **MLResumeScreener** (`bias_detection.py`)
   - Advanced feature engineering (20+ features)
   - Random Forest model with synthetic data training
   - Cross-validation and performance metrics
   - Ensemble prediction methods

3. **BiasDetector** (`bias_detection.py`)
   - Demographic inference from resume text
   - Statistical bias analysis (t-tests, demographic parity)
   - Bias mitigation algorithms
   - Fairness metrics computation

4. **Streamlit Interface** (`streamlit.py`)
   - Interactive web application
   - Real-time processing and visualization
   - Professional dashboard with Plotly charts


---

## Performance & Metrics

### Model Performance
- **R² Score**: ~0.85-0.90 on validation data
- **MSE**: <0.05 on normalized scores
- **Cross-validation**: 5-fold CV with consistent performance
- **Feature Importance**: Balanced across skill, experience, and education factors

### Bias Detection Capabilities
- **Gender Bias Detection**: Statistical significance testing
- **Age Group Analysis**: Multi-group fairness assessment  
- **Demographic Parity**: Equal opportunity metrics
- **Mitigation Strength**: Configurable bias correction (0.0-1.0)

---

## Installation & Setup

### 1. Clone Repository
```
git clone https://github.com/yourusername/resume-screener.git
cd resume-screener
```

### 2. Install Dependencies
```
pip install -r requirements.txt
```

**requirements.txt**:
```
streamlit==1.28.0
pandas==2.1.0
numpy==1.24.3
scikit-learn==1.3.0
sentence-transformers==2.2.2
plotly==5.15.0
PyPDF2==3.0.1
scipy==1.11.1
matplotlib==3.7.2
seaborn==0.12.2
```


## Usage Guide

### Basic Workflow

1. **Train ML Model** (First-time setup)
   - Click "Train ML Model" in sidebar
   - System generates 800+ synthetic training samples
   - Model trains automatically 

2. **Input Job Description**
   - Paste job posting in left text area
   - Include required skills, experience, education

3. **Upload Resumes**
   - Multiple file upload capability
   - Automatic text extraction

4. **Configure Settings**
   - Enable/disable bias mitigation
   - Adjust mitigation strength (0.0-1.0)
   - Model automatically processes and ranks candidates

5. **View Results**
   - **Rankings Tab**: Final scored rankings
   - **Comparison Tab**: Before/after bias mitigation
   - **Bias Analysis Tab**: Detailed fairness metrics
   - **Details Tab**: Feature importance and raw data


---


## Future Enhancements

### Technical Improvements
- [ ] **Database Integration**: PostgreSQL/MongoDB backend
- [ ] **Cloud Deployment**: AWS/Azure containerization  
- [ ] **Security Features**: Data encryption and privacy controls
- [ ] **Resume Templates**: Auto-generated candidate summaries
- [ ] **Deep Learning Integration**: BERT-based text understanding

---


## Contributing

We welcome contributions! Here's how to get involved:

### Areas for Contribution
- **Algorithm Improvements**: Better bias detection methods
- **UI Enhancements**: Additional visualization options
- **Performance Optimization**: Faster processing algorithms
- **Testing Coverage**: Comprehensive test suites

---

