
<h1> FlowerSpeciesClassification </h1>

<img width="1298" alt="Screenshot 2023-04-16 at 2 56 08 PM" src="https://user-images.githubusercontent.com/30067377/232335459-d686abc5-e865-47d6-8d56-d3b9fd9d732c.png">

Accurate identification and classification of flower species is a crucial task for the understanding and conservation of various plant species. However, the lack of available information about the different flower species poses a significant challenge to achieving this goal. This report proposes a Flower Identification System focused on identifying the correct class/specie of a given flower. The project utilizes three different datasets containing a varied number of flower species, that were used to train three different Convolutional Neural Network (CNN) architectures - MobileNetV2, ResNet18, and VGG16. The training process was done for nine instances trained from scratch, three instances for transfer learning and multiple instances for hyperparameter tuning. In this report, the outcomes of the  scratch and transfer learning training, hyperparameter tuning, Grad-CAM and TSNE visualization are discussed. The analysis helps determine which model-dataset combination provides the maximum accuracy along with optimal hyperparameters for training the models. This study aims to contribute towards enhancing the classification and identification of flower species, which will be beneficial for the conservation and protection of various plant species.

<h2> Project aim </h2> • Develop a flower classification system using deep learning techniques to aid botanists, agriculturists, and horticulturists in identifying different species of flowers.<br>
<h2> Methodology </h2> • Building deep-learning-based classification models using a combination of state-of-the-art convolutional neural network (CNN) architectures. <br>
 <br>
 <img width="1403" alt="Screenshot 2023-04-16 at 3 11 18 PM" src="https://user-images.githubusercontent.com/30067377/232336475-88c33415-d9a7-4770-8cb4-9fbf531f8387.png">


<h2> Goals </h2>
    • Explore and provide a detailed analysis of how different CNN architectures and combinations fare against the chosen datasets of flowers. <br>
    • Compare all eleven models that were trained. <br>
    • Provide a detailed performance analysis. <br>
<br>

<h2> Requirements to run the code (libraries, etc) </h2>
 
 ```sh
  pip install -r requirements.txt
  ```

<h3> Instructions to run the code : </h3>
• Jupyter Notebook or any compatible software to run .ipynb files. <br>
• Access to the dataset, which is assumed to be stored in Google Drive. <br>
• Access to the pre-trained models, which are stored inside PreTrainedModels. <br>
• The required libraries and modules should be installed in the environment, including but not limited to PyTorch, scikit-learn, tqdm, and matplotlib. <br>

<h2>Training and Validating the Models</h2>

The models are trained in the folders as in Dataset-1, Dataset-2, Dataset-3. The codes are in .ipynb files. Some Sample files are given below :
MobilenetV2_Dataset1.ipynb
Dataset2_VGG16_Final.ipynb
Resnet18_Dataset3.ipynb


<h2>To run the pre-trained model on the provided sample test dataset </h2> 
• Access the "TestingModel" folder where the pre-trained sample testing model is located. <br>
• Retrieve the corresponding pre-trained model weights from the below given drive link. <br>
• Obtain the sample test dataset from the below given drive link. (https://drive.google.com/drive/folders/1BrCI3fdoxvH840Ii5AD914SgKfVjv8Ci?usp=share_link) <br>


<h2>Links to the Dataset</h2>
• Flowers Dataset 1, URL: https://www.kaggle.com/datasets/nadyana/flowers <br>
• Flowers Dataset 2, URL: https://www.kaggle.com/datasets/utkarshsaxenadn/flower-classification-5-classes-roselilyetc <br>
• Flowers Dataset 3, URL: https://www.kaggle.com/datasets/l3llff/flowers <br>

<br>
 <img width="1043" alt="Screenshot 2023-04-16 at 3 12 50 PM" src="https://user-images.githubusercontent.com/30067377/232336567-81f01015-daf6-4210-83d2-c3bb410a5f75.png">




![std2](https://user-images.githubusercontent.com/30067377/231942056-2a3c504c-c9ba-4346-8294-b73b69d5e27b.png)

<h3>Dataset-1 </h3> 
  • It has 7 evenly balanced classes with 1600 images per class (11200 total images). However, we pruned the number of classes to 5 making the total images to 8000(to maintain a diverse number of classes per dataset). 
  
<img width="905" alt="Screenshot 2023-04-12 at 2 13 04 AM" src="https://user-images.githubusercontent.com/30067377/231367104-14256f00-be8a-4684-968c-7f70ed518342.png">

<h3>Dataset-2 </h3> 
  • It has 10 evenly distributed classes with 1500 images per class (15000 total images).
  
<img width="905" alt="Screenshot 2023-04-12 at 2 13 42 AM" src="https://user-images.githubusercontent.com/30067377/231367205-7fe78ffb-0c40-4ef8-bf3c-dc59e668a8a0.png">


<h3>Dataset-3 </h3> 
  • It has 16 classes unevenly distributed with a total of 15,740 images. There are 980 images on average per class in Dataset-3 where the number of images per class fell in the range of 737-1054. 
  
  <img width="905" alt="Screenshot 2023-04-12 at 2 14 05 AM" src="https://user-images.githubusercontent.com/30067377/231367296-2d956e6a-c479-4881-892d-5ed5bd2d4642.png">

<h3> Problematic Images in Dataset 2 </h3>

<img width="905" alt="Screenshot 2023-04-12 at 2 15 01 AM" src="https://user-images.githubusercontent.com/30067377/231367467-287da706-15e2-43bf-ad24-d5da7eebac71.png">

<br> <br>


<h3> The imported libraries and modules include : </h3>

* [![Python][Python.js]][Python-url]
* [![torch][torch.js]][torch-url]
* [![torch.nn, torch.nn.functional][torch.nn.js]][torch.nn-url]
* [![torch.utils.data][torch.utils.data.js]][torch.utils.data-url]
* [![torchvision.datasets, torchvision.transforms, torchvision.models][torchvision.js]][torchvision-url]
* [![sklearn][sklearn.js]][sklearn-url]
* [![tqdm][tqdm.js]][tqdm-url]
* [![torchsummary][torchsummary.js]][torchsummary-url]
* [![pandas][pandas.js]][pandas-url]
* [![numpy][numpy.js]][numpy-url]
* [![matplotlib][matplotlib.js]][matplotlib-url]
* [![omnixai][omnixai.js]][omnixai-url]
* [![optuna][optuna.js]][optuna-url]

[Python.js]: https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white
[Python-url]: https://www.python.org/
[torch.js]: https://img.shields.io/badge/torch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white
[torch-url]: https://pytorch.org/
[torch.nn.js]: https://img.shields.io/badge/torch.nn%2C%20torch.nn.functional-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white
[torch.nn-url]: https://pytorch.org/docs/stable/nn.html
[torch.utils.data.js]: https://img.shields.io/badge/torch.utils.data-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white
[torch.utils.data-url]: https://pytorch.org/docs/stable/data.html
[torchvision.js]: https://img.shields.io/badge/torchvision.datasets%2C%20torchvision.transforms%2C%20torchvision.models-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white
[torchvision-url]: https://pytorch.org/vision/
[sklearn.js]: https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white
[sklearn-url]: https://scikit-learn.org/stable/
[tqdm.js]: https://img.shields.io/badge/tqdm-4B8BBE?style=for-the-badge&logo=python&logoColor=white
[tqdm-url]: https://tqdm.github.io/
[torchsummary.js]: https://img.shields.io/badge/torchsummary-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white
[torchsummary-url]: https://github.com/sksq96/pytorch-summary
[pandas.js]: https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white
[pandas-url]: https://pandas.pydata.org/
[numpy.js]: https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white
[numpy-url]: https://numpy.org/
[matplotlib.js]: https://img.shields.io/badge/matplotlib-11557C?style=for-the-badge&logo=python&logoColor=white
[matplotlib-url]: https://matplotlib.org/
[omnixai.js]: https://img.shields.io/badge/omnixai-1C263F?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgo
[omnixai-url]: https://github.com/salesforce/OmniXAI
[optuna.js]: https://optuna.org/assets/img/optuna-logo@2x.png
[optuna-url]: https://optuna.org/


• There are also installations of the optuna and omnixai libraries using the !pip install command. <br>


<h2>Folder Descriptions : </h2>

<h3>• Data Analysis:</h3> This folder contains scripts and code used to perform data analysis on the datasets used in the project. It contain scripts for data cleaning, data exploration, and data visualization. Data analysis is an important step in any machine learning project, as it helps to identify patterns and insights in the data that can inform the development of machine learning models.<br>

<h3>• Dataset-1, Dataset-2, Dataset-3: </h3>These folders contain code used for training and testing machine learning models. Each dataset has its own set of comparison codes, which are used to compare the performance of models on the dataset.<br>

<h3>• GradCAM:</h3> This folder contains code for the GradCAM algorithm, which is used to generate heatmaps that visualize the important regions of an image that a deep learning model is using to make its predictions.<br>

<h3>• Model and dataset comparison:</h3> This folder contains code for comparing the performance of different machine learning models on various datasets.<br>

<h3>• SampleTesting:</h3> This folder contains code for running sample tests on all models on dataset3. These tests are used to evaluate the performance of the models.<br>

<h3>• TSNE:</h3> This folder contains code for the t-SNE algorithm, which is used to visualize high-dimensional data in a low-dimensional space<br>

<h3>• Transfer learning:</h3> This folder contains code for comparing the metrics of transfer learning models vs. training models from scratch. Transfer learning involves using a pre-trained model as a starting point for a new model, rather than starting from scratch.<br>

<h3>• Optimization:</h3> This folder contains code for optimizing a model with different set of learning rate. Optimization involves finding the best set of hyperparameters for a model to improve its performance.<br>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield1]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-shield2]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge


[contributors-url1]:https://github.com/AhmedAlagha1418
[contributors-url2]: https://github.com/mahdihosseini



