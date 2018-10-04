	 	 	 	
### Bio
I am Gates Kempenaar and I am a 3rd year Computer Science student at the University of Lethbridge. During this term I will be developing tools to predict minimum inhibitory concentration (MIC) for thirteen different antimicrobial agents using genome sequences.
I will focus  on Salmonella enterica serovars Kentucky and Heidelberg, and test how dataset composition affects performance.

### Introduction
S. enterica is a foodborne pathogen that causes gastrointestinal infections such as: typhoid fever, paratyphoid fever, and salmonellosis. In Canada 2016 alone an estimated 87,500 people contract salmonella each year, resulting in 925 hospitalizations and 17 deaths (3).

The Heidelberg and Kentucky serovars are most commonly found in North America. They have an increased antimicrobial resistance (AMR) over the past few years compared to other servars of S. Enterica as well as being multiple-drug resistant (MDR) (1,2,4). The amount of antimicrobial agent required to prevent bacterial growth is refered to as the MIC. MIC values are currently determined using laboratory tests that are costly and time consuming (5). Whole genome sequencing (WGS) is becoming routine for obtaining a genome sequence in humans and animals. WGS can be used directly to identify MIC values for bacteria of different species eg. Salmonella Enterica and Salmonella Bongori, as well as for groups within a species. 

In this coop term I will be using publicly available, and Canadian WGS data sets generated as part of the Genomics Research and Development Initiative on AMR, with their accompanying MIC values. I will be focusing on the S. enterica serovars Heidelberg and Kentucky because of their recently increased AMR and MDR (1,2,4)

WGS data will be reformatted for use in supervised machine learning models that will be used to predict MIC values.

### Implementation
I will be using machine learning because it is fast, scalable, and only requires WGS data combined with a corresponding MIC value to be able to make a prediction. The raw WGS data will be converted to a numeric input based on the frequency of DNA sequence substrings in the k-mer. Counts of k-mers with length 11 will be computed for each genome using the program Jellyfish (6). A k-mer length of 11 was  previously found to be optimal.

We will use two machine learning methods: Gradient Boosted Decision Trees (XGBoost) (7) and artificial neural networks (ANN). XGBoost uses an ensamble of weaker decision trees that when working together to answer a series of true or false questions create a strong model to make a prediction. While an ANN uses layers of neurons with corresponding weights to make a prediction based on specified input neurons. The XGBoost model will be used as implemented using the XGBoost Python package and the ANN using Keras (8), TensorFlow (9), and scikit-learn (10).

### Conclusion
Successful completion of this project will lead to faster and more accurate MIC predictions based solely on genome sequence data. This could decrease the cost and reduce testing times, leading to healthier Canadians.

### References 
1.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5047448/
2.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5622158/
3.	https://www.canada.ca/en/public-health/services/food-borne-illness-canada/yearly-food-borne-illness-estimates-canada.html
4.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1082862/
5.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4503790/
6.	https://github.com/gmarcais/Jellyfish
7.	https://xgboost.readthedocs.io/en/latest/
8.	https://keras.io/
9.	https://www.tensorflow.org/
10.	http://scikit-learn.org/stable/index.html
