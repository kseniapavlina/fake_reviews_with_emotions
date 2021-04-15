# Fake Reviews Classification with Emotion Features

This repository contains code and data used for completion of final year project on exploration of emotion feature influence in fake review detection for Amazon reviews.

The repository is organised as follows:
- <tt>data</tt> contains all datasets (and some plots) used to obtain classification results and obtained throughout the project. Within the directory, the following files can be located:
	- <tt>BERT\_plots</tt> - a directory containing plots obtained from training a BERT classifier (i.e., confusion matrices, classification reports, and learning rate search plot)
	- <tt>preprocessed</tt> - contains \texttt{amazon.csv} file - a cleaned version of Amazon dataset used for veracity predictions.
	- <tt>results</tt> - contains intermediate and final emotion classification results. In particular, <tt>amazon\_final.csv</tt> is the final dataset obtained from cross-referencing results of chosen classifiers, and the rest of the files contain results associated with a single classifier depicted in the name of the file.
	- <tt>training_data</tt> - contains datasets used for emotion classification (granularity of 5, 7, and 13 classes). Dataset sources: 5 classes - https://github.com/lukasgarbas/nlp-text-emotion, 7 classes - https://www.aclweb.org/anthology/I17-1099/, 13 classes - https://data.world/crowdflower/sentiment-analysis-in-text.
	- <tt>amazon\_initial.csv</tt> - dataset containing Amazon reviewed labelled with veracity. Source: https://www.kaggle.com/lievgarcia/amazon-reviews.
	- <tt>amazon\_samples.csv</tt> - samples used for manual labelling by volunteers.
	- <tt>amazon\_sample\_responses.csv</tt> - anonymised responses obtained from volunteers asked to assign emotion to each of the selected Amazon samples.
- <tt>scripts</tt> - contains all code used to complete the project. The folder is organised as follows:
	- <tt>classification\_analysis</tt> - contains scripts related to obtained results analysis. In particulat, <tt>emotion\_prediction\_accuracy</tt> examines how the final emotion dataset compares to classification results obtained from volunteers. <tt>multitask\_model</tt> is a script examining how emotion classification relates to veracity prediction by constructing a multitask model completing both tasks simultaneously. <tt>performance\_improvement\_significance</tt> is used to determine whether observed accuracy changes from introducing emotion classification features are statistically significant. Finally, <tt>results\_examination</tt> script is used to explore produced emotion classification and examine statistical patterns in the obtained data.
	- <tt>emotion\_classification</tt> contains scripts for intermediate emotion classification results with BERT, CNN, GRU, and DepecheMood WordNet.
	- <tt>omitted\_model\_scripts</tt> contains the scripts and classification results for the models that were not used in the construction of final emotion dataset due to poor performance.
	- <tt>veracity\_prediction</tt> directory contains scripts for obtaining veracity predictions on traditional ML algorithms and deep learning models. All models make predictions based on textual features alone or textual features combined with emotion features.
	- <tt>final\_dataset\_construction</tt> is a script for cross-referencing intermediate emotion classification results.
	- <tt>intial\_data\_cleaning</tt> is a script for preprocessing intial Amazon reviews dataset.
	- <tt>review\_samples</tt> is a script to obtain a set of random samples for manual labelling.
- <tt>trained\_models</tt> directory contains all models used to produce final emotion classification. Note: due to large size, BERT models were uploaded to Google Drive instead. They can be accessed on https://drive.google.com/drive/folders/1stJHVn8c78_cPGqI5AtYaxaqf3TKldIZ?usp=sharing.