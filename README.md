# Brain Teaser - A Novel Task Defying Common Sense
Authors: Vagdevi Sahasra Bandaru

## Introduction
This is the github repo for our ENLP course project. We used 4 models: Canine, T5, BERT and Mistral for this task. The code for each model is separate: `canine.ipynb`, `t5.ipynb`, `bert.ipynb` and for Mistral, `mistral_baseline` for zero-shot inference and `mistral_fewshot` for few-shot inference.

## How To Run
### Load The Data
The training and testing data are in `SP-train.npy` and `WP-train.npy`, and we performed a train-test split on these files.

#### Load From Local
This is the default setting, make sure the .npy files are in the same directory of the notebook.

#### Load From Google Drive
If you are using colab, you can uncomment lines like these, and you will have to upload those files to the indicated locations in the notebook:

```python
spTrain = np.load('/content/drive/MyDrive/Georgetown/BrainTeaser/SP-train.npy', allow_pickle=True)
wpTrain = np.load('/content/drive/MyDrive/Georgetown/BrainTeaser/WP-train.npy', allow_pickle=True)
```

### Load the Model
The models are loaded from HuggingFace directly. For Mistral-7B,**you will need a HuggingFace account** for a token, and you will have to accept the conditions on their [page](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.2) before accessing the model.


#### Training and Evaluation
We performed a train-test split on the data and evaluated on the model accuracy on test set. The training and testing part are similar for all these notebooks and should be straightforward. After loading the data and the model, you can execute the train/test block to see the results.