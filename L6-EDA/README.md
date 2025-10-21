# Homework-2

Team: 18-22\
Authors:\
- Mykhailo Buleshnyi\
- Maksym Buleshnyi\
- Artur Pelcharskiy\
- Davyd Ilnytskyi\

## Missing Values Correlation Visualization - Analysis

### Motivations
Understanding how missing values correlate across columns helps diagnose data quality problems and detect systematic missingness.  
If two columns often have missing values together, it may suggest a shared cause (e.g., a data collection issue or dependent variables).  
Visualizing these correlations helps guide imputation strategies and feature selection.

### Key Ideas
We calculated pairwise correlations between columns’ missingness indicators (1 = missing, 0 = present).  
This matrix quantifies how strongly missing patterns align between features.  
The visualization uses a heatmap to display correlations, where darker colors indicate stronger co-missing relationships.  
This approach makes patterns of dependent missingness immediately visible.

### Design Decisions
- **Color:** Diverging colormap (`blue → red`) emphasizes both positive and negative correlations.  
- **Scale:** Normalized between -1 and 1 for interpretability.  

### Limitations
- High correlation does not imply causation — columns may appear related due to hidden dependencies.  
- Sparse datasets may yield misleading correlations if too few observations remain.  
- Scalability: Correlation matrix computation scales quadratically with the number of columns, so large datasets require sampling or dimensionality reduction.  
- Airbnb dataset may have uneven missingness, making some columns dominate visually; subsetting columns improves readability.

### Visualization


