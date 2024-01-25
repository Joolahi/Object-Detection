# Object-Detection

Object detection project to my machine learning-course final project.

### image_collection.ipynb
That file is made by using python and purpose of that is to create folders, take pictures by webcam and labeling pictures to train the model.
Scripts in file makes needed folders in correct locations for the project,
it will also take 5 pictures by webcam in each folders for training and tesing model.
End of the file there are script that will automatically clone needed repository for labeling images and creating needed xml file to training model.

### training.ipynb
That file is made by using python and purpose of that is to download needed pre trained model, train it and eventually detect wanted object from the picture and after all from live video. 
Scripts will clone needed repos for pre trained model. 
Then it will load data from "image_collection" notebook and make train/test split.
After that, it will define a base model architecture with transfer learning,
and then fine tune this model on our own dataset. After all of these steps,
the script will save the best weights into hdf5 format. Finally, it will evaluate
this model on test set and print out accuracy and loss values.


### Results:





Made with TensorFlow object detection. 
For labeling taken images used https://github.com/tzutalin/labelImg repository
Script for generating Tensorflow record files is made with this sample https://github.com/nicknochnack/GenerateTFRecord/blob/main/generate_tfrecord.py
Pretrained model i used in this project is tf2 detection zoom: SSD MobileNet V2 FPNLite 320x320
Also used nicknochnack repositories for implementing this.
