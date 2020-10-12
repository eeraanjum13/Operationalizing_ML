# Operationalizing Machine Learning

## **Overview:** 

In this Project, we are a given dataset (Bank-marketing dataset) which is trained using Azure ML. The completed model is then deployed and the endpoint is consumed.

**The steps include:**

1. Loading the given dataset and importing to Azure ML studio

2. Running the Automated ML experiment with the dataset and finding the best performing model with maximum accuracy.

3. To select the Best Model from the top performing models in Auto ML and deploying them.

4. Enabling Application insights in order to check performance of the deployed model's endpoint.

5. Swagger.json file is used for POST requests in the local host. This is done to see if the model is reponsive with POST requests.

6. Consuming the model by running endpoint.py file which will take features from the swagger.json file. 

7. Enabling an automated ML pipeline. 


## Step 1: Authentication

This step was not needed as a Virtual Machine was used where the authentication was already done.

## Step 2: Automated ML Experiment
**Data**

The dataset used in this project can be found [here](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv).

This dataset is first registered in the Auto ML Studio, shown in the image below. 

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/registered-dataset.PNG)

The ML experiment run in ML Studio is completed, as shown in the image below.
![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/auto-ml-completed.PNG)


After the experiment is completely run, few of the best performing models are listed with the highest accuracies. The top model is shown in the image below:

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/best-model.PNG)


## Step 3: Deploy the Best Model

The best model is selected from the Auto ML model. 

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/best-model.PNG)

The accuracy is close to 92% which shows that this model will be perfect for our dataset. The image below shows the 
details of the best chosen model.

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/step2-show-model.PNG)


## Step 4: Enable Application Insights

After deploying the model we need to enable the application insights. The configuration information in the form of config.json can 
be downloaded from the subscription of ML Studio. Then, keeping the config.json file in the same directory of the project, we can run the log.py file after adding
the system.update(enable_application_insights=TRUE). 

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/logs1.PNG)

After running logs.py:

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/log2.PNG)

This will enable the application insights of our model. 

![alt text](https://github.com/eeraanjum13/Operationalizing_ML/blob/main/application-insights-enabled.PNG)


## Step 5: Swagger Documentation


## Screencast of Project:

The screencast of the project in given [here](https://youtu.be/Y6VtDNEmzOg)
