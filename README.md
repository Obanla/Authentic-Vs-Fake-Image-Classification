# Authentic-Vs-Fake-Image-Classification
This project belongs to a series of projects on classsification in machine learning. Here using deep learning techniques, the aim is to determine which Convolutional Neural Network works best for the task of classifying fake and authentic images. This project analyzes the performance of two state of the art Convolutional Neural Network Models for this classfication task; The ResNet-18 and VGG-16 CNN Models. By establishing which of these two CNN models performs best, improving the accuracy of results in the digital forensics and medical imaging can be achieved.   
## Datasets
The CASIA v2.0 dataset was used for this project. It consists of 12,323 images, with 5,123 forged and 7,200 authentic images. The dataset includes tampered images created via splicing (copy-paste operations) with post-processing techniques such as rotation, resizing, and blurring to make detection more challenging. Images were resized to 
128
×
128
128×128 pixels for uniformity and computational efficiency. Data augmentation techniques (e.g., flipping, rotation, cropping, brightness/contrast adjustments) and Error Level Analysis (ELA) were applied to enhance feature extraction and improve model generalization.

## Method
The methodology involved training two pre-trained CNN models—ResNet-18 and VGG-16—on the CASIA v2.0 dataset using transfer learning. Key steps included:
### Preprocessing: Resizing images, data augmentation, ELA application, and addressing class imbalance by assigning higher weights to minority classes.
### Model Architecture:
#### ResNet-18: Utilized residual blocks with skip connections to address vanishing gradient issues.
#### VGG-16: A deeper architecture with sequential convolutional layers but no residual connections.

### Training Process: Fine-tuning parameters of both models over multiple iterations using binary cross-entropy loss and the Adam optimizer.
### Evaluation Metrics: Accuracy, precision, recall, F1-score, and confusion matrices were used to assess model performance.

## Results
The results demonstrated that:
ResNet-18 outperformed VGG-16 in terms of accuracy and generalization:
Best accuracy: 87%
Precision (for forged class): 63%
F1-score (for forged class): 75%
VGG-16 achieved slightly lower performance:
Best accuracy: 81%
Precision (for forged class): 54%
F1-score (for forged class): 66%
ResNet-18's residual architecture helped mitigate vanishing gradient issues and improved computational efficiency compared to VGG-16's deeper network.

## Future Work
Future improvements include:
Enhancing VGG-16's performance by integrating residual connections or hybrid architectures.
Implementing advanced forgery localization techniques using U-Net or similar models.
Exploring additional datasets for better generalization across diverse image manipulation scenarios.
Investigating other state-of-the-art architectures like EfficientNet or XceptionNet for comparison.
