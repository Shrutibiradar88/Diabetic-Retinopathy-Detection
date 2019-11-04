# Diabetic-Retinopathy-Detection

Here is a short summary of the work done on this project.
The first file EDA.ipynb is mean for exploratory analysis of this dataset. Here I have used two commoonly used techniues of PCA and 
TSNE to visualize how data points look and if any meaningful clusters are apparent.
This may help us in seeing whether there is apparent class seperation between classes.

The link to this file can be found here https://nbviewer.jupyter.org/github/shivayogibeeradar/Diabetic-Retinopathy-Detection/blob/master/EDA.ipynb

The second file is implementation of Resnet50 with downsampling of classes to 700 for each category.
The acurracy was low but quadratic kappa score was negative which indicated that the predictionas werent accurate and at the same time
the balance in the predictionas was also missing.

Th link to this file can be found here : 
https://nbviewer.jupyter.org/github/shivayogibeeradar/Diabetic-Retinopathy-Detection/blob/master/fastai-downsampling%20modelling.ipynb

The third file inculdes a list of preprocessing steps that I tried using open cv on this dataset.
The link to this file can be found here :
https://nbviewer.jupyter.org/github/shivayogibeeradar/Diabetic-Retinopathy-Detection/blob/master/Preprocessing.ipynb

I then tried the resnet model again but using the best of preprocessing steps that is brightening the image around the mean for all images.

The quadratic kappa score rose from negative and so did accuracy.However the quadratic kappa was zero and on further inspection I 
found that model was predicting only one class.

The link to the notebook can be found here :
https://nbviewer.jupyter.org/github/shivayogibeeradar/Diabetic-Retinopathy-Detection/blob/master/fastai%20downsampling%20with%20preprocessing.ipynb

Finally , I decided to use Data Augmentation to reduce bias and used image preporcessing in the previous step with random oversampling of all classes.

This model took approximately 6 hours to train but had the best result amongst all the techniques trued so far.

The accuracy was close to 0.51 but quadratic kappa score was 0.69 ( yes positive !!) which is a descent benchmark for this problem and high kappa score 
meant were making somewhat balanced predictions as was corroborated by confusion matrix plot in the notebbok.

The notebook link can be found here :
https://nbviewer.jupyter.org/github/shivayogibeeradar/Diabetic-Retinopathy-Detection/blob/master/Reset50_oversample.ipynb

For any further clarifications please feel free to revert me at biradar.s@husky.neu.edu



