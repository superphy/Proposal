	 	 	 	
Bio
I am Gates Kempenaar and I am a 3rd year Computer Science student at the University of Lethbridge. During this term I will be developing tools to predict minimum inhibitory concentration (MIC) for thirteen different antimicrobial agents using genome sequences.
I I will focus  on Salmonella enterica serovars Kentucky and Heidelberg, and test how dataset composition affects performance.
Introduction
S. enterica is a foodborne pathogen that causes gastrointestinal infections such as: typhoid fever, paratyphoid fever, and salmonellosis In Canada alone 88,000 people contract salmonella each year, resulting in 925 hospitalizations and 17 deaths (are these numbers averages or for a particular year?) (4).

The Heidelberg and Kentucky serovars are most commonly found in North America. They have an increased antimicrobial resistance (AMR) (compared to other Salmonella?) and are multiple-drug resistant (MDR) (3,5). The amount of antimicrobial agent required to prevent bacterial growth is refered to as the MIC. MIC values are currently determined using laboratory tests that are costly and time consuming (6). 

(Whole genome sequencing is becoming routine etc …) WGS can be used directly to identify MIC values for bacteria of different species eg. … (ref to other species), as well as for groups within a species. 
In this coop term I will be using publicly available, and Canadian WGS data sets generated as part of the Genomics Research and Development Initiative on AMR, with their accompanying MIC values. I will be focusing on the S. enterica serovars Heidelberg and Kentucky because ….. . (Enteritidis and Typhimurium are the most prevalent, you need to identify why you are focusing on Kentucky and Heidelberg)

WGS data will be reformatted for use in supervised machine learning models that will be used to predict MIC values.
Implementation
I will be using machine learning because it is fast, scalable, and only requires WGS data combined with a corresponding MIC value to be able to make a prediction. The raw WGS data will be converted to a numeric input based on the frequency of DNA sequence substrings in the genome (k-mer)  Counts of k-mers with length 11 will be computed for each genome using the program Jellyfish (7). A k-mer length of 11 was  previously found to be optimal.

We will use two machine learning methods: Gradient Boosted Decision Trees (XGBoost) (8), and artificial neural networks (ANN). (Give a brief explanation as to how each work) The XGBoost model will be used as implemented in … and the ANN using Keras (10), TensorFlow (11), and scikit-learn (12).
Conclusion
Successful completion of this project will lead to faster and more accurate MIC predictions based solely on genome sequence data. This could decrease the cost and reduce testing times, leading to healthier Canadians.

References 
1.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4643846/
2.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5047448/
3.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5622158/
4.	https://www.foodnavigator.com/Article/2015/08/10/Canadian-research-on-Salmonella-gets-grant
5.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1082862/
6.	https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4503790/
7.	https://github.com/gmarcais/Jellyfish
8.	https://xgboost.readthedocs.io/en/latest/
9.	https://keras.io/
10.	https://www.tensorflow.org/
11.	http://scikit-learn.org/stable/index.html
