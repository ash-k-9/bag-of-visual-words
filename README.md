# bag-of-visual-words
## Introduction
The project uses Bag of Visual Words (BOVW) technique for image classification. BOVW is a technique used in computer vision for image classification and retrieval tasks. It is based on the concept of bag of words (BOW) commonly used in information retrieval and natural language processing (NLP). In BOVW, an image is represented as a set of visual features, i.e. descriptors and keypoints. These features are extracted using techniques like Oriented FAST and Rotated BRIEF (ORB), Speeded Up Robust Feature (SURF), or Scale-Invariant Feature Transform (SIFT). The features are then clustered into a set of visual words, using unsupervised learning techniques mostly k-means clustering. Each image is then represented as a histogram of visual word occurrences, where the frequencies of each visual word represent the image's features. The histograms can be used to train a machine learning classifier for image classification tasks or to search for similar images. BOVW is a powerful technique for image classification and retrieval, and it has been used successfully in many applications, such as object recognition, scene classification, and image retrieval.
## Steps to Classify Images Using BOVW
![Methodology](https://user-images.githubusercontent.com/127419841/224563824-8badf6b4-c2e8-49d7-8636-278922f763e5.png)

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
## Quantitative Results 

**SVM Classifier**

Object Dataset

1. Accuracy: 75%
2. F1 Score: 0.74
3. True Positive: [5 6 6 5]
4. False Positive: [1 1 0 0]

Flower Dataset

1. Accuracy: 56.81%
2. F1 Score: 0.57
3. True Positive: [572 457 547 549 494]
4. False Positive: [82 44 62 54 75]

**Randon Forest Classifier**

Object Dataset

1. Accuracy: 75%
2. F1 Score: 0.75
3. True Positive: [4 6 6 6]
4. False Positive: [0 1 0 1]

Flower Dataset

1. Accuracy: 53%
2. F1 Score: 0.53
3. True Positive: [563 460 555 525 488]
4. False Positive: [75 54 74 60 82]

## Visual Results
**Objects Dataset**

###### Image and keypoints in the image

![Objects-Keypoints-Image](https://user-images.githubusercontent.com/127419841/224568746-7be902f5-dfe4-4be3-981c-a3b43b7c54ed.png)

###### Vocabulary
![Objects-Vocabulary](https://user-images.githubusercontent.com/127419841/224569691-6310dcab-0ae2-4dba-9efc-643d61b4ae6d.png)

###### Confusion Matrix 

SVM Classifier:

![Objects-Confusion-SVM](https://user-images.githubusercontent.com/127419841/224569658-27030fe8-d00f-499f-bed5-14eca109a266.png)

Random Forest Classifier:

![Objects-Confusion-RFC](https://user-images.githubusercontent.com/127419841/224569059-b2a6f78c-fe31-4076-8d39-b46cf92b98d4.png)

**Flower Dataset**

###### Image and keypoints in the image

![Flowers-Keypoints-Image](https://user-images.githubusercontent.com/127419841/224569754-77f27d3d-f1ea-4afd-a405-585507750f3c.png)

###### Vocabulary
![Flowers-Vocabulary](https://user-images.githubusercontent.com/127419841/224569005-7eacf73a-c3ec-4281-a712-124d17e4858a.png)

###### Confusion Matrix 

SVM Classifier:

![Objects-Confusion-SVM](https://user-images.githubusercontent.com/127419841/224569658-27030fe8-d00f-499f-bed5-14eca109a266.png)

Random Forest Classifier:

![Objects-Confusion-RFC](https://user-images.githubusercontent.com/127419841/224569059-b2a6f78c-fe31-4076-8d39-b46cf92b98d4.png)
