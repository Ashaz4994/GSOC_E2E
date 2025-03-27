# Specific Task 2j
### Dataset Description 
MNIST Dataset in which images are rotated in steps of 30 degrees.
### Task 1
#### Latent Space Creation
For latent space creation, I trained a Variational Autoencoder (VAE). I tried different latent space dimensions and found that 64 was the best.
### Task 2
#### Supervised Symmetry Discovery
We were supposed to train an MLP that maps every image vector to its rotated version. The MLP consists of two parts: one for means and the other for log-variance. To achieve this, I randomly rotated the image, obtained its latent space vector, and then computed the means and log-variance using the MLP. I then recursively computed the means and log-variance for the next 30-degree rotated image. This approach allows me to obtain the latent space vector of a 90-degree rotated image from the original image by applying the process recursively.
### Task 3
#### Unsupervised Symmetry Discovery
I took the latent space vector of each image and trained an oracle that predicts the correct label for an image. It achieved an ROC AUC score of 0.999.  

After that, I implemented the loss function mentioned in the paper and trained the generator, but I did not obtain satisfactory results. It could be due to high dimension that i have choosen for latent space.

#### [Model Weights](https://drive.google.com/drive/folders/16NFYIhpMY22iWh4UoLRgfapQuLCeiAx_?usp=drive_link)
