# PRODIGY_ML_02: Customer Segmentation with K-Means Clustering

## Project Overview
This project implements unsupervised machine learning techniques to segment mall customers into distinct groups based on their shopping behavior. Using K-Means clustering, we analyze customer data to identify actionable segments and provide targeted marketing strategies.

## Dataset
**Source**: Kaggle "Mall Customers" dataset  
**File**: `Mall_Customers.csv`  
**Features**:
- CustomerID: Unique identifier
- Gender: Customer gender (Male/Female)
- Age: Customer age
- Annual Income (k$): Annual income in thousands
- Spending Score (1-100): Score assigned based on customer behavior and spending nature

## Project Structure
```
PRODIGY_ML_02/
│
├── Mall_Customers.csv          # Input dataset
├── customer_segmentation.py    # Main Python script
├── customer_segmentation.ipynb # Jupyter notebook version
├── requirements.txt            # Project dependencies
├── README.md                   # Project documentation
├── report.pdf                  # Detailed analysis report
│
├── outputs/
│   ├── optimal_k_analysis.png      # Elbow and silhouette analysis
│   ├── clustering_visualizations.png # Cluster visualizations
│   ├── clustering_comparison.png    # Comparison of methods
│   └── mall_customers_clustered.csv # Data with cluster labels
│
└── notebooks/
    └── customer_segmentation.ipynb  # Interactive notebook
```

## Installation
1. Clone the repository:
```bash
git clone https://github.com/ammarpvl29/PRODIGY_ML_02.git
cd PRODIGY_ML_02
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

## Key Features

### 1. Data Preprocessing
- Missing value analysis
- Gender encoding (Male=0, Female=1)
- Feature standardization using StandardScaler

### 2. Clustering Scenarios
- **Scenario A (2D)**: Annual Income vs Spending Score
- **Scenario B (3D)**: Annual Income, Spending Score, and Age
- PCA implementation for 3D visualization

### 3. Optimal K Selection
- Elbow method (inertia analysis)
- Silhouette score analysis
- Davies-Bouldin score evaluation

### 4. Customer Segments Identified

#### Cluster 0: Average Income, Average Spenders
- Balanced customers with moderate income and spending patterns
- Target with mid-range products and seasonal promotions

#### Cluster 1: High Income, High Spenders (Premium Customers)
- VIP segment with high purchasing power
- Focus on luxury experiences and exclusive products

#### Cluster 2: Low Income, Low Spenders (Budget Conscious)
- Price-sensitive customers
- Emphasize value deals and budget-friendly options

#### Cluster 3: Low Income, High Spenders (Young Enthusiasts)
- Trend-conscious customers who spend beyond means
- Offer flexible payment options and trendy products

#### Cluster 4: High Income, Low Spenders (Careful Spenders)
- Quality-focused, conservative spenders
- Highlight long-term value and sustainability

### 5. Alternative Clustering Methods
- **DBSCAN**: For density-based clustering
- **Agglomerative Clustering**: For hierarchical clustering
- Comparative analysis with K-Means

## Results Summary
- **Optimal number of clusters**: 5 (based on elbow and silhouette analysis)
- **Best performing method**: K-Means clustering
- **Silhouette Score**: ~0.55 (indicating good cluster separation)
- **Davies-Bouldin Score**: ~0.70 (lower is better)

## Business Recommendations

### 1. Premium Customer Strategy (Cluster 1)
- Implement VIP membership programs
- Offer personalized shopping experiences
- Create exclusive product lines
- Focus on quality and status symbols

### 2. Young Enthusiast Strategy (Cluster 3)
- Introduce Buy Now, Pay Later options
- Leverage social media marketing
- Create trendy, affordable collections
- Use gamification techniques

### 3. Budget Conscious Strategy (Cluster 2)
- Develop value product lines
- Implement aggressive discount strategies
- Focus on bulk buying options
- Emphasize practical benefits

## Visualizations
The project generates several key visualizations:
1. Elbow curves for optimal K selection
2. Silhouette score analysis
3. 2D and 3D cluster visualizations
4. Cluster distribution charts
5. Comparative analysis of clustering methods

## Usage
Run the main script:
```bash
python customer_segmentation.py
```

Or use the Jupyter notebook for interactive analysis:
```bash
jupyter notebook customer_segmentation.ipynb
```

## Technologies Used
- Python 3.8+
- pandas - Data manipulation
- numpy - Numerical operations
- scikit-learn - Machine learning algorithms
- matplotlib & seaborn - Data visualization
- PCA - Dimensionality reduction

## Future Enhancements
1. Implement additional clustering algorithms (GMM, Mean Shift)
2. Add customer lifetime value prediction
3. Create interactive dashboard for real-time segmentation
4. Integrate with CRM systems for automated targeting
5. Implement time-based segmentation for seasonal patterns

## Contributing
Feel free to fork this repository and submit pull requests for any enhancements.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Author
Created as part of the Prodigy InfoTech Machine Learning Internship

## Acknowledgments
- Kaggle for providing the Mall Customers dataset
- Prodigy InfoTech for the project opportunity
- scikit-learn documentation for clustering guidance