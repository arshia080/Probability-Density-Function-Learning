# Probability-Density-Function-Learning

## Objective
The objective of this assignment is to learn the parameters of a probability density function using a roll-number-parameterized non-linear transformation applied to real-world air quality data.

## Dataset
The dataset used is the India Air Quality Data, which contains air pollution measurements collected from multiple locations across India.
For this assignment, NO₂ concentration values are selected as the feature of interest.

## Data Preprocessing
The NO₂ column contains missing and non-numeric entries.
These entries are removed to ensure that only valid numeric values are used for probability density estimation.

## Data Transformation
Each NO₂ value 𝑥 is transformed into a new variable 𝑧 using the following roll-number-dependent transformation: z=x+ar*​sin(br*​x)
The parameters 𝑎𝑟 and 𝑏𝑟 are computed using my university roll number.
This transformation introduces controlled non-linearity while preserving the overall structure of the data.

## Probability Density Model
The transformed variable 𝑧 is modeled using a Gaussian-style probability density function: p(z)= c⋅e^(−λ(z−μ)^2)
The parameters 𝜆, 𝜇, and 𝑐 are learned from the data.

## Methodology
1. NO₂ concentration values were extracted after removing invalid entries.
2. A roll-number-based non-linear transformation was applied to obtain the variable 𝑧.
3. The parameters of the probability density function were estimated using Maximum Likelihood Estimation (MLE).
4. The learned parameters define a theoretical probability distribution for the transformed data.
5. A histogram of the transformed data was plotted along with the learned PDF for visualization.

## Parameter Interpretation
- μ (Mean): Represents the central tendency of the transformed NO₂ values
- σ² (Variance): Indicates the spread of pollution levels
- λ (Lambda): Controls the width of the probability density curve
- c: Scaling constant that ensures the probability density function is valid

## Result Graph
A histogram of the transformed variable 𝑧 represents the empirical distribution of the data.
The learned probability density function is overlaid to visualize how well the theoretical model approximates the observed values.
<img width="871" height="496" alt="image" src="https://github.com/user-attachments/assets/97e7bae7-389f-4059-8d39-3b850cc8c63e" />

## Observations
- The distribution of the transformed NO₂ values is right-skewed.
- Most observations are concentrated at lower pollution levels.
- A long right tail indicates the presence of high pollution values.
- The Gaussian-style model provides an approximate representation but does not perfectly capture skewness.

## Conclusion
This assignment demonstrates how probability density functions can be learned from real-world environmental data.
Although theoretical distributions provide useful approximations, air quality data often exhibits skewness and extreme values.
The results highlight the difference between ideal statistical models and real-world observations.
