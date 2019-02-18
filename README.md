# Opencv
Keras Functional API for multiple inputs and mixed data 


House price dataset includes both numerical/categorical data along with images data for each of the 535 example houses in the dataset.

The numerical and categorical attributes include:

Number of bedrooms
Number of bathrooms
Area (i.e., square footage)
Zip code

A total of four images are provided for each house as well:

Bedroom
Bathroom
Kitchen
Frontal view of the house


To accomplish these goals  a multiple input neural network was defined which was capable of accepting:

1) Numerical data : The numerical data was min-max scaled to the range [0, 1] prior to training.
Categorical data : The categorical data was one-hot encoded (also ensuring the resulting integer vectors were in the range [0, 1]).
2) Image data : image data was also scaled to the range [0, 1]

Inputs to the Keras
The numerical and categorical data were then concatenated into a single feature vector to form the first input to the Keras network. 
Image data served as the second input to the Keras network.

One branch of the model included strictly fully-connected layers (for the concatenated numerical and categorical data) while the second branch of the multi-input model was essentially a small Convolutional Neural Network.

The outputs of both branches were combined and a single output (the regression prediction) was defined.


* House Prices dataset is from Ahmed and Moustafa’s 2016 paper, House price estimation from visual and textual features.
* Based on an article from pyimagesearch
