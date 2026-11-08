# K-means Clustering of Penguins

Unsupervised learning project that uses K-means to group penguins by physical measurements and sex, then checks how well the clusters match known species.

## Overview

The dataset covers 344 penguins from three species (Adelie, Chinstrap, Gentoo) with bill length, bill depth, flipper length, body mass, island and sex. The goal is to see whether K-means, without being given species labels, finds meaningful groups.

## Workflow

1. Load the data and run basic exploration
2. Drop rows with missing values (333 penguins remain)
3. Encode `sex` with one-hot encoding and drop `island`
4. Scale features with `StandardScaler`
5. Fit K-means for k = 2 to 10 and compare inertia (elbow method)
6. Compare silhouette scores for each k
7. Fit the final model and compare clusters against `species` and `sex`

## Results

- The elbow plot and silhouette score both point to **k = 6** (silhouette score about 0.53).
- Each of the six clusters is almost entirely one species and one sex, for example Adelie female or Gentoo male.
- This shows that species and sex both drive physical differences in the sample.

## Files

| File | Description |
| --- | --- |
| `Activity_Build_a_K-means_model_completed.ipynb` | notebook  |
| `penguins.csv` | Penguin dataset used by in the notebook |

## Run it

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook Activity_Build_a_K-means_model_completed.ipynb
```

penguins.csv

## Tools

Python, pandas, NumPy, scikit-learn, seaborn, matplotlib

## Reference

Gorman, K. B., et al. (2014). Ecological Sexual Dimorphism and Environmental Variability within a Community of Antarctic Penguins (Genus Pygoscelis). *PLOS ONE*, 9(3), e90081. https://doi.org/10.1371/journal.pone.0090081

## Author

Boston Palanga ([@bpalanga](https://github.com/bpalanga))
