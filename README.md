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

Everything works as expected. The trained data was small (10 images per object), so the results were also in line with that.
The results were also influenced by the fact that all training data was taken in a similar environment, such as light, background, etc..
However, the end result was a functional whole. It would be easy to improve the project by adding more data and training the model more.

Pictures of detecting object from live video:
![ThumbsDownLive](/media_for_docs/ThumbsDownLive.png)
![LetsRock](/media_for_docs/LetsRockLive.png)





Made with TensorFlow object detection. 
For labeling taken images used https://github.com/tzutalin/labelImg repository
Script for generating Tensorflow record files is made with this sample https://github.com/nicknochnack/GenerateTFRecord/blob/main/generate_tfrecord.py
Pretrained model i used in this project is tf2 detection zoom: SSD MobileNet V2 FPNLite 320x320

