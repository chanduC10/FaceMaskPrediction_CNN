FaceMask detection using CNN.
Datapreprocessing on Training and Testing datasets.
In train_datagen is used to convert single image into requirements needed, later in training_set the train_datagen is to apply on large scale.
Rather then training all of data_sets we use batch_size(32), with takes 32 batches. Since data is either with/with_out mask we use binary model.
Two convolutional layers are used one automatically initialise while Initialising CNN.
After training data_sets with epochs of 10 the accuracy achieved is 96%.
cnn.fit(x = training_set, validation_data = test_set, epochs = 10)
In line 7, while we are training the training_set we automatically checks with test_set weather the image is with/with_out mask.
Overall the Accuracy(96%) was achieved, if we need more(>96%) then increase size of data_sets and traing with more number of epochs with iterates with batch_size.
