
# Machine Learning Models with Auto AI 

In this workshop you will learn how to build and deploy your own AI Models.

For the workshop we will be using AutoAI, a graphical tool that analyses your dataset and discovers data transformations, algorithms, and parameter settings that work best for your problem setting.

Using AutoAI, you can build and deploy a machine learning model with sophisticated training features and no coding.

We will a public dataset to build and deploy model pipelines, and analyse the outcome.

## Set up

Follow the steps in [this module](https://github.com/IBM/ddc-2021-jumpstart-your-journey/tree/main/workshop/project-setup) to set up your IBM cloud account and Watson Studio Service.

- Once you are in Watson Studio, you can create a new project by clicking on `Get Started` and `New Project`, or `Create Project` or work with an exisiting project as well. 


![](https://github.com/YaminiRao/Data-Visualisation-with-Python/blob/master/Images/Watson_Studio.png)


### Once you are in the Project Dashboard, click on "Add to Project" on the top right and select AutoAI Experiment 

![](https://github.com/IBMDeveloperUK/Machine-Learning-Models-with-AUTO-AI/blob/master/Images/AutoAI.png)

### Associate a Machine Learning service 

- Give your Auto AI experiment a unique name 
- Associate a Watson Machine Learning service, if you have already created one this will apear in the dropdown or you can create a new one. 
- Once this is done, click the "Reload" button for your Machine Learning service to appear 

![](https://github.com/IBMDeveloperUK/Machine-Learning-Models-with-AUTO-AI/blob/master/Images/MLservice.png)


- Your machine learning service will appear under "Associated services"
- Click Create 

### Upload your Data Sets

- Browse and add your Data source 
- The dataset for this workshop have been acquired from : 

https://www.kaggle.com/noordeen/insurance-premium-prediction


![](https://github.com/IBMDeveloperUK/Machine-Learning-Models-with-AUTO-AI/blob/master/Images/Data_Source.png)

- Once your dataset is successfully uploaded, you will see an option to choose your prediction column. Optionally, you can also refer to the experiment settings to make changes to the AutoAI Experiment. Once done, click on Run Experiment. 

![](https://github.com/IBMDeveloperUK/Machine-Learning-Models-with-AUTO-AI/blob/master/Images/experiment.png)

## Completed AutoAI experiment 

![](https://github.com/IBMDeveloperUK/Machine-Learning-Models-with-AUTO-AI/blob/master/Images/experiment-2.png)


### In this module we will work through the different aspects of configuring our AutoAI experiment and discuss the pipelines that are created. 

