# World Happiness Report 2023 - Principal Component Analysis

## Project description
This project performs Principal Component Analysis (PCA) on the World Happiness Report 2023 dataset to explore relationships between different factors contributing to national happiness scores in 2022

## Dataset
The following analysis is based on a dataset for [World Happiness Report 2023](https://worldhappiness.report/ed/2023/#appendices-and-data). It contains the following columns:

1. **Country name**: 114 countries in 2022
2. **Year**: from 2005 and 2022
3. **Life Ladder**: the answer of the question is "Please imagine a ladder, with steps numbered from 0 at the bottom to 10 at the top. The top of the ladder represents the best possible life for you and the bottom of the ladder represents the worst possible life for you. On which step of the ladder would you say you personally feel you stand at this time?"
4. **Log of GDP per capita**: extend the GDP-per-capita time series from 2021 to 2022 by incorporating country-specific forecasts of real GDP growth in 2022 and then take the logarithm
5. **Healthy Life Expectancy**: Healthy life expectancies at birth are based on the data extracted from the World Health Organization's (WHO) Global Health Observatory data repository. To get the data for 2022, extrapolation was performed  
6. **Social support**: the average of the binary responses (either 0 or 1) to the question "If you were in trouble, do you have relatives or friends you can count on to help you whenever you need them, or not?"
7. **Freedom to make life choices**: the national average of responses to the question "Are you satisfied or dissatisfied with your freedom to choose what you do with your life?"
8. **Generosity**: the residual of regressing national average of response to the question "Have you donated money to a charity in the past month?" on GDP per capita. 
9. **Corruption Perception**: the national average of the survey responses to two questions "Is corruption widespread throughout the government or not" and "Is corruption widespread within businesses or not?" 

More detailed description of the dataset can be found in [Statistical Appendix 1 for Chapter 2](https://worldhappiness.report/ed/2023/#appendices-and-data)

## Analysis
The notebook performs the following steps:
1. Data cleaning and preprocessing
2. Standardisation of features
3. PCA implementation using both NumPy and scikit-learn
4. Visualization of results with interactive plots
5. Analysis of principal components by continent and happiness scores

## Findings
- The first two principal components explain a significant portion of the variance in the data
- PC1 represents a 'well-being versus corruption' axis
- PC2 captures 'generosity-driven resilience and freedom'
- Clear continental patterns emerge in the PCA projection

## File Structure
* `data`
    * `DataForTable2.1WHR2023.xls`: Raw data
    * `WHR+23_Statistical_Appendix.pdf`: Schema for the dataset
    * `WHR+23_Ch2.pdf`: Chapter 2 of World Happiness Report 2023
* `Method.md`: Detailed explanation of PCA methodology and implementation steps
* `Result.ipynb`: Jupyter notebook containing data analysis, visualizations, and findings

## Requirements
* numpy
* pandas
* scikit-learn
* seaborn
* matplotlib
* plotly
* pycountry_convert