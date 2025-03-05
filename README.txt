FaceMask detection using CNN.
Datapreprocessing on Training and Testing datasets.
In train_datagen is used to convert single image into requirements needed, later in training_set the train_datagen is to apply on large scale.
Rather then training all of data_sets we use batch_size(32), with takes 32 batches. Since data is either with/with_out mask we use binary model.
Two convolutional layers are used one automatically initialise while Initialising CNN.
After training data_sets with epochs of 10 the accuracy achieved is 96%.
cnn.fit(x = training_set, validation_data = test_set, epochs = 10)
In line 7, while we are training the training_set we automatically checks with test_set weather the image is with/with_out mask.
Overall the Accuracy(96%) was achieved, if we need more(>96%) then increase size of data_sets and traing with more number of epochs with iterates with batch_size.
Rescale:Normalizes pixel values to the range [0,1] (instead of [0,255] because Neural networks perform better when input values are small and normalized, Pixel values in images range from 0 to 255. Dividing by 255 scales them to 0-1, making training more stable.
Shear_range is used to Helps the model recognize objects from different angles.
Zoom_size: Randomly zooms in or out of images and Helps the model learn to detect objects at different scales.
horizontal_flip: Randomly flips images left-to-right, helps the model generalize better by seeing mirrored images.
The target_size=(64, 64) parameter resizes all images in the dataset to 64x64 pixels before feeding them into the model, target_size=(64,64) ensures all images are uniform in size.Prevents errors when images have different dimensions, speeds up training by reducing computational load. Using of target_size=(128,128) would take more memory but give good/better accuracy.
Difference of using sequential, functional API, subclassing API is Sequential uses layer-by-layer models, Functional API uses complex architectures with multiple inputs/outputs, Subclassing API	uses custom behavior, dynamic architectures.
Coming to activations RELU is fast and used in hidden layers in cnn, works well for feature extraction by keeping positive values and setting negative values to 0.
Sigmoid outputs are between 0 and 1, good for probabilities, PRELU Learns better than ReLU, but it is expensive and used for advanced CNNs for better feature extraction.
Maxpoll selects only the strongest feature (max value) in a given region, averagepoll Takes the average of all values in the region, minpool
picks the smallest value from the region and removes unwanted noise.
Conv2D (2D Convolution) is used for 2D data, like images, Conv3D is used for 3D data, like videos or volumetric data (CT scans, MRI, 3D objects).


