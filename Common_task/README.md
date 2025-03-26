
# Common Task: Electron/photon classification
#### Dataset Description:
The Dataset contains 32x32 matrices with two channels and has Two classes Electron and Photon. Training set has 249000 images of electron and 249000 images of photon. 
#### Task
To build a model which can classify the data into Electrons and Photons

For this task I trained Foloowing Models:

- Resnet15
- SEResnet15
- Feed Forward Neural Network
#### Approach
First, I trained my model on the data and got an ROC AUC score of 0.78 on ResNet-15 and SE-ResNet-15. Then, I removed the time channel from the data, and my SE-ResNet-15 model achieved a better ROC AUC score of 0.8. Finally, I trained my feedforward neural network on the data with the time channel removed, further improving the ROC AUC score to 0.81.

| Model      | With Time Channel | Without Time Channel |
|:-----------:|:------------------:|:-------------------:|
|Resnet15|0.78|-|
|SEResnet15|0.78|0.8|
|Feed Forward Neural Network|-|0.81|

[Model Weights](https://drive.google.com/drive/folders/17QkTxSgGILdHlKxdvq2YA2N5BGDRe3R4?usp=drive_link)
