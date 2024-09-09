The dataset contains images of 9 types of boats. It contains a total of 1162 images. The training images are provided in the directory of the specific class itself. 
Classes:
●	ferry_boat, gondola, sailboat, cruise_ship, kayak, inflatable_boat, paper_boat, buoy, freight_boat
Perform the following steps:
1.	Build a CNN network to classify the boat.
2.	Split the dataset into train and test in the ratio 80:20, with shuffle and random state=43. 
3.	Use Keras ImageDataGenerator to initialize the train generator with validation_split=0.2 and test generator. Generators are required to avoid out of memory issues while training. 
4.	Both generators will be initialized with data normalization. 
(Hint: rescale=1./255). 
5. Load train, validation and test dataset in batches of 32 using the generators initialized in the above step.
6. Build a CNN network using Keras with the following layers
7. Cov2D with 32 filters, kernel size 3,3, and activation relu, followed by MaxPool2D
8. Cov2D with 32 filters, kernel size 3,3, and activation relu, followed by MaxPool2D
9. GLobalAveragePooling2D layer
10. Dense layer with 128 neurons and activation relu
11. Dense layer with 128 neurons and activation relu
12. Dense layer with 9 neurons and activation softmax.
13. Compile the model with Adam optimizer, categorical_crossentropy loss, and with metrics accuracy, precision, and recall.
14. Train the model for 20 epochs and plot training loss and accuracy against epochs.
15. Evaluate the model on test images and print the test loss and accuracy.
