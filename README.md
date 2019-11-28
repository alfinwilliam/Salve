# Salve
1. Salve is an android chat application with reply suggestion capabilities that was developed using Seq2seq model and LSTM neural network.
2. The predication of responses are computed on a python3 TCP server deployed on local machine and send back to the android app.
3. The seq2seq model was trained on [Amazon Sagemaker](https://aws.amazon.com/sagemaker/) using Amazon Free tier facility.
4. The predications are at 80% accuracy at the present stage and we are intending on improving it in future.

# Build Instructions

1. Download the latest version of Android Studio [here.](https://developer.android.com/studio/)
2. Create the apk of android application using android emulator and install it on atleast 2 android devices.
3. Run the Server.py file on Server Socket directory to initialize local server machine on your laptop / desktop.
    ` async python3 server.py`
4. Connect the android devices on to same wifi network as the local server is initialised.
5. Run android application and start chat to view context relevant reply suggestions as responses.

# Data Model Developed

* The machine learning model was trained on AWS Sagemaker t3.medium instance using amazon free tier. It was trained for approx 40 epochs
and took 40 hours of training. We are providing our trained model at Salve/Server-Socket/model.npz.
* The training data used is [Twitter Chat Corpus](https://github.com/marsan-ma/chat_corpus) , you can also use [Cornell Movie Data Corpus](https://github.com/suriyadeepan/datasets/tree/master/seq2seq/cornell_movie_corpus)
to increase accuracy.
* For more information regarding training model , refer this [blog](http://complx.me/2016-12-31-practical-seq2seq/).

This project was created as a Mini project for Semester 5 MCA at College of Engineering Trivandrum.

# Contributors

1. [Alfin William](https://github.com/alfinwilliam)
2. [Febin Baiju](https://github.com/febinbaiju)
3. [Sethumadhavan KS](https://github.com/SethumadhavanKS)
