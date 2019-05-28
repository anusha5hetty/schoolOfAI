Architectural Basics

1.	How many layers: 
•	To start, add layers till the image size is reduced to 11 x 11 and the receptive field is around the size of the image. 
•	Based on the accuracy you get with the first model increase or decrease the number of layers. 
•	Layers can be added till the image size reaches 1 x 1 and receptive field is same as the image size.
•	For large image it is recommended to add layers till the size of the image is reduced to 11 x 11 as the number of pixels getting convolved 9 times is low (with 3 x 3 kernel)
2.	Receptive Field:
•	Input space a CNN’s feature is looking at
•	The receptive field of a model should be almost same as size of the image.
•	 It depends on position of the object in the training and testing image. If the object is at the center of the image it is okay for the model to not see the edge pixels. Eg: if the image size is 100 x 100 and the object is in the center – 94 x 94  the model doesn’t have to see the other rows and columns (the outer 6 rows and columns) i.e the receptive field can be 94 x 94. 
3.	Kernels and how do we decide the number of kernels?
•	Number of kernels depends on the objective of model.
•	It is suggested to increase the number of kernels layer by layer in a convolution block. You can decrease the number in the second convolution block and increase again. So the first layer in each convolution block will be smaller than rest of the layers in the block
•	As the complexity of the dataset increases the number of kernels should increase
4.	3x3 Convolutions,
•	With 3x3 convolutions we can get the effect of any convolution. Eg: Two layers of 3x3 convolution gives the effect of 5x5 convolution. The receptive field after two layers of 3x3 will be same as after one layer of 5x5 convolution
•	The number of pixels that convolve 9 times is more in 3x3 compared to any other convolution. 
5.	Maxpooling,
•	Takes the highest pixel in every 2x2 matrix (if maxpooling of 2 x 2 is done)
•	Allows translation invariance and rotational invariance (even the feature to be detected is moved or rotated a little bit, with max pooling the feature will be captured as the highest pixel is captured)
•	Reduces number of convolution layers
6.	Position of Maxpooling,
•	Max pooling should be placed at least after two layers of convolution – because we might lose  
7.	The distance of Maxpooling from Prediction,
•	At least 3 convolution layers from Prediction – Because with maxpooling we lose 3 out of 4 pixels in every 2x2 block of image (if maxpooling of 2x2 is added). If we do maxpooling close to prediction layer, we affect the prediction accuracy.
8.	1x1 Convolutions,
•	Filters the required feature and suppresses the rest of them without reducing the size of the image. It takes the weighed sum of all the channels
•	Eg: If edges & gradients are formed in previous layer, 1x1 convolution picks just the edges & gradients that we need for the next layer. The output of 1x1 will be edges & gradients
•	Used to reduce the number of channels in the image without losing information
•	Eg: image size of – 24x24x32 with  1x1x32x8 convolution will give 24x24x8. The number of kernels are reduced from 32 to 8. All the 32 channels are merged into 8
•	Can be used to increase the number of channels but there should be a specific purpose for it.
•	Should be placed before or after Maxpooling
9.	Concept of Transition Layers,
•	Used to reduce the number of channels in the image and size of the image
10.	Position of Transition Layer,
•	Can be placed once any of the following is formed in the previous layer - edges&gradients/textures/patterns/parts of object
11.	SoftMax,
•	Used to separate the predicted class very distinctively.
•	Eg If the output of the model is Cat – 6, Dog – 8, ferret – 2, After softmax: Cat – 12% Dog – 87% Ferret – 1%. 
Even though prediction for cat more than half of prediction for dog, after Softmax the prediction for cat goes very low and prediction for dog goes high  
12.	Batch Normalization,
•	Addresses covariance shift
•	Eg for covariance shift: if we have trained the model with black cats and we apply this model to data with colored cats the model will not perform well because the kernels are adjusted based on the pixels in black cats
•	Adds a little bit of noise in the image, which would address overfit problem. If batch normalization is used we can reduce the dropout value
•	Some values of pixels in the image could be lesser than others during convolution, because of which some of the features may not be caught by the kernel. With batch normalization all the pixels will be distributed between 0 to 1 by which the features with low value of pixel will be caught by the kernel.
13.	Image Normalization,
•	Applied in the beginning of the model to the image on which the model will be trained
•	Used so that the features in the training image is clearer for convolution
14.	Number of Epochs and when to increase them,
15.	Dropout
16.	When do we introduce DropOut, or when do we know we have some overfitting
17.	The distance of Batch Normalization from Prediction,
18.	When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
19.	How do we know our network is not going well, comparatively, very early
20.	Batch Size, and effects of batch size
21.	When to add validation checks
22.	Learning Rate,
•	Controls the adjustment of the kernels (weights)
•	If the value is too small, it will take long time to reach the optimum weights (when the cost function is lowest)
•	If the value is too large we might not get the optimum weights. 
•	It is suggested to have a high learning rate and reduce it after each iteration.
23.	
24.	LR schedule and concept behind it
25.	Adam vs SGD

