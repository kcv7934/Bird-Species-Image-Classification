# Bird Image Classification with MobileNetV2

This project uses a **MobileNetV2** model pre-trained on ImageNet for bird species classification. 

## Technologies Used
- **Python**  
- **PyTorch**  
- **MobileNetV2**  
- **Pandas**  
- **NumPy**  
- **PIL**  
- **torchvision**  

## Dataset
The dataset consists of images of birds stored in a directory. The corresponding labels (bird species) are stored in a CSV file 'gt.csv' that contains the image paths and labels.

Link to Google Drive containg validation and training set: https://drive.google.com/drive/folders/1ZYDd-pcToBeAAzSTSHm9qKWNxyTA9AY3?usp=share_link

## Model Architecture
The model architecture is based on **MobileNetV2**, which has been fine-tuned to classify bird images:
- **Pre-trained MobileNetV2** weights are used for learning.
- The last few layers of the model are replaced with a custom classifier consisting of a **dropout layer**, **fully connected layers**, and **batch normalization**.

## Hyperparameters
- Learning Rate: **0.0009**
- Batch Size: **32**
- Epochs: **15**
- **Adam Optimizer** used for training.

## Training Process
- The model was trained for **15 epochs** on the custom bird image dataset.
- **Data augmentation** including resizing, center cropping, and normalization was applied to the images.

## Results
- Achieved **83% accuracy** on the validation set after 15 epochs of training.
