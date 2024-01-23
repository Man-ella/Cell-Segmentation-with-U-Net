# Cell-Segmentation-with-U-Net
Background & Motivation
Fast and efficient cell identification and segmentation has become important in attempts to explore the role of cellular heterogeneity in dynamic living systems.
Manual methods of cell segmentation are tedious, time consuming and prone to more errors
The advancement of machine learning is providing an efficient approach to cell segmentation.
This project creates and trains a deep learning neural network, U-Net, to perform cell segmentation.

Dataset
The entire model makes use of 7590 samples divided into three different sets: 
Validation, Testing & Training datasets in the ratio 1 : 1.5 : 3
Training dataset has 4140 samples
Validation dataset has 1380 samples
Testing dataset has 2070 samples
Each sample consists of an image 
and a corresponding image mask

Highlevel Approach
U-Net used a Binary Cross-Entropy (log) loss function since this project is a binary classification method. A Categorical Cross-Entropy loss function wasn’t optimal since this cell segmentation method has only two classes.
Utilized the ADAM optimization algorithm since it’s the most efficient method and is a combination of Adadelta, RMSProp and Adagrad.
Training in batches for 50 epochs and used weights from the best epoch (highest validation DICE score) to finalize the model
