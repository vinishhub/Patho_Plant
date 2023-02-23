# Plant Disease Detection using Python

This project aims to develop a system for detecting plant diseases using Python programming language. The system uses image processing techniques to analyze images of plants and determine whether they are infected with a disease.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository

       git clone https://github.com/<username>/plant-disease-detection.git
       cd plant-disease-detection
  
  
2. Create a virtual environment and activate it

       python -m venv venv
       source venv/bin/activate # for Linux/Mac
       venv\Scripts\activate.bat # for Windows 

  
3. Install the required packages


       pip install -r requirements.txt`


## Usage

1. Download the dataset and extract it to a directory named `data` at the root of the project.

2. Train the model

       python train.py

3. Test the model on a single image

       python test.py --image path/to/image.jpg```

4. Test the model on a directory of images

       python test.py --dir path/to/directory
  
## Data

The dataset used in this project is the [PlantVillage](https://plantvillage.psu.edu/) dataset. It contains images of healthy and diseased plant leaves, and the diseases are labeled. The dataset can be downloaded from the [official website](https://www.kaggle.com/datasets/emmarex/plantdisease).

## Methodology

The system uses a convolutional neural network (CNN) to classify images into healthy and diseased plants. The CNN is trained on the PlantVillage dataset using transfer learning with the VGG16 architecture. The weights of the pre-trained VGG16 model are frozen, and the final layers are replaced with a fully connected layer and a softmax activation function. The model is trained using the categorical cross-entropy loss function and the Adam optimizer.

## Results

The trained model achieved an accuracy of 95% on the validation set. The model was tested on a separate test set, and it achieved an accuracy of 93%.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.

## License

This project is licensed under the [Apache-2.0 license](LICENSE).
