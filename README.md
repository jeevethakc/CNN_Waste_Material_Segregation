# CNN_Waste_Material_Segregation

## Project Summary

This project focuses on the classification of waste images into seven predefined categories: Cardboard, Food Waste, Glass, Metal, Paper, Plastic, and Other. A custom Convolutional Neural Network (CNN) was developed using the Keras Sequential API and trained on RGB images resized to 128×128×3 dimensions.

A noticeable challenge was the imbalance in class distribution, with Plastic having the highest number of samples and Cardboard the fewest. To counter this issue, the model leveraged real-time data augmentation using Keras' ImageDataGenerator. The applied transformations included rotation, shifting, shearing, zooming, and horizontal flipping. Labels were generated from folder structures and transformed into a one-hot encoded format to support multi-class classification.

## Key Highlights

Model Architecture: Custom 3-layer CNN with Batch Normalization, Dropout, ReLU activations, and a Softmax output layer.

Training Accuracy: Approximately 95%

Validation Accuracy: Increased from ~64% to ~69% after applying augmentation.

Evaluation Metrics: Included accuracy, precision, recall, F1-score, and a confusion matrix for class-wise performance insight.

Handling Class Imbalance: Real-time data augmentation was used; future improvements may involve class weighting or resampling strategies.

To avoid overfitting, the training process included early stopping and learning rate reduction strategies. Despite strong performance on the training set, the model struggled with closely resembling classes such as Plastic and Food Waste. Augmentation helped reduce the overfitting gap and enhanced the model’s generalization on unseen data.

Overall, the project underlines the critical role of data preprocessing and regularization when working with imbalanced image datasets. Potential enhancements for future work include integrating transfer learning via pre-trained networks like ResNet or MobileNet, experimenting with focal loss, or automating augmentation strategies using tools like AutoAugment.
