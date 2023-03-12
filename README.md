# bag-of-visual-words
## Introduction
The project uses Bag of Visual Words (BOVW) technique for image classification. BOVW is a technique used in computer vision for image classification and retrieval tasks. It is based on the concept of bag of words (BOW) commonly used in information retrieval and natural language processing (NLP). In BOVW, an image is represented as a set of visual features, i.e. descriptors and keypoints. These features are extracted using techniques like Oriented FAST and Rotated BRIEF (ORB), Speeded Up Robust Feature (SURF), or Scale-Invariant Feature Transform (SIFT). The features are then clustered into a set of visual words, using unsupervised learning techniques mostly k-means clustering. Each image is then represented as a histogram of visual word occurrences, where the frequencies of each visual word represent the image's features. The histograms can be used to train a machine learning classifier for image classification tasks or to search for similar images. BOVW is a powerful technique for image classification and retrieval, and it has been used successfully in many applications, such as object recognition, scene classification, and image retrieval.
## Steps to Classify Images Using BOVW
The following steps have been taken to implement image classification using bag of visual words
1.	Image Preprocessing: Convert the input images to a suitable representation for feature extraction, in this project the images are converted into grayscale.
2.	Feature Extraction: Extract local features from the preprocessed images using a SIFT as the feature detection algorithm.
3.	Codebook Creation: Cluster the extracted features using k-means clustering algorithm to form a vocabulary.
4.	Histogram Generation: Compute a histogram of visual words for each image, where the histogram bins correspond to the codebook clusters, and the bin counts represent the frequency of each visual word in the image.
5.	Machine Learning using SVM and Random Forest: Train SVM or Random Forest classifiers, using the normalized histograms as input to classify images.
6.	Testing: Evaluate the performance of the machine learning model on a separate set of test images, using metrics such as accuracy, confusion matrix (true positive and false positive) and F1-score.
## Instructions to setup the environment for running code
The datasets need to be uploaded on google drive prior to the ode being executed on google colab.
In order to run download the code and open the notebook in google colabs
