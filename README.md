# Brain-Tumor-Survival-Prediction

### Overview
I implemented three different models to predict brain tumor survival of a patient based on
the dataset. The dataset consists of brain tumor MRI exams derived from the MICCAO
Brain Tumor Segmentation Challenge. For preparing the data set for survival prediction, the
brain MRI volume was cropped to the boundaries of the tumor and resampled to form a uniform
3D volume of shape (96,96,96,4). I created a custom config dictionary to create generators to
have two separate target labels, for survival scores and tumor segmentation. The generator
uses 096*vox-org to get the correct client template.

### Models
Model 1: Fully Convoluted Network<br/>
Model 2: Contracting and Expanding layers with global regression type loss function<br/>
Model 3: Incorporated SE Net with Pre Trained Auto Encoder strategy<br/>

### Results
I evaluated the model based the Mean Absolute Error. Model 1 performed the best. The outputs and
the statistics of the training and validation cohort is stored in results.csv
