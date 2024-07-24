# Satellite Roadway Segmentation

### Overview

This project focuses on identifying roadways from satellite images using deep learning techniques. The model used is a U-Net, a type of convolutional neural network (CNN) designed specifically for image segmentation tasks. The dataset includes high-resolution RGB satellite images and corresponding masks indicating road pixels.

## Dataset
Structure
Training Data: 6226 RGB satellite images (1024x1024 pixels) with masks.
Validation Data: 1243 RGB satellite images(without masks), so I split train data to use 15% of data as validation set
Test Data: 1101 RGB satellite images (without masks).
Labels
Road Pixels: White (255)
Background Pixels: Black (0)
#### Note: The mask values might not be exactly 0 and 255. Masks are binarized at a threshold of 128.

### Model Architecture
The U-Net model used consists of an encoder-decoder structure:

Encoder: Extracts features using convolutional layers.
Decoder: Reconstructs the image while retaining the location information.

### Intersection over Union(IOU) and Dice Coefficient is used as scoring metric

## Some results of trained model from test data
![Screenshot from 2024-07-24 08-24-18](https://github.com/user-attachments/assets/f033a547-fea3-447f-896f-95f7640e7681)

![Screenshot from 2024-07-24 08-27-23](https://github.com/user-attachments/assets/249c2d04-ea4d-45c4-a29d-2ec31ae4ce83)

