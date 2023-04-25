# Brain-Tumor-Detection
This project demonstrates how you can use the TensorFlow Python library to build a deep learning model for image classification. The goal was to create a convolutional neural network that can process brain image scans and determine if a tumor is present.

The [image dataset][dataset] used to train the model was downloaded from Kaggle. The user, who uploaded the dataset, described the images as "X-ray images of Brain." However, judging from the visual features of the scans, it appears that these images most likely came from MRI scans, as there are no dense bone structures present.

A model was trained on 80% of the data and evaluated on the other 20%. The final test accuracy came out to ~97%. This model was exported in the SavedModel format to `\brain_tumor_detection_model\`, so anyone can load same the model and use it to make predictions on new images. To experiment with different model and training hyperparameters, follow the steps below to set up your environment.

## How to use
1. Clone the repository by running the command `git clone https://github.com/Nielam-Dass/Brain-Tumor-Detection.git`.
2. While in the project folder, create a virtual environment of your choice. This process may vary depending on your operating system. On Windows, run `python -m venv venv`, to create an environment folder named `venv`.
3. Activate the environment with `venv\Scripts\activate.bat`.
4. Once the environment is active, install the necesary packages with `pip install -r requirements.txt`.
5. Go to the [Kaggle][kaggle] website and generate an API token, which will be downloaded in JSON format. The file will contain values for the `username` and `key` fields.
6. Create a `.env` file in the project folder, which will define the environment variables `KAGGLE_USERNAME="your_username"` and `KAGGLE_KEY="your_key"` according to the downloaded JSON data.
7. At this point, you can tweak the code in the Jupyter notebook to build and train a new model.

## Disclaimer
This project is designed for experimental purposes only! Any models created from this code (or a modified version of it) should NOT be used in a professional medical setting.

[dataset]: https://www.kaggle.com/datasets/preetviradiya/brian-tumor-dataset
[kaggle]: https://www.kaggle.com/
