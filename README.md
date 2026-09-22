# Exoplanet Transit Classifier
## **Overview**

A machine learning classifier that distinguishes confirmed exoplanets from false positives using Kepler transit data. Achieved ROC-AUC of 0.940 with a Random Forest model

## **Data**

Source: NASA Exoplanet Archive KOI cumulative table
Size: 7,328 signals after filtering

Key features used: orbital period, transit depth, duration, radius ratio, equilibrium temperature, insolation

## **Approach**

Random Forest (100 trees, max_depth=10)

Stratified 80/20 train-test split

6 physically meaningful features

## **Results**

ROC-AUC: 0.940

Feature importance: koi_ror (planet-to-star radius ratio) was the strongest predictor at 0.30, consistent with eclipsing binary false positives producing anomalously large radius ratios

## **Files**

transit_classifier.ipynb : full analysis

koi_cumulative.csv : raw data from NASA
