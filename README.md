# eecs-349-final

"""
This is an example of using the k-nearest-neighbors(knn) algorithm for the facial recognition of RuPaul Charles, drag queen extraordinaire.

What do I need to use this example?
Before running anything, you'll need to download TensorFlow, dlib, scikit-learn, and OpenFace.
These repositories contain useful machine learning techniques to expedite the coding flow.

Algorithm Description & How It Works:
A collection of 150 labeled images of RuPaul in drag and 150 images of RuPaul out of drag were collected and placed in a directory of the following structure:

        <train_dir>/
        ├── <rupaul_no_drag>/
        │   ├── <rupaul1>.jpeg
        │   ├── <rupaul2>.jpeg
        │   ├── ...
        ├── <rupaul_in_drag2>/
        │   ├── <drag1>.jpeg
        │   └── <drag2>.jpeg
        └── ...
        
The classifier is first trained on both subdirectories, in which the facial recognition program generates unique embeddings for each group of pictures.

Calling the prediction function then takes an unkown image, and finds the k most similar faces (images with closet face-features via the embedding and under eucledian distance) in its training set,
and performing a weighted majority vote on the image's resulting label.

Usage:
- First, collect images containing people you wish to determine are or are not RuPaul.

- Call 'predict' to classify.



