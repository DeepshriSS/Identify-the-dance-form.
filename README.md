# Identify-the-dance-form.
A challenge put up by HackerEarth.
The challenge was to classify the dataset into eight different dance forms that exist in India.
The training dataset had very little data with just 364 images to be trained. 
The baseline model was a clear case of overfitting with 100% training and 40% validation accuracy.

The major task was to increase the amount of data. Tried ImageDataGenerator at first but it actually didn't help. 
It just created 6 different images for every image with no peculiar differences. Even though it increased the training accuracy but failed on the validation.
So to overcome the problem of little data, I used OpenCV features and fixed the number of images I wanted in my training dataset.
Applied all the annotation techniques and got a considerable amount of data to be trained.

After the data generation, the next task was to improve the accuracy, for which I used Transfer learning.
I tried VGG16 and VGG19 and played around with the parameters. The accuracy improved a lot on the training dataset but the score was not good after the submission.
I switched to ResNet50 which is considered to be better than VGG16. Another trick is that I didn't split the dataset into training and validation. 
Instead I just trained the entire data and the score on submission improved.

To improve the score I used fine tuning and freezed some of the layers and the score improved again.
Finally after playing a lot with the parameters I chose to increase the data by some 1000 images more and the score on submission increased from 72 to 85 out of 100.
The accuracy achieved was 98.99% and the final score was 85/100 with a rank of 105.
