# Sign Language Classification  
### Max Clark, Lukas Schneider, Rowan King, Brendan McGuinness  
  
This project intends to train a Convolutional Neural Network (CNN) to classify images of hands based on how many fingers the hand is holding up. We initially use a dataset from Kaggle for training and testing, and then attempt to apply the model to new, less uniform data that may encountered in the real world.

---

## Objectives  

- Verify class balance and stratification across training and testing splits
- Build and train a CNN to classify images based on the number of fingers raised in the image
- Analyze model successes and failures in testing
- Apply CNN to our own dataset designed to challenge the model

---

## Repository Structure

```
|---jpeg_images                        # Self-made dataset of images
|      |---0                           # Sub-folders containing specified classes of images
|      |---1
|      |---2
|      |---3
|      |---4
|      |---5
|---README.md
|---SignLanguageClassification.ipynb   # Final Project Jupyter Notebook
|---test.h5                            # test dataset
|---train.h5                           # train dataset
```

---

## Methodology

### Dataset
- Sourced from Kaggle user Shivam Aggarwal [link](https://www.kaggle.com/datasets/shivamaggarwal513/dlai-hand-signs-05)
