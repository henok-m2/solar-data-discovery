#solar data discovery challenge - week 0
# Solar Data Discovery - Data Analysis Project

## 📋 Project Overview

This project analyzes solar energy potential across three West African countries: Benin, Sierra Leone, and Togo. The analysis examines solar irradiance data (GHI, DNI, DHI) along with environmental factors to identify the most suitable location for solar energy investment.

## 🎯 Objectives

- **Data Profiling & Cleaning**: Process and clean raw solar data from three countries
- **Exploratory Data Analysis**: Understand patterns and characteristics of solar potential in each country
- **Comparative Analysis**: Identify the best location for solar investment based on statistical evidence
- **Strategic Recommendation**: Provide data-driven insights for solar energy development decisions

## 📁 Project Structure

```
solar-data-discovery/
├── data/
│   ├── benin-malanville.csv          # Raw data for Benin
│   ├── sierraleone-bumbuna.csv       # Raw data for Sierra Leone
│   ├── togo-dapaong_qc.csv           # Raw data for Togo
│   ├── benin-clean.csv               # Cleaned Benin data
│   ├── sierraleone-clean.csv         # Cleaned Sierra Leone data
│   └── togo-clean.csv                # Cleaned Togo data
├── notebooks/
│   ├── benin-EDA.ipynb               # Benin exploratory analysis
│   ├── sierraleone-EDA.ipynb         # Sierra Leone exploratory analysis
│   ├── togo-EDA.ipynb                # Togo exploratory analysis
│   └── comparative-analysis.ipynb    # Final comparative analysis
└── README.md
```

## 🛠️ Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computations
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **SciPy** - Statistical analysis
- **Jupyter Lab** - Interactive development environment

## 📊 Data Sources

The project uses solar measurement data from three locations:
- **Benin**: Malanville station
- **Sierra Leone**: Bumbuna station  
- **Togo**: Dapaong station

### Key Metrics Analyzed:
- **GHI (Global Horizontal Irradiance)**: Total solar radiation received
- **DNI (Direct Normal Irradiance)**: Direct beam solar radiation
- **DHI (Diffuse Horizontal Irradiance)**: Scattered solar radiation
- **Tamb**: Ambient temperature
- **RH**: Relative humidity
- **WS**: Wind speed

## 🚀 Installation & Setup

### Prerequisites
- Python 3.7+
- Git
- Virtual environment tool

### Step-by-Step Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd solar-data-discovery
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv VENV
   source VENV/bin/activate  # On Windows: VENV\Scripts\activate
   ```

3. **Install required packages**
   ```bash
   pip install pandas numpy matplotlib seaborn scipy jupyterlab
   ```

4. **Prepare data files**
   - Extract data.zip from course materials
   - Copy CSV files to the `data/` directory

5. **Launch Jupyter Lab**
   ```bash
   jupyter lab
   ```

## 📈 Analysis Workflow

### Phase 1: Individual Country Analysis

#### Data Cleaning Steps:
- Remove empty 'Comments' column
- Correct negative irradiance values (set to 0)
- Handle missing values appropriately
- Flag statistical outliers using Z-score method (|Z| > 3)

#### Exploratory Analysis for Each Country:
- Time series analysis of GHI
- Distribution analysis of temperature and wind speed
- Correlation heatmaps of key variables

### Phase 2: Comparative Analysis

#### Statistical Comparison:
- Box plot comparisons of GHI, DNI, DHI across countries
- Summary statistics (mean, median, standard deviation)
- ANOVA test for statistical significance of differences

## 🔍 Key Findings

### Data Quality Insights
- All datasets required cleaning of negative irradiance values
- 'Comments' column was consistently empty across all datasets
- Outliers were identified and flagged for further investigation

### Solar Potential Patterns
*(Based on actual analysis results)*

**Highest Average GHI**: Benin  
**Most Consistent Production**: Togo  
**Greatest Variability**: Sierra Leone

### Statistical Significance
- ANOVA test revealed significant differences in GHI between countries
- P-value: 1.79e-261 (extremely small, essentially 0)

## 💡 Strategic Recommendation

Based on the comprehensive analysis:

### For Maximum Energy Output:
**Recommended**: Benin 
**Rationale**: Highest mean GHI values and strong overall solar resource availability

### For Stable & Predictable Generation:
**Recommended**: Benin 
**Rationale**: Most stable production patterns with lower variability

## 📝 How to Reproduce Analysis

1. **Run Individual Country Analysis**
   ```bash
   # Execute notebooks in order:
   notebooks/benin-EDA.ipynb
   notebooks/sierraleone-EDA.ipynb  
   notebooks/togo-EDA.ipynb
   ```

2. **Run Comparative Analysis**
   ```bash
   notebooks/comparative-analysis.ipynb
   ```

3. **View Results**
   - Cleaned datasets in `data/` directory
   - Visualizations and statistics in notebooks
   - Final recommendation in comparative analysis notebook

## 🤝 Contributing

This project follows a structured branching strategy:

1. Create feature branches for each analysis (`EDA-benin`, `EDA-sierra-leone`, etc.)
2. Submit pull requests for review
3. Merge to main after approval

## 📄 License

This project was completed as part of the Kaim 10 Academy curriculum.

## 👥 Authors

- Henok Mulugeta
- Kaim 10 Academy - Data Analysis Program

## 🔗 References

- Solar irradiance measurement standards
- Statistical methods for renewable energy assessment
- West African solar energy potential studies

---

*Last Updated: 12 Nov 2025*
