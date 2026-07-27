# Factor-Analysis-Organic-Food-Study
Factor Analysis of partial field study data on Understanding consumer resistance to the consumption of organic food : A study of ethical consumption, purchasing, and choice behaviour.

## Research Objective: 
To identify latent constructs (barriers) behind observed questionnaire items for Understanding Consumer Resistance to the Consumption of Organic Food.
Identify underlying factors influencing consumer perception toward organic food.

## Data Collection: 
Primary data taken as a limited sample from data collected for the research work undertaken by researchers: Shiksha Kushwaha, Amandeep Dhirb, Mahim Sagar for “Understanding consumer resistance to the consumption of organic food. A study of ethical consumption, purchasing, and choice behaviour”. 

- Based on Structured Questionnaire with Likert Scale (1-7)
- Sample size : 73 Responses (rows of data)
- Questions Considered : 18 (columns of data)

> **Note:** The dataset is not included in this repository due to licensing and repository size limitations.


## Bartlett’s Test of Sphericity

Chi-square Value = 878.6747502638859
- Tests whether correlation matrix is an identity matrix.
- Very high value
- Strong deviation from identity matrix
- High inter-correlation among variables

P-value = 2.9978044574006208e-102
- This p-value is far below 0.05
- The correlation matrix is not identity matrix
- So there is underlying latent structure
- Strong interrelationships
- High chance of meaningful factor extraction

Bartlett’s Test of Sphericity is highly significant, indicating that the correlation matrix is not an identity matrix. The extremely low p-value confirms the presence of strong correlations among variables, validating the suitability of the dataset for factor analysis.


## Kaiser-Meyer-Olkin (KMO) Test

KMO = 0.7635258799210928
- KMO falls in “Good / Acceptable” range
- So data is adequately suitable for factor analysis
- There is sufficient shared variance
- Factor extraction will be reasonably reliable

The KMO (Kaiser, Henry F., 1974) measure of sampling adequacy is 0.764 approx, indicating a good level of common variance among variables and confirming the suitability of the dataset for factor analysis. 


## Method : Principal Component Analysis (PCA)
PCA is a dimensionality reduction technique and helps us to reduce the number of features in a dataset while keeping the most important information. It changes complex datasets by transforming correlated features into a smaller set of uncorrelated components.

<img width="1536" height="1024" alt="PCAdescription" src="https://github.com/user-attachments/assets/c1426414-8f11-4883-acfd-6a9d37a6d766" />

- PCA uses linear algebra to transform data into new features called principal components.
- It finds these by calculating eigenvectors (directions) and eigenvalues (importance) from the covariance matrix.
- PCA selects the top components with the highest eigenvalues and projects the data onto them simplify the dataset.

## Eigenvalues:

[6.78300873 | 2.65233998 | 1.58737174 | 1.46080355 | 1.00225284 | 0.89706132 | 0.74046103 | 0.55501324 | 0.40696955 | 0.39909063 | 0.3464222  | 0.28296436 | 0.24772289 | 0.19155505 | 0.15219382 | 0.13626164 | 0.10183697 | 0.05667044]

## Determining Number of Factors

From Scree Plot, observations are:
- Sharp drop initially (Factor 1 to Factor 3) Eigenvalue drops steeply from ~6.8 (Factor 1) to ~1.6 (Factor 3).
- This indicates the first few factors explain a large portion of variance.
- Elbow point: The curve starts to flatten after Factor 3 or 4.
- Eigenvalue > 1 rule (Kaiser Criterion)
- After Factor 5, eigenvalues drop below 1.

## Correlation Heatmap for Factors

It is observed that:
- Most correlations are moderate (0.3–0.7) which makes it suitable for factor analysis
- Very few extreme correlations (>0.9), so no severe multicollinearity
- Clear cluster patterns visible → strong factor structure exists
The correlation heatmap reveals distinct clusters of variables representing health perception, purchase intention, environmental behavior, and skepticism

## Factor Loadings
Starting with recommended 4 factors >>  Applying Rotation >> Factor Loadings

## Contrast in Pre-PCA to Post-PCA Plot

Before PCA: 
- Using the First 2 Standardized Features as the x and y axes where each point represents a data instance. 
- This plot gives a direct look at the spread and relationship between these two specific original features.
 Having taken the elements in their original form prior to denoting principal components.

After PCA: Projected onto 2 Principal Components,
- This plot shows the same data points, but now they’re represented in a new coordinate system defined by the first two principal components (PC1 and PC2). 
- Principal components are new variables constructed as linear combinations of the original variables. - PC1 (x-axis) captures the most variance in the data, and PC2 (y-axis) captures the second most variance, orthogonal to PC1. 
- The goal of PCA is to find these components that best summarize the data's variability. 

We see the underlying structure of data in a reduced dimension, revealing clusters or patterns that are not obvious in the original high-dimensional space.

## Cronbach’s Alpha Reliability Test
PCA reduces data to identify underlying components, while Cronbach’s alpha checks if items within those components consistently measure the same construct.

- Output:
(np.float64(0.8148333000598921), array([0.727, 0.878]))

Here, [ 0.815 > 0.7 ]

-  A high alpha (>0.8) indicates strong internal consistency
- This shows that the items in the PCA component are highly correlated.

## Conclusion : PCA Interpretation

Final Principal Components Identified:
- PC1 = “Pro-Organic Orientation” factor
- PC2 = “Skepticism vs Green Behavior” factor

- Interpretation of PC1 - High loadings (approx ≥ 0.25)
Theme: Positive Attitude + Purchase Intention toward Organic/Ethical Products
This component combines:
a) Beliefs (healthy, natural)
b) Behavioral intent (buy, plan, consume)
c) Ethical orientation


- Interpretation of PC2 (Principal Component 2) - High positive & negative loadings
Theme: Skepticism vs Environmental Commitment
Herein, 
Positive side (Distrust / skepticism)
Negative side (Actual eco-friendly behavior)












