# Face Mask Detection using CNN
This repository contains a project for detecting face masks using Convolutional Neural Networks (CNN). The goal of this project is to build a model that can accurately classify whether a person is wearing a face mask or not.

## Project Overview

Face mask detection is crucial in the current global scenario to ensure compliance with health guidelines. This project leverages CNN to classify images of faces as either "with mask" or "without mask". The project involves:

- **Fetching and preprocessing image data**: Collecting data from sources such as Kaggle and preparing it for training and evaluation.
- **Building and training a CNN model**: Designing a Convolutional Neural Network and training it using the preprocessed data.
- **Evaluating the model performance**: Assessing the trained model using various metrics to ensure its effectiveness.
- **Deploying the model for real-time mask detection**: Implementing the model to detect face masks in real-time scenarios.
Certainly! Here’s a complete and detailed guide for setting up your Kaggle dataset in Google Colab:

---

# Setting Up Face Mask Detection Dataset in Google Colab

This guide provides step-by-step instructions to set up and fetch the dataset for the Face Mask Detection project using Google Colab.

## 1. Install Kaggle Package

First, you need to install the Kaggle package if it’s not already available in your Colab environment. Run the following command:

```python
!pip install kaggle
```

## 2. Upload Kaggle API Key

To access Kaggle datasets, you need to upload your Kaggle API key (`kaggle.json`) to your Colab environment. Follow these steps:

1. **Upload the `kaggle.json` file**:

   ```python
   from google.colab import files
   files.upload()  # Select and upload your kaggle.json file here
   ```

2. **Move the `kaggle.json` file to the appropriate location**:

   ```python
   !mkdir -p ~/.kaggle
   !mv kaggle.json ~/.kaggle/
   ```

3. **Set the correct permissions for the file**:

   ```python
   !chmod 600 ~/.kaggle/kaggle.json
   ```

## 3. Fetch the Dataset from Kaggle

Use the Kaggle API to download the dataset. Replace `omkargurav/face-mask-dataset` with the appropriate dataset identifier if needed.

```python
!kaggle datasets download -d omkargurav/face-mask-dataset
```

## 4. Unzip the Dataset

After downloading, unzip the dataset to access its contents:

```python
!unzip face-mask-dataset.zip -d data
```

## 5. Verify Dataset Files

Check if the dataset files are extracted correctly:

```python
!ls data
```

This will list the contents of the `data` directory, allowing you to verify that the files have been extracted as expected.

## Additional Notes

- Ensure that you replace `omkargurav/face-mask-dataset` with the correct dataset identifier if you are using a different dataset.
- The `kaggle.json` file should contain your Kaggle API credentials, which are necessary for accessing Kaggle datasets programmatically.

---

You can now proceed with your project by training and evaluating your model using the dataset you've set up.
