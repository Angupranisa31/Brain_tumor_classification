Brain Tumor MRI Classification
Problem Statement
This project focuses on multi-class classification of brain MRI images into four categories: glioma, meningioma, pituitary tumor, and no tumor.

Approach
Data Preparation
  Loaded images using ImageDataGenerator.
  Resized to 224x224.
  Normalized pixel values (1/255).
  Applied augmentation (rotation, zoom, horizontal flip).
  Used 80-20 train-validation split.

Model Architecture
  Used MobileNetV2 pre-trained on ImageNet as feature extractor.
  Frozen base model layers.
  Added:
    GlobalAveragePooling2D
    Dropout (0.3)
    Dense(128, ReLU)
    Dense(4, Softmax)

Training
  Optimizer: Adam
  Loss: Categorical Crossentropy
  EarlyStopping applied
  Trained for 5 epochs (due to time constraint)

Evaluation
  Test Accuracy: 85.96%
  Macro F1 Score: (add your value)
  Confusion matrix generated.

Results
  The model achieved strong performance using transfer learning within limited time constraints. With additional fine-tuning, performance can be further improved.


