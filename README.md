# Comparative Analysis of Predictive Models for Blast Fragmentation  

## 📌 **Project Overview**  

Blast fragmentation significantly impacts mining efficiency, influencing costs, safety, and productivity. This project presents a **comparative analysis** of two predictive models:  
1. **Multivariate Regression Analysis (MRA)**: A statistical approach.  
2. **Artificial Neural Networks (ANN)**: A machine-learning-based model.  

The aim is to evaluate their effectiveness in predicting rock fragmentation outcomes for underground mining scenarios.  

---

## 🚀 **Features**  

- **Accurate Predictions**: Focused on predicting d20, d50, and d90 (fragmentation sizes) based on key parameters.  
- **Comprehensive Analysis**: Evaluation using industry-standard metrics:
  - **Mean Absolute Error (MAE)**  
  - **Mean Absolute Percentage Error (MAPE)**  
  - **Root Mean Square Error (RMSE)**  
  - **Relative Root Mean Square Error (RRMSE)**  
- **Real-World Data**: Tested on data from 38 underground bench blasts.  

---

## 🔧 **Methodology**  

### **1. Data Collection**  

The dataset includes critical parameters for blast design and rock properties:  

| **Parameter**                | **Description**                        |  
|-------------------------------|----------------------------------------|  
| **No. of Holes**             | Number of drill holes per blast.       |  
| **Bench Height**             | Height of the rock layer (m).          |  
| **Burden and Spacing**       | Distance between and around holes (m). |  
| **Explosive Quantities**     | Explosives per hole, total explosive.  |  
| **Charge Factor**            | Explosive weight per volume of rock.   |  

### **2. Models Developed**  

#### **A. Multivariate Regression Analysis (MRA)**  
- **Tools Used**: Microsoft Excel.  
- **Parameters Modeled**: Burden, charge factor, stemming, and explosive quantities.  
- **Equation Example**:  
  \[
  d_{50} = 1524.14 + 1.40N - 1.84H - 314.65B + 286.09S + 1.82Q_{\text{max}} - 1909.92q
  \]
  where \(N\): No. of Holes, \(H\): Bench Height, \(B\): Burden, \(q\): Charge Factor.  

#### **B. Artificial Neural Network (ANN)**  
- **Tools Used**: MATLAB Neural Network Toolbox.  
- **Architecture**:  
  - 7 Input Neurons: Parameters like burden, spacing, and explosive factors.  
  - 1 Hidden Layer: 10 neurons (optimized through experimentation).  
  - 1 Output Neuron: Predicted fragmentation size.  
- **Training Algorithm**: Levenberg-Marquardt Backpropagation with Bayesian Regularization.  

### **3. Validation and Testing**  
- **Training Data**: 75% of the dataset.  
- **Testing Data**: 25% of the dataset (mutually exclusive).  
- **Performance Metrics**: MAE, MAPE, RMSE, RRMSE.  

---

## 📊 **Results and Insights**  

### **Performance Metrics**  

| **Metric**       | **MRA Value** | **ANN Value** |  
|-------------------|---------------|---------------|  
| **MAE (mm)**      | 40.8          | 164.2         |  
| **MAPE (%)**      | 30.0          | 113.8         |  
| **RMSE (mm)**     | 50.5          | 207.4         |  
| **RRMSE**         | 0.1           | 0.2           |  

### **Key Observations**  
- **MRA Model**:  
  - Lower error rates across all metrics.  
  - Stronger predictive accuracy for all fragment sizes (d20, d50, and d90).  
  - High generalizability for underground blasting scenarios.  

- **ANN Model**:  
  - Exhibited higher error rates, particularly for larger fragment sizes (d90).  
  - Performance was inconsistent due to limited dataset size.  

### **Visual Comparison**  
Scatter plots of predicted vs. measured values:  
- MRA predictions closely align with measured values for d20, d50, and d90.  
- ANN predictions show greater deviation, especially for larger fragments.  

---

## ✅ **Conclusion**  

### **Key Findings**  
1. **Multivariate Regression Analysis (MRA)**:  
   - Superior performance in predicting blast fragmentation.  
   - Consistently lower MAE, MAPE, RMSE, and RRMSE values.  
   - Practical for optimizing blasting operations in underground mining.  

2. **Artificial Neural Network (ANN)**:  
   - Suitable for scenarios with larger datasets and complex non-linear relationships.  
   - Requires further tuning and a larger dataset for improved performance.  

### **Practical Benefits**  
- **Optimized Blasting**: Enhanced predictions lead to better control of fragmentation, reducing costs for secondary blasting and processing.  
- **Increased Efficiency**: Supports mining operations by improving productivity and safety.  

---

## 🔮 **Future Scope**  

- **Data Expansion**: Collect more data from diverse geological and operational conditions.  
- **Real-Time Monitoring**: Integrate dynamic data like vibration measurements and rock properties.  
- **Hybrid Approaches**: Combine regression with advanced machine learning methods (e.g., ensemble models) for enhanced accuracy.  

---

## 🙏 **Acknowledgments**  

This project was guided by **Dr. Ranjit Kumar Paswan**, Department of Rock Excavation Engineering, CISR-CIMFR. Resources and support were provided by CISR-CIMFR.  

**Contributor**:  
- **Rahul Kumar Sharma**  
  B.Tech (Mining Engineering), IIT (ISM) Dhanbad  

---

## 📚 **References**  

1. Cunningham, C., "The Kuz-Ram Model for Prediction of Fragmentation from Blasting," 1983.  
2. Ouchterlony, F., "The Swebrec Function, Linking Fragmentation by Blasting and Crushing," 2005.  
3. Haykin, S., "Neural Networks: A Comprehensive Foundation," 2004.  
4. Other references as listed in the project documentation.  
