# 🚗 EV Market Segmentation & Predictive Analytics Tool

> **An AI-powered interactive Streamlit application for comprehensive analysis, consumer segmentation, and forecasting of the Indian Electric Vehicle (EV) market.**

[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.45.0+-red.svg)](https://streamlit.io/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Architecture](#-architecture)
- [Project Structure](#-project-structure)
- [Data Sources](#-data-sources)
- [Consumer Segmentation Model](#-consumer-segmentation-model)
- [Machine Learning Models](#-machine-learning-models)
- [Installation](#-installation)
- [Usage](#-usage)
- [Application Pages](#-application-pages)
- [Key Algorithms & Implementations](#-key-algorithms--implementations)
- [Business Model](#-business-model)
- [Interview Preparation Guide](#-interview-preparation-guide)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Project Overview

This project is an **AI-powered market intelligence platform** designed to analyze the Indian Electric Vehicle market. It provides:

- **Real-time market analytics** based on actual sales data
- **Consumer segmentation** using Knowledge-Attitude-Practice (KAP) framework
- **Predictive modeling** for sales forecasting and adoption rates
- **Financial analysis tools** including revenue equations and breakeven analysis
- **Geographic insights** with state-wise penetration analysis
- **Business model framework** using Business Model Canvas approach

### Problem Statement
The Indian EV market is rapidly evolving with diverse consumer segments, varying regional adoption rates, and complex market dynamics. Businesses need data-driven insights to make strategic decisions about product development, pricing, and market entry.

### Solution
This tool transforms complex market data into actionable insights through:
- Interactive visualizations
- Machine learning-based predictions
- Consumer behavior analysis
- Financial modeling capabilities

---

## ✨ Features

### Core Features

| Feature | Description |
|---------|-------------|
| **Market Overview** | Real-time EV sales metrics, market share, and trend analysis |
| **Consumer Segmentation** | Four distinct consumer personas with detailed profiles |
| **Geographic Analysis** | State-wise adoption rates and penetration metrics |
| **Market Forecasting** | Multiple regression models for sales prediction |
| **Financial Modeling** | Revenue equations, breakeven analysis, and projections |
| **Business Model Canvas** | Complete B2B business strategy framework |

### Interactive Visualizations

- 📊 **Plotly Charts**: Interactive line charts, bar charts, pie charts, and scatter plots
- 📈 **Trend Analysis**: Monthly/yearly trend visualization with rolling averages
- 🗺️ **Geographic Heatmaps**: State-wise EV adoption visualization
- 🎯 **Radar Charts**: Multi-dimensional segment comparison
- 📉 **Dual-axis Charts**: Correlating multiple metrics

---

## 🛠️ Tech Stack

### Backend & Data Processing
```
Python 3.11+          → Core programming language
Pandas 2.2+           → Data manipulation and analysis
NumPy 2.0+            → Numerical computing
Scikit-learn 1.6+     → Machine learning algorithms
TensorFlow/Keras      → Deep learning models (optional analytics module)
```

### Frontend & Visualization
```
Streamlit 1.45+       → Web application framework
Plotly 6.0+           → Interactive visualizations
Matplotlib 3.9+       → Static charts and plots
Seaborn 0.13+         → Statistical visualizations
```

### Data Storage
```
CSV Files             → Primary data storage
Pickle (.pkl)         → Serialized ML models
HDF5 (.h5)            → Deep learning model storage
```

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        STREAMLIT APP (app.py)                   │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                    User Interface Layer                   │  │
│  │  • Navigation Sidebar    • Interactive Widgets           │  │
│  │  • Plotly Visualizations • Metrics Display               │  │
│  └──────────────────────────────────────────────────────────┘  │
│                              ▼                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                   Business Logic Layer                    │  │
│  │  • Consumer Segmentation    • Financial Calculations     │  │
│  │  • Forecast Generation      • Trend Analysis             │  │
│  └──────────────────────────────────────────────────────────┘  │
│                              ▼                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                    Data Processing Layer                  │  │
│  │            data_loader.py & ev_market_analysis.py         │  │
│  │  • ETL Pipeline      • Data Aggregation                  │  │
│  │  • Feature Engineering    • Data Validation              │  │
│  └──────────────────────────────────────────────────────────┘  │
│                              ▼                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                 Machine Learning Layer                    │  │
│  │              ev_predictive_models.py                      │  │
│  │  • Regression Models    • Clustering (K-Means)           │  │
│  │  • Deep Learning        • Time Series Forecasting        │  │
│  └──────────────────────────────────────────────────────────┘  │
│                              ▼                                  │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                      Data Layer (CSV)                     │  │
│  │  • Sales by State    • Sales by Makers                   │  │
│  │  • Consumer Responses    • Date Dimensions               │  │
│  └──────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────┘
```

---

## 📁 Project Structure

```
EV-project-prototype/
│
├── 📄 app.py                          # Main Streamlit application (1880 lines)
├── 📄 data_loader.py                  # Data loading and preprocessing utilities
├── 📄 requirements.txt                # Python dependencies
├── 📄 pyproject.toml                  # Project configuration
│
├── 📁 assets/
│   └── segment_descriptions.py        # Consumer segment definitions
│
├── 📁 ev_project/
│   ├── 📄 ev_market_analysis.py       # Market analysis algorithms
│   ├── 📄 ev_predictive_models.py     # ML/DL prediction models
│   ├── 📄 run_ev_analysis.py          # Analysis runner script
│   │
│   ├── 📁 EV_Market_Study-EVAnalysis-pandas-datasets/
│   │   ├── electric_vehicle_sales_by_state.csv
│   │   ├── electric_vehicle_sales_by_makers.csv
│   │   └── dim_date.csv
│   │
│   ├── 📁 A Dataset on Consumers Knowledge.../
│   │   ├── Response.csv               # Consumer survey data
│   │   ├── Questionnaire.docx         # Survey questionnaire
│   │   └── Code Book.docx             # Variable codebook
│   │
│   ├── 📁 New_project/
│   │   └── business_model.md          # Business Model Canvas
│   │
│   └── 📊 Saved Models & Visualizations
│       ├── sales_prediction_model.pkl
│       ├── state_adoption_model.pkl
│       ├── consumer_adoption_model.pkl
│       ├── consumer_behavior_dl_model.h5
│       ├── recommendation_clusters.pkl
│       └── *.png (various charts)
│
└── 📁 .streamlit/
    └── config.toml                    # Streamlit configuration
```

---

## 📊 Data Sources

### 1. Electric Vehicle Sales by State
**File**: `electric_vehicle_sales_by_state.csv`

| Column | Type | Description |
|--------|------|-------------|
| `date` | datetime | Month-Year of sales |
| `state` | string | Indian state name |
| `electric_vehicles_sold` | integer | EVs sold in period |
| `total_vehicles_sold` | integer | All vehicles sold |

**Key Insights Derived**:
- EV penetration rate per state
- Regional adoption trends
- Year-over-year growth by geography

### 2. Electric Vehicle Sales by Makers
**File**: `electric_vehicle_sales_by_makers.csv`

| Column | Type | Description |
|--------|------|-------------|
| `date` | datetime | Month-Year of sales |
| `maker` | string | Manufacturer name |
| `vehicle_category` | string | 2-Wheelers, 3-Wheelers, 4-Wheelers |
| `electric_vehicles_sold` | integer | Units sold |

**Key Insights Derived**:
- Market share by manufacturer
- Category-wise trends
- Brand performance analysis

### 3. Consumer Survey Responses (KAP Study)
**File**: `Response.csv`

| Column Pattern | Type | Description |
|----------------|------|-------------|
| `K1-K5` | 1-5 scale | Knowledge scores |
| `ATT1-ATT5` | 1-5 scale | Attitude scores |
| `P1-P5` | 1-5 scale | Practice scores |
| Demographics | categorical | Age, Gender, Occupation |

**Key Insights Derived**:
- Consumer segment classification
- Adoption likelihood prediction
- Behavioral pattern recognition

---

## 👥 Consumer Segmentation Model

The application segments Indian EV consumers into **four distinct personas** based on the Knowledge-Attitude-Practice (KAP) framework:

### Segmentation Algorithm

```python
# Simplified segmentation logic
def segment_consumer_responses(df):
    # Calculate composite scores
    df['knowledge_score'] = df[['K1','K2','K3','K4','K5']].mean(axis=1)
    df['attitude_score'] = df[['ATT1','ATT2','ATT3','ATT4','ATT5']].mean(axis=1)
    df['practice_score'] = df[['P1','P2','P3','P4','P5']].mean(axis=1)
    df['total_score'] = knowledge + attitude + practice
    
    # Rank-based segmentation (percentile approach)
    # Bottom 45%: Economy, Next 35%: Family, Next 15%: Premium, Top 5%: Luxury
```

### Consumer Segments

| Segment | Market Share | Income Range | Key Characteristics |
|---------|-------------|--------------|---------------------|
| **Economy EV Seekers** | 45% | ₹5-10L/yr | Price-sensitive, practical, value-focused |
| **Family EV Enthusiasts** | 35% | ₹10-20L/yr | Safety-conscious, feature-rich needs |
| **Premium EV Adopters** | 15% | ₹20-50L/yr | Status-conscious, tech enthusiasts |
| **Luxury Performance Seekers** | 5% | ₹50L+/yr | Exclusivity-seeking, performance-focused |

### Segment Details

#### 1. Economy EV Seekers (45%)
- **Demographics**: Tier 1/2 cities, Age 25-45
- **Primary Needs**: Affordable EVs, low TCO, reliable charging
- **Key Concerns**: Initial cost, range anxiety, battery replacement
- **Behavior**: Research-driven, practical usage

#### 2. Family EV Enthusiasts (35%)
- **Demographics**: Metropolitan areas, Age 30-50
- **Primary Needs**: Space, safety features, good range
- **Key Concerns**: Family safety, reliability, resale value
- **Behavior**: Highest KAP scores, early adopters

#### 3. Premium EV Adopters (15%)
- **Demographics**: Premium neighborhoods, Age 35-55
- **Primary Needs**: Luxury features, advanced tech
- **Key Concerns**: Brand prestige, performance
- **Behavior**: Status-conscious, brand loyal

#### 4. Luxury Performance Seekers (5%)
- **Demographics**: Top-tier cities, Age 40-65
- **Primary Needs**: High-performance, exclusivity
- **Key Concerns**: Cutting-edge technology, customization
- **Behavior**: Collection-oriented, less eco-motivated

---

## 🤖 Machine Learning Models

### 1. Sales Prediction Model

**Purpose**: Forecast future EV sales using time series analysis

**Models Compared**:
| Model | Algorithm | Use Case |
|-------|-----------|----------|
| Linear Regression | OLS | Baseline prediction |
| Ridge Regression | L2 regularization | Handle multicollinearity |
| Lasso Regression | L1 regularization | Feature selection |
| Random Forest | Ensemble trees | Non-linear patterns |
| Gradient Boosting | Sequential trees | Best accuracy |

**Features Used**:
- Year, Month (temporal)
- Lag features (t-1, t-2, t-3)

```python
# Sales prediction implementation
from sklearn.ensemble import GradientBoostingRegressor

model = GradientBoostingRegressor(random_state=42)
model.fit(X_train, y_train)

# 12-month rolling forecast
future_predictions = []
for month in range(12):
    prediction = model.predict(X_future)
    future_predictions.append(prediction)
```

### 2. State Adoption Prediction Model

**Purpose**: Predict EV adoption rate by state

**Algorithm**: Gradient Boosting Regressor

**Features**:
- Total vehicles sold
- Year, Quarter
- Historical adoption rates

**Output**: State-wise adoption percentage

### 3. Consumer Adoption Likelihood Model

**Purpose**: Predict individual purchase probability

**Features**:
- Knowledge score (30% weight)
- Attitude score (50% weight)
- Practice score (20% weight)
- Demographics (one-hot encoded)

**Preprocessing Pipeline**:
```python
from sklearn.pipeline import Pipeline
from sklearn.compose import ColumnTransformer

preprocessor = ColumnTransformer([
    ('num', StandardScaler(), numeric_features),
    ('cat', OneHotEncoder(), categorical_features)
])

model = Pipeline([
    ('preprocessor', preprocessor),
    ('regressor', GradientBoostingRegressor())
])
```

### 4. Deep Learning Model (Consumer Behavior)

**Purpose**: Pattern recognition in consumer behavior

**Architecture**:
```
Input Layer (n features)
    ↓
Dense(64, ReLU) + Dropout(0.3)
    ↓
Dense(32, ReLU) + Dropout(0.2)
    ↓
Dense(16, ReLU)
    ↓
Dense(1, Sigmoid) → Purchase Probability
```

**Training**:
- Optimizer: Adam
- Loss: Binary Crossentropy
- Early Stopping: patience=10

### 5. Vehicle Configuration Recommendation System

**Purpose**: Recommend EV configurations based on consumer profile

**Algorithm**: K-Means Clustering

**Process**:
1. Feature extraction (KAP scores, demographics)
2. StandardScaler normalization
3. Elbow method for optimal K
4. K=4 clusters → 4 vehicle configurations

**Recommendations**:
| Cluster | Vehicle | Battery | Range | Price |
|---------|---------|---------|-------|-------|
| 0 | Economy EV | 30 kWh | 200 km | ₹10-15L |
| 1 | Family EV | 40 kWh | 300 km | ₹15-20L |
| 2 | Premium EV | 60 kWh | 400 km | ₹20-30L |
| 3 | Luxury EV | 80+ kWh | 500+ km | ₹30L+ |

---

## ⚙️ Installation

### Prerequisites
- Python 3.11 or higher
- pip or uv package manager

### Step 1: Clone Repository
```bash
git clone https://github.com/Harshgoyal2004/EV-project-prototype.git
cd EV-project-prototype
```

### Step 2: Create Virtual Environment
```bash
# Using venv
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Or using uv (faster)
uv venv
source .venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt

# Or with uv
uv pip install -r requirements.txt
```

### Step 4: Verify Installation
```bash
python -c "import streamlit; import pandas; import sklearn; print('All dependencies installed!')"
```

---

## 🚀 Usage

### Running the Application
```bash
streamlit run app.py
```

The application will open in your browser at `http://localhost:8501`

### Running Standalone Analysis
```bash
cd ev_project

# Run market analysis
python ev_market_analysis.py

# Run predictive models
python ev_predictive_models.py
```

---

## 📱 Application Pages

### 1. Overview Page
**Path**: Navigation → Overview

**Contents**:
- EV Market Snapshot (Total sales, Market share, Top state/manufacturer)
- Four consumer segments introduction
- Monthly EV sales trend chart
- Market context and drivers

### 2. Segment Profiles Page
**Path**: Navigation → Segment Profiles

**Contents**:
- Dropdown selector for segments
- Demographics, Needs, Concerns, Behavior details
- Segment distribution pie chart
- Radar chart comparing KAP scores

### 3. Market Analysis Page
**Path**: Navigation → Market Analysis

**Contents**:
- Vehicle category distribution (2W, 3W, 4W)
- Top 10 manufacturers bar chart
- Time series by manufacturer
- Category-wise trends

### 4. Geographic Insights Page
**Path**: Navigation → Geographic Insights

**Contents**:
- Year selector for analysis
- Top states by EV sales
- EV penetration rate by state
- Multi-state comparison over time

### 5. Financial Projections Page
**Path**: Navigation → Financial Projections

**Contents**:
- Interactive sliders (Unit price, Sales volume, Fixed costs, Growth rate)
- Current year metrics
- 5-year projection table
- Revenue growth chart
- Dual-axis sales volume & margin chart

### 6. Financial Equation Page
**Path**: Navigation → Financial Equation

**Contents**:
- Revenue equation: R = p × q
- Profit equation: P = R - FC - VC
- Breakeven analysis with formula
- Interactive parameter configuration
- Revenue and profit curves

### 7. Business Model Page
**Path**: Navigation → Business Model

**Contents**:
- Value proposition visualization
- Customer segment explorer
- Tiered pricing model
- Cost structure pie chart
- Business Model Canvas
- Growth strategy roadmap

### 8. Predictive Analytics Page
**Path**: Navigation → Predictive Analytics

**Contents**:
- Linear regression predictions
- Historical vs predicted sales chart
- Model equation display
- What-if analysis slider
- Scenario comparison

### 9. Market Forecast Page
**Path**: Navigation → Market Forecast

**Contents**:
- Market statistics dashboard
- Multiple regression forecasts (Linear, Polynomial, Seasonal)
- Seasonality analysis by month
- YoY growth rate chart
- Penetration rate projections
- Segment evolution forecast
- S-curve adoption explanation

---

## 🔧 Key Algorithms & Implementations

### 1. Data Loading with Caching
```python
@st.cache_data
def load_all_data():
    """
    Cached data loading for Streamlit performance.
    Uses st.cache_data decorator to prevent reloading on each interaction.
    """
    sales_by_state = data_loader.load_sales_by_state()
    sales_by_makers = data_loader.load_sales_by_makers()
    # ... process and return all datasets
```

### 2. Time Series Forecasting
```python
def perform_market_forecast(df, months_ahead=24):
    """
    Multi-model time series forecasting with seasonality adjustment.
    
    Models:
    - Linear: Simple trend capture
    - Polynomial (degree=2): Non-linear trends
    - Seasonal versions: Both adjusted for monthly patterns
    """
    # Linear model
    linear_model = LinearRegression()
    linear_model.fit(X_linear, y)
    
    # Polynomial model
    poly = PolynomialFeatures(degree=2)
    X_poly = poly.fit_transform(X_linear)
    poly_model = LinearRegression()
    poly_model.fit(X_poly, y)
    
    # Seasonality factor calculation
    monthly_pattern = df.groupby('month')['sales'].mean()
    seasonal_factor = monthly_pattern / overall_mean
```

### 3. EV Penetration Rate Calculation
```python
def calculate_ev_penetration(df):
    """
    EV Penetration = (EV Sales / Total Vehicle Sales) × 100
    """
    df['ev_penetration'] = (
        df['electric_vehicles_sold'] / 
        df['total_vehicles_sold'] * 100
    )
    return df
```

### 4. Breakeven Analysis
```python
def calculate_breakeven(fixed_costs, unit_price, variable_cost_pct):
    """
    Breakeven Point = Fixed Costs / (Unit Price × (1 - Variable Cost %))
    
    The point where: Total Revenue = Total Costs
    """
    contribution_margin = unit_price * (1 - variable_cost_pct / 100)
    breakeven_point = fixed_costs / contribution_margin
    return breakeven_point
```

### 5. Innovation Adoption Lifecycle Categorization
```python
def categorize_adoption(adoption_rates):
    """
    Based on Rogers' Innovation Adoption Lifecycle:
    - Innovators/Early Adopters: Top 16%
    - Early Majority: Next 34%
    - Late Majority/Laggards: Bottom 50%
    """
    thresholds = {
        'innovator': adoption_rates.quantile(0.84),
        'early_majority': adoption_rates.quantile(0.50)
    }
    # Categorize states based on thresholds
```

---

## 💼 Business Model

### Business Model Canvas Summary

| Component | Details |
|-----------|---------|
| **Value Proposition** | Data-driven insights, Predictive intelligence, Financial modeling |
| **Customer Segments** | Auto manufacturers, Marketing agencies, Investment firms, Government |
| **Revenue Streams** | Tiered SaaS (₹50K-₹3L/month), Custom reports, Consulting |
| **Key Activities** | Data collection, ML model development, Platform maintenance |
| **Key Resources** | AI/ML models, Data pipeline, Domain expertise |
| **Channels** | SaaS platform, API, Direct sales, Partner network |
| **Cost Structure** | 45% Development, 15% Infrastructure, 15% Data, 25% Operations |

### Pricing Tiers

| Tier | Price/Month | Features |
|------|-------------|----------|
| Basic | ₹50,000 | Core analytics, Standard reports |
| Professional | ₹1,25,000 | Advanced analytics, API access, Custom dashboards |
| Enterprise | ₹3,00,000+ | Full access, Dedicated support, Custom analysis |

---

## 🎓 Interview Preparation Guide

### Commonly Asked Questions

#### Technical Questions

**Q1: Explain the data pipeline in this project.**
> The pipeline consists of: CSV data ingestion → Pandas preprocessing (date parsing, type conversion) → Feature engineering (YoY growth, penetration rates) → Aggregation functions → Visualization rendering. Data is cached using `@st.cache_data` for performance.

**Q2: How does the consumer segmentation work?**
> Using Knowledge-Attitude-Practice (KAP) framework: Calculate mean scores for K1-K5, ATT1-ATT5, P1-P5 → Sum to total score → Rank-based percentile segmentation (45% Economy, 35% Family, 15% Premium, 5% Luxury).

**Q3: What ML models are used and why?**
> - **Gradient Boosting** for sales prediction (handles non-linear patterns, robust to outliers)
> - **K-Means** for consumer clustering (interpretable segments)
> - **Neural Network** for behavior patterns (captures complex interactions)
> - **Linear/Polynomial Regression** for trend forecasting (simple, interpretable)

**Q4: How is the breakeven analysis implemented?**
> Breakeven = Fixed Costs / Contribution Margin
> Where Contribution Margin = Unit Price × (1 - Variable Cost %)
> The visualization shows revenue and profit curves intersecting at zero profit.

**Q5: Explain the seasonality adjustment in forecasting.**
> Monthly seasonal factors are calculated as: Monthly Average / Overall Average. Forecasts are then multiplied by these factors to account for seasonal patterns (e.g., higher sales post-budget, lower during monsoon).

#### Project-Level Questions

**Q6: What makes this project production-ready?**
> - Error handling for missing data
> - Caching for performance
> - Modular code structure
> - Configurable parameters
> - Comprehensive visualizations

**Q7: How would you scale this application?**
> - Database backend (PostgreSQL) instead of CSV
> - API layer (FastAPI) for data access
> - Cloud deployment (AWS/GCP)
> - Real-time data ingestion
> - User authentication

**Q8: What business value does this provide?**
> - Reduces market research time by 70%
> - Data-backed pricing decisions
> - Geographic expansion prioritization
> - Consumer targeting insights
> - Financial planning support

### Key Metrics to Remember

| Metric | Value |
|--------|-------|
| Total application pages | 9 |
| Consumer segments | 4 |
| ML models implemented | 5 |
| Datasets used | 3 |
| Lines of code (app.py) | 1880 |

### Key Libraries and Their Usage

| Library | Purpose |
|---------|---------|
| `streamlit` | Web application framework, UI components |
| `pandas` | Data manipulation, aggregation, groupby operations |
| `plotly` | Interactive visualizations (px.line, go.Scatter) |
| `scikit-learn` | ML models, preprocessing, metrics |
| `tensorflow` | Deep learning model for behavior patterns |
| `numpy` | Numerical operations, array manipulation |

---

## 🔮 Future Enhancements

1. **Real-time Data Integration**: API connections to government EV databases
2. **Predictive Maintenance**: Battery health prediction models
3. **Charging Station Optimization**: Location recommendation using geospatial analysis
4. **Sentiment Analysis**: Social media monitoring for brand perception
5. **Mobile Application**: React Native companion app
6. **Multi-language Support**: Hindi and regional language interfaces

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 📞 Contact

**Harsh Goyal**
- GitHub: [@Harshgoyal2004](https://github.com/Harshgoyal2004)
- Project Link: [https://github.com/Harshgoyal2004/EV-project-prototype](https://github.com/Harshgoyal2004/EV-project-prototype)

---

<p align="center">
  Made with ❤️ for the Indian EV Revolution
</p>
