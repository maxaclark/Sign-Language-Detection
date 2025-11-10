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
- Sourced from Kaggle user Shivam Aggarwal ([link](https://www.kaggle.com/datasets/shivamaggarwal513/dlai-hand-signs-05)) containing images of the user's hand as he holds up a number of fingers from 0 to 5
- Pre-split into train (1080 images) and test (120 images) sets
- Classes labels: `0`, `1`, `2`, `3`, `4`, and `5`, corresponding to the number of fingers held up in the image of the hand

### Workflow
1. **Data Processing and EDA**: Converting data from .h5 format and ensuring class balance across subsets
2. **Image Data Generator Construction**: RGB rescaling with no further transformations for baseline performance measures
3. **Model Building**: 7-layer Convolutional Neueral Network
4. **Testing and Evaluation**: Accuracy used for testing metric
5. **Application to Real-World Dataset**: Testing using self-made dataset designed to challenge model

---

## Key Visualizations

### Model Structure
```
model = Sequential()
#1
model.add(Conv2D(filters=32, kernel_size=3, strides=1,
                 padding='same', activation='relu',
                 input_shape=[64, 64, 3]))
#2
model.add(MaxPooling2D(2, ))
#3
model.add(Conv2D(filters=64, kernel_size=3, strides=1,
                 padding='same', activation='relu'))
#4
model.add(MaxPooling2D(2))
#5
model.add(Flatten())
#6
model.add(Dense(128, activation='relu'))
#7
model.add(Dense(6, activation='softmax'))
```


