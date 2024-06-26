# ECG Signals Classification using Feature Extraction
In this project, a large and widely available ECG dataset, [2017 PhysioNet](https://physionet.org/challenge/2017/), has been utilized as train set to solve a binary classification task between Normal and Atrial Fibrillation. Although this dataset contains 4 classes, we only used the data of two classes; Normal, and Atrial Fibrillation. We utilized this data as train set since we did not have sufficient amount of ECG signals. After training multiple classifiers, such as MLP, KNN and SVM, we saved trained classifiers to classify our ECG signals. 
With regards to feature extraction stage, we extracted 199 features based on this [repository](https://github.com/victorkifer/ecg-af-detection-physionet-2017/tree/master/features) from Viktor Kifer, although we modified some of them based on our needs.

As the sampling rate of recorded signals by our device (130 Hz) was different from that of train set (300 Hz), we conduct upsampling on our signals in order to extract features from test set (our signals) just like train set (2017 PhysioNet signals). If, in contrast, we did not carry out upsampling on our signals, features extracted from test set would not become compatible with classifiers which had been trained based on features extracted from 2017 PhysioNet dataset. 


