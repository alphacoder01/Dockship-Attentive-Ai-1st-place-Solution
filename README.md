# Note: 
1. The dataset (tfrecords)[299x299] can be found [here](https://www.kaggle.com/ashish2001/attentiveaitfrecords299x299)
2. Original images are [here](https://dockship.io/challenges/6006f6015c9276402bd77e83/attentive-ai-internship-hiring-challenge/overview)

# Approach:
1. Converted Original data to TFRecords, for using the Kaggle's TPU using [this](https://github.com/alphacoder01/Dockship-Attentive-Ai-1st-place-Solution/blob/main/Convert_to_tfrecords.ipynb)
2. All images were scaled to 299x299 considering majority of the images had similar resolution.
3. Model used **EfficientNet-B4 (noisy student weights)** freezed BatchNorm layers.
4. Augmentations used:
    * Horizontal Fips
    * Shearing
    * H/W Zoom
    * H/W Shift
5.  Custom Cosine Annealed Learning Schedule
6.  5-Fold Cross Validation pipeline.
7.  Class weights to combat class-imbalance.
   

`Will be making the kaggle notebook public soon!`
