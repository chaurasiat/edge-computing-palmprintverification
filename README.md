# edge-computing-palmprintverification
used Siamese-Networks-for-One-Shot-Learning for this
Data preparation steps:
1.	Divided the total data into training and testing 
2.	500 training and 100 testing images
3.	For testing, for every class (001,002….100),I have taken one image at  random and put it into respective testing folder .
4.	Also, I have cropped the images and excluded some initial rows and columns:
image= image[10:120, 10:120]

so, the final image size was (110,110)

The Siamese model summary (network reference from) : 
https://github.com/asagar60/Siamese-Neural-Networks-for-One-shot-Image-Recognition/tree/e1712e9f30aea81e1dd0577bb08dea26e11df845

•	I have changed the kernel initializer and bias initializer as initially the total trainable parameters were huge, close to 68,000,000. after doing this step the total trainable parameters were 10,636,098
•	Also, I have tried and tested between euclidean_dist and difference of tensors approach and went with euclidean_dist

•	 
•	
 
 
I have trained the model for 500 iteration: The error at the end of 500 iteration was : 0.38721391558647156.
 
Wrote code to test model testing accuracy, it was able to correctly recognize all the test images because of Cropping the images and Euclidean distance .
 
 
