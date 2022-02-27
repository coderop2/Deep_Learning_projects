# Deep Learning projects
Following projects can be found in this repository:-
1. **CNN, its basics and its understanding** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/CNN_and_its_understanding.ipynb) - This notebook uses MNIST as data and trains a simple CNN. Which is further used to understand how it works on a lyer by layer basis. Here i use each layer to understand that if a full CNN is trained then how good of a classifier is each of the netwroks layer, which i have preseneted and studied through the use of PCA and T-SNE decompostion. Experiment done :- 
    - Using random 10 units from a layer to answer the question how good of a classfier can that make ? Turns out that there are some combination of units which when selected will actually give a pretty good result (defenitly not as good as the final classifier layer). 
    - Further experimentation is done on how does different weights initialization (both kernels and bias) affect the training/test/validation accuracy and error rates.
    - Comparison between the use of dropout and no dropout - looks like dropout helps in creating a more generalized model which fits testing and validation data well.
2. **CNN with/out Augmentation** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/CNN_with_out_augmentation.ipynb) - Although we are in the age of data where we can get data very readily on any topic or area that we desire, the problem is the amount of data we have. While for some cases we have so much data that the model might not be able to handle it, while in other we have so little that the model is not able to generalize well and ends up getting over fitting to the data thats present. So in order to avoid that and understand the use of augmentation i studied the effect of use of augmentation and not augmentation of the CIFAR 10 dataset with the use of CNNs and the network. Experimentation done :-
    - Augmentation Vs Non-augmented dataset - Augmentation won with over 3% better results, provided i was only using 3 augmentation techniques.
    - Transfer learning on a smaller subset of dataset from CIFAR and then further studing the effects of augmentation
3. **Speech Denoising Using RNN** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/RNN_on_Audio.ipynb) - A simple RNN to leverage the use to sequential data in the audio file and train them on bidirectional LSTMs, that is after converting them into frequency and time domain which actually brings out the wave form of the audio files.
4. **CNN on Audio Data** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/CNN_on_Audio.ipynb) - Although there might be a debate as too which might bring the most of audio files CNNs or RNNs. I simply ignore these debates and focus on FCNs and CNNs. Experiments done :-
    - Training and comparing audio files between a 5 layer fully connected neural network and a 5 layer deep CNN. The comparison was done using SNR for before and after. Althouh not surprising CNNs performed better than FCNs as they were able accomodate better the different peks and valleys of the signal than a FCN.
    - Further use a CNN to predict the secind half of the audio file given the first half (something like a audio GAN).
5. **RNNs as a generative model** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/Pixel_Gen_RNNs.ipynb) - A RNN is good at learning about sequential data and taking this fact into consideration i establish a goal to generate images based on the fact that some part is given(like the input is the top half and the job of the model isto predict the bottom half). So that the resulting image is a complete image. Data being used here is MNIST and getting a great accuracy of 98%-99% when compared to original. Tthis is a generative model that can “draw” handwritten digits.
6. **Network Compression Using SVD** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/CNN_SVD_Siamese_Ntw.ipynb) - ```"In linear algebra, the singular value decomposition (SVD) is a factorization of a real or complex matrix. It generalizes the eigendecomposition of a square normal matrix with an orthonormal eigenbasis to any {\displaystyle m\times n}m\times n matrix. It is related to the polar decomposition."``` As explained in wikipedia, SVD helps in dimentionality reduction and extracts information by decomposing a matrix into 3 submatrices. Experiments done :-
    - Running SVD single time on the model weights, then extract top 20 features from the decompsed matrices and regain the original sized matrix by doing matrix muliplication on the selected features. Evaluate the model by setting back the weights.
    - Layer wise SVD weights decomposition
    - Create a custom layer and perform SVD decomposition at each iteration/epoch
7. **Speaker Verification using Siamese Network** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/Siamese_Ntw.ipynb) - A Siamese neural network (sometimes called a twin neural network) is an artificial neural network that uses the same weights while working in tandem on two different input vectors to compute comparable output vectors. So, the job is to build a speaker verification system. It takes two utterances as input, and predicts whether they were spoken by the same speaker (positive class) or not (negative class). Here the training data is Audio files and the target is to check if a particular audio is played by the same speaker or not.
8. **Variational Autoencoders on Poor Sevens** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/VAE.ipynb) - ```"Variational autoencoders (VAEs) are autoencoders that tackle the problem of the latent space irregularity by making the encoder return a distribution over the latent space instead of a single point and by adding in the loss function a regularisation term over that returned distribution in order to ensure a better organisation of the latent space."``` As a VAE, it needs a hidden layer that is dedicated to learn the latent embedding. In this layer, each hidden unit is governed by a standard normal distribution as its a priori information. Using a limited number of hidden units ```K``` in code layer (the embedding vector) - here the latent dimension is 4. Out of K, there must be a dimension that explains the effect of different 7's. Experiments done :- 
    - Each of the 4 latent dimensions control a aspect of image 7 and changin each will result is a different kind of 7.
    - For my case the 4 latent dimensions control the following :-
        - 1st dimension - Rotation
        - 2nd Dimension - Thickness
        - 3rd Dimension - size of the horizontal line
        - 4th Dimension - Rotation
9. **GAN** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/GAN.ipynb) - ```"Given a training set, this technique learns to generate new data with the same statistics as the training set. For example, a GAN trained on photographs can generate new photographs that look at least superficially authentic to human observers, having many realistic characteristics. Though originally proposed as a form of generative model for unsupervised learning, GANs have also proved useful for semi-supervised learning, fully supervised learning, and reinforcement learning."```
10. **Missing Value Imputation Using Conditional GAN** [LINK](https://github.com/coderop2/Deep_Learning_projects/blob/main/ConditionalGAN.ipynb) - ```Conditional generative adversarial network, or cGAN for short, is a type of GAN that involves the conditional generation of images by a generator model. A generative adversarial network (GAN) is a Machine Learning framework used to train generative models. Read more about GANs here. GANs rely on a generator that learns to generate new images, and a discriminator that learns to distinguish synthetic images from real images. In cGANs, a conditional setting is applied, meaning that both the generator and discriminator are conditioned on some sort of auxiliary information (such as class labels or data) from other modalities. As a result, the ideal model can learn multi-modal mapping from inputs to outputs by being fed with different contextual information.``` Here using the theory of conditional GAN i create a missing value imputation system. Assuming that only the center part of the image is known, while the generator has to predict what the other surrounding pixels are. Experiments done :-
    - I added another regularizer to my generator so that it functions as an autoencoder at least for the center pixels. In an ordinary GAN setup, the generator loss has to penalize the discriminator’s decision that classifies the fake examples into the fake class (i.e., when the generator fails to fool the discriminator). 
    - On top of this ordinary generator loss, I add a simple mean squared error term that penalizes the difference between the conditioning vector and the center patch of the generated image, as they have to be the same, essentially.
