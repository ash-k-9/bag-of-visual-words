# bag-of-visual-words
## Steps to Classify Images Using BOVW
The following steps have been taken to implement image classification using bag of visual words
1.	Image Preprocessing: Convert the input images to a suitable representation for feature extraction, in this project the images are converted into grayscale.
2.	Feature Extraction: Extract local features from the preprocessed images using a SIFT as the feature detection algorithm.
3.	Codebook Creation: Cluster the extracted features using k-means clustering algorithm to form a vocabulary.
4.	Histogram Generation: Compute a histogram of visual words for each image, where the histogram bins correspond to the codebook clusters, and the bin counts represent the frequency of each visual word in the image.
5.	Machine Learning using SVM and Random Forest: Train SVM or Random Forest classifiers, using the normalized histograms as input to classify images.
6.	Testing: Evaluate the performance of the machine learning model on a separate set of test images, using metrics such as accuracy, confusion matrix (true positive and false positive) and F1-score.
