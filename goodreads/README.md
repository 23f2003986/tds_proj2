# Automated Dataset Analysis

## Overview
This folder contains an analysis of the dataset **goodreads.csv**. The following sections describe the preprocessing steps, the analysis conducted, clustering results, visualizations, and insights derived from the data.

## Dataset Summary
The dataset consists of the following structure:

### Data Overview
- Total Rows: 10000
- Total Columns: 23
### Column Data Types
```
- book_id: float64
- goodreads_book_id: float64
- best_book_id: float64
- work_id: float64
- books_count: float64
- isbn: object
- isbn13: float64
- authors: object
- original_publication_year: float64
- original_title: object
- title: object
- language_code: object
- average_rating: float64
- ratings_count: float64
- work_ratings_count: float64
- work_text_reviews_count: float64
- ratings_1: float64
- ratings_2: float64
- ratings_3: float64
- ratings_4: float64
- ratings_5: float64
- image_url: object
- small_image_url: object
```
### Missing Values
```
- book_id: 0 missing values
- goodreads_book_id: 0 missing values
- best_book_id: 0 missing values
- work_id: 0 missing values
- books_count: 0 missing values
- isbn: 0 missing values
- isbn13: 0 missing values
- authors: 0 missing values
- original_publication_year: 0 missing values
- original_title: 0 missing values
- title: 0 missing values
- language_code: 0 missing values
- average_rating: 0 missing values
- ratings_count: 0 missing values
- work_ratings_count: 0 missing values
- work_text_reviews_count: 0 missing values
- ratings_1: 0 missing values
- ratings_2: 0 missing values
- ratings_3: 0 missing values
- ratings_4: 0 missing values
- ratings_5: 0 missing values
- image_url: 0 missing values
- small_image_url: 0 missing values
```
### Numeric Summary
```
book_id:
- count: 10000.0
- mean: 5000.5
- std: 2886.8956799071675
- min: 1.0
- 25%: 2500.75
- 50%: 5000.5
- 75%: 7500.25
- max: 10000.0
goodreads_book_id:
- count: 10000.0
- mean: 5264696.5132
- std: 7575461.863589608
- min: 1.0
- 25%: 46275.75
- 50%: 394965.5
- 75%: 9382225.25
- max: 33288638.0
best_book_id:
- count: 10000.0
- mean: 5471213.5801
- std: 7827329.890719957
- min: 1.0
- 25%: 47911.75
- 50%: 425123.5
- 75%: 9636112.5
- max: 35534230.0
work_id:
- count: 10000.0
- mean: 8646183.4246
- std: 11751060.824080037
- min: 87.0
- 25%: 1008841.0
- 50%: 2719524.5
- 75%: 14517748.25
- max: 56399597.0
books_count:
- count: 10000.0
- mean: 75.7127
- std: 170.4707276502585
- min: 1.0
- 25%: 23.0
- 50%: 40.0
- 75%: 67.0
- max: 3455.0
isbn13:
- count: 10000.0
- mean: 9756530621824.22
- std: 429753045646.841
- min: 195170342.0
- 25%: 9780330413197.5
- 50%: 9780451528640.0
- 75%: 9780807760637.5
- max: 9790007672390.0
original_publication_year:
- count: 10000.0
- mean: 1982.0339
- std: 152.4196907456574
- min: -1750.0
- 25%: 1990.0
- 50%: 2004.0
- 75%: 2011.0
- max: 2017.0
average_rating:
- count: 10000.0
- mean: 4.002191000000001
- std: 0.25442748053872877
- min: 2.47
- 25%: 3.85
- 50%: 4.02
- 75%: 4.18
- max: 4.82
ratings_count:
- count: 10000.0
- mean: 54001.2351
- std: 157369.95643554686
- min: 2716.0
- 25%: 13568.75
- 50%: 21155.5
- 75%: 41053.5
- max: 4780653.0
work_ratings_count:
- count: 10000.0
- mean: 59687.3216
- std: 167803.7852374182
- min: 5510.0
- 25%: 15438.75
- 50%: 23832.5
- 75%: 45915.0
- max: 4942365.0
work_text_reviews_count:
- count: 10000.0
- mean: 2919.9553
- std: 6124.378131569907
- min: 3.0
- 25%: 694.0
- 50%: 1402.0
- 75%: 2744.25
- max: 155254.0
ratings_1:
- count: 10000.0
- mean: 1345.0406
- std: 6635.626262783453
- min: 11.0
- 25%: 196.0
- 50%: 391.0
- 75%: 885.0
- max: 456191.0
ratings_2:
- count: 10000.0
- mean: 3110.885
- std: 9717.123578396895
- min: 30.0
- 25%: 656.0
- 50%: 1163.0
- 75%: 2353.25
- max: 436802.0
ratings_3:
- count: 10000.0
- mean: 11475.8938
- std: 28546.44918318239
- min: 323.0
- 25%: 3112.0
- 50%: 4894.0
- 75%: 9287.0
- max: 793319.0
ratings_4:
- count: 10000.0
- mean: 19965.6966
- std: 51447.35838380065
- min: 750.0
- 25%: 5405.75
- 50%: 8269.5
- 75%: 16023.5
- max: 1481305.0
ratings_5:
- count: 10000.0
- mean: 23789.8056
- std: 79768.88561077177
- min: 754.0
- 25%: 5334.0
- 50%: 8836.0
- 75%: 17304.5
- max: 3011543.0
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
