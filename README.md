# ECCV: Enhanced Clustering using Conditional Volatility

## 📌 Original Thesis Implementation

This repository contains the **original implementation** developed for the thesis research on **ECCV (Enhanced Clustering using Conditional Volatility)**. It demonstrates the complete methodology and algorithms used in the research.

**Important Notes:**
- Data paths, file access, and environment configurations may vary depending on your setup
- This repository is provided to illustrate the algorithms and methodology of the ECCV framework
- You may need to adapt code and file paths to work with your own data sources and environment

---

## 📄 Framework Overview

This repository contains the source code, datasets, and supporting materials for the research framework **ECCV (Enhanced Clustering using Conditional Volatility)** for clustering time-series data, including both benchmark datasets and real-world Thai stock market data.

---

## 🔍 Project Structure

This project is organized into two main parts:

- `benchmark/`: Analysis using synthetic datasets from UCR archive
- `real_world/`: Analysis using Thai stock market data
- `images/`: Framework diagram and visual assets

---

## 📁 benchmark/

- `A_Benchmark_study_ARIMA_GARCH.ipynb`  
   → Code for building ARIMA-GARCH models to estimate conditional volatility on benchmark datasets.
- `A_Benchmark_study_Clustering.ipynb`  
   → Code for running clustering algorithms (KMeans, Spectral, CLARA, etc.) using CV as features.
- `A_Benchmark_study_TS_dataset_source.txt`  
   → UCR dataset links used for benchmarking.
- `Statistics_test.ipynb`  
   → Statistical tests (e.g., normality, variance) to enhance clustering performance.
- `RandIndex_NMI_Result.csv`  
   → Clustering evaluation metrics (Rand Index, Normalized Mutual Information) for all methods.

📊 Meta-Feature Summary Files

- `Meta_type_summary_statistics.csv`
→ Summary statistics of key meta-features (e.g., ACF Lag-1, stationarity ratio, mean, std) grouped by dataset type. Useful for identifying structural patterns and comparing clustering performance across domains.

- `Meta_datasets_statistics.csv`
→ Dataset-level summary of meta-features for each benchmark dataset, including autocorrelation, stationarity, variability, and skewness metrics. Used for type-level and dataset-level analysis.

- `Meta_type_difference_summary.csv`
→ Difference in meta-feature values (Δ ACF Lag-1, Δ stationarity ratio) before and after applying CV, grouped by dataset type. This helps analyze how CV transformation structurally alters each data type.

---

## 📁 real_world/

- `Real_world_Thai_stock_data.ipynb`  
   → Full pipeline: data cleaning, ARIMA-GARCH modeling, CV extraction, and clustering on Thai stock data.
- `Adj_price_stock_raw_data.csv`  
   → Adjusted closing prices from Yahoo Finance for listed Thai companies.
- `Best_ARIMA_Model.csv`  
   → Summary of best ARIMA models with AIC and related parameters.
- `Best_GARCH_Model.csv`  
   → Summary of best GARCH models for each stock.
- `Conditional_volatility_data.csv`  
   → Conditional Volatility (CV) matrix generated from GARCH modeling.
- `Seasonal_test.csv`  
   → Results of seasonal tests (ADF, LBQ, etc.) for stationarity.
- `Thai_Stock_Sector.csv`  
   → Sector and industry labels for each stock, used in post-clustering analysis.

---

## 📊 Framework Diagram

![ECCV Framework](images/ECCV_framework_diagram.png)

---

## 📦 How to Use

### ⚠️ Important: Large Notebook Files

Some Jupyter notebooks contain large outputs and visualizations that exceed GitHub's file preview limit:
- `A_Benchmark_study_ARIMA_GARCH.ipynb` (38.5 MB)
- `A_Benchmark_study_Clustering.ipynb` (21.7 MB)
- `Real_world_Thai_stock_data.ipynb` (10.8 MB)

**To view these files:**
1. **Clone the repository** to your local machine:
   ```bash
   git clone https://github.com/Prakarn-Taranodom/eccv-implementation.git
   ```
2. **Download as ZIP** from GitHub and extract locally
3. **Use nbviewer**: Paste the GitHub file URL at https://nbviewer.org/

### Setup Instructions

1. **Install environment**:
   - Use Jupyter or Google Colab
   - (Optional) Set up virtual environment with:
     ```bash
     pip install -r requirements.txt
     ```

2. **Run Notebooks**:
   - Benchmark studies: navigate to `benchmark/`
   - Real-world Thai stock study: navigate to `real_world/`

3. **Google Colab Note**:
   - Mount Google Drive before accessing files
   - You may need to change file paths (e.g., `/content/drive/MyDrive/...`)

---

## 📎 Citation & Repository

This GitHub repository is cited in the thesis appendix.

**Repository URL**: [https://github.com/Prakarn-Taranodom/eccv-implementation](https://github.com/Prakarn-Taranodom/eccv-implementation)

For the research framework details and methodology, please refer to the thesis documentation and the notebooks in this repository.

