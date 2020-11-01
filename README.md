
# Operationalizing ML Model in Azure, by Ranganath Venkataraman

## Overview
This project creates an AutoML model whose best performer is deployed to a HTTP endpoint for public consumption. Consumption is enabled through swagger, which uses 
a json interface to consume the endpoint. Effectively this allows 3rd parties to use an application produced within Azure.

## Architectural Diagram
*TODO*: Provide an architectual diagram of the project and give an introduction of each step. An architectural diagram is an image that helps visualize the flow of operations from start to finish. In this case, it has to be related to the completed project, with its various stages that are critical to the overall flow. For example, one stage for managing models could be "using Automated ML to determine the best model". 

## Key Steps
#### Step 1: upload dataset, compile and run AutoML experiment. Below are snapshots of the registered dataset and the completed AutoML run. 
##### Below are snapshots of the dataset in register and completed experiment.
![Dataset in register](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_1_Registered_Datasets_Showing_Bankmktg.png)
![Completed experiment](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_2_Completed_Run.png)
#### Step 2: the completed AutoML run points to a single-best model, a VotingEnsemble Classifier
##### Below is a snapshot of the best model.
![Best model](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_3_Best_Model.png)
#### Step 3: deploy the best performing model.
#### Step 4: enable application insights, which allows us to see how the deployment is functioning in terms of metrics like response time
##### Below is a snapshot showing Application Insights Enabled
![Application Insights enabled](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_4_Endpoint_ApplicationInsightsEnabled.png)
#### Step 5: run logs to monitor experiments and track results
##### Below are snapshots of log.py script running and output
![Logs.py script and output](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_5_running_logspy.png)
![Logs.py script and output](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_5_running_logspy_part_2.png)
#### Step 6: consume deployed model using swagger to create http: interface that illustrates API methods and responses for the model. 
##### Below are snapshots of swagger running on the localhost
![Swagger interface](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_6_swagger_localhost_methods_responses.png)
![Swagger interface](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_6_swagger_localhost_methods_responses_part_2.png)
### Step 7: update model endpoint.py script with the relevant URI and authentication. 
#### Proof of this is seen when endpoint.py is run with resulting output being 'yes' or 'no'
![Swagger interface](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_7_endpoint_script_out_showing_yes_no.png)
### Step 8: updated the automl pipeline creation notebook with relevant keys, URI, dataset etc. Running this script creates, publishes, and consumes final pipeline

## Screen Recording - below is my description of the modeling, deployment, and consume efforts involved in creating an accessible model that predicts banking purchase 
behaviors.
https://www.youtube.com/watch?v=FcC4ktLLKIk


