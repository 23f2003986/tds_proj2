# Automated Dataset Analysis

## Overview
This folder contains an analysis of the dataset **happiness.csv**. The following sections describe the preprocessing steps, the analysis conducted, clustering results, visualizations, and insights derived from the data.

## Dataset Summary
The dataset consists of the following structure:

### Data Overview
- Total Rows: 2363
- Total Columns: 11
### Column Data Types
```
- Country name: object
- year: float64
- Life Ladder: float64
- Log GDP per capita: float64
- Social support: float64
- Healthy life expectancy at birth: float64
- Freedom to make life choices: float64
- Generosity: float64
- Perceptions of corruption: float64
- Positive affect: float64
- Negative affect: float64
```
### Missing Values
```
- Country name: 0 missing values
- year: 0 missing values
- Life Ladder: 0 missing values
- Log GDP per capita: 0 missing values
- Social support: 0 missing values
- Healthy life expectancy at birth: 0 missing values
- Freedom to make life choices: 0 missing values
- Generosity: 0 missing values
- Perceptions of corruption: 0 missing values
- Positive affect: 0 missing values
- Negative affect: 0 missing values
```
### Numeric Summary
```
year:
- count: 2363.0
- mean: 2014.7638595006347
- std: 5.059436468192803
- min: 2005.0
- 25%: 2011.0
- 50%: 2015.0
- 75%: 2019.0
- max: 2023.0
Life Ladder:
- count: 2363.0
- mean: 5.483565806178587
- std: 1.1255215132391931
- min: 1.281
- 25%: 4.647
- 50%: 5.449
- 75%: 6.3235
- max: 8.019
Log GDP per capita:
- count: 2363.0
- mean: 9.400895471857808
- std: 1.1452751661753884
- min: 5.527
- 25%: 8.52
- 50%: 9.503
- 75%: 10.382
- max: 11.676
Social support:
- count: 2363.0
- mean: 0.8095076174354633
- std: 0.12089203860051445
- min: 0.228
- 25%: 0.744
- 50%: 0.8345
- 75%: 0.904
- max: 0.987
Healthy life expectancy at birth:
- count: 2363.0
- mean: 63.44710325856962
- std: 6.756315797293227
- min: 6.72
- 25%: 59.545
- 50%: 65.1
- 75%: 68.4
- max: 74.6
Freedom to make life choices:
- count: 2363.0
- mean: 0.7505975454930174
- std: 0.13831425560919763
- min: 0.228
- 25%: 0.662
- 50%: 0.771
- 75%: 0.861
- max: 0.985
Generosity:
- count: 2363.0
- mean: -0.000659754549301734
- std: 0.15864720823860745
- min: -0.34
- 25%: -0.108
- 50%: -0.022
- 75%: 0.088
- max: 0.7
Perceptions of corruption:
- count: 2363.0
- mean: 0.7468554803216251
- std: 0.18032105258484046
- min: 0.035
- 25%: 0.696
- 50%: 0.7985
- 75%: 0.864
- max: 0.983
Positive affect:
- count: 2363.0
- mean: 0.6519949217096911
- std: 0.10570446303305288
- min: 0.179
- 25%: 0.573
- 50%: 0.663
- 75%: 0.7364999999999999
- max: 0.884
Negative affect:
- count: 2363.0
- mean: 0.2730753279729158
- std: 0.08684027838928517
- min: 0.083
- 25%: 0.209
- 50%: 0.262
- 75%: 0.326
- max: 0.705
```

## Data Preprocessing
The following preprocessing steps were conducted to clean and prepare the data:

- **Missing Values Handling**: Missing values in categorical columns were replaced with 'Unknown'. Numeric columns had missing values imputed using the median.
- **Date Parsing**: Any columns containing dates were parsed and converted into datetime objects.
- **Standardization**: Numerical data was standardized to ensure that features are on the same scale before applying clustering algorithms.
### Cluster Distribution
The following plot shows the distribution of data points across the clusters:

![Cluster Distribution](cluster_distribution.png)

## Visualizations
The following visualizations help in understanding the data distribution and clustering results:

### Correlation Heatmap
This heatmap shows the correlation between numerical features in the dataset.

![Correlation Heatmap](correlation_heatmap.png)

## Narrative Summary
Below is the narrative generated from the dataset analysis:

### Insights
```
An error occurred while generating the narrative.
```

## Conclusion
The analysis provides insights into the dataset, revealing key patterns and relationships. The clustering analysis provided segmentation insights, and visualizations helped in understanding the data distribution. Further exploration could involve testing other clustering methods or optimizing the preprocessing steps.
