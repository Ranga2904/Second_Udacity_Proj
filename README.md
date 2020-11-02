
# Operationalizing ML Model in Azure, by Ranganath Venkataraman

## Overview
This project creates an AutoML model whose best performer is deployed to a HTTP endpoint for public consumption. Consumption is enabled through swagger, which uses 
a json interface to consume the endpoint. Effectively this allows 3rd parties to use an application produced within Azure.

## Architectural Diagram
This architectural diagram shows the flow from starting dataset to final completed pipeline. 
![Dataset in register](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Pipeline_drawings.png)


## Key Steps

#### Step 1: upload dataset, compile and run AutoML experiment. Below are snapshots of the registered dataset and the completed AutoML run. 
##### Below are snapshots of the dataset in register and completed experiment.

####### Snapshot of registered datasets showing Bank Marketing dataset
![Dataset in register](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_1_Registered_Datasets_Showing_Bankmktg.png)
####### Snapshot of completed AutoML run
![Completed experiment](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_2_Completed_Run.png)

#### Step 2: the completed AutoML run points to a single-best model, a VotingEnsemble Classifier

####### Snapshot of best model
![Best model](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_3_Best_Model.png)

#### Step 3: deploy the best performing model.
#### Step 4: enable application insights, which allows us to see how the deployment is functioning in terms of metrics like response time

####### Snapshot of Application Insights enabled
![Application Insights enabled](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_4_Endpoint_ApplicationInsightsEnabled.png)

#### Step 5: run logs to monitor experiments and track results

####### Snapshot of completed log.py script running and output
![Logs.py script and output](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_5_running_logspy.png)
![Logs.py script and output](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_5_running_logspy_part_2.png)

#### Step 6: consume deployed model using swagger to create http: interface that illustrates API methods and responses for the model. 

####### Snapshot of swagger running on localhost demonstrating inputs needed, methods used, and responses
![Swagger interface](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_6_swagger_localhost_methods_responses.png)
![Swagger interface](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_6_swagger_localhost_methods_responses_part_2.png)

#### Step 7: update model endpoint.py script with the relevant URI and authentication. Proof of this is seen when endpoint.py is run with resulting output being 'yes' or 'no'

####### Proof of updated endpoint
![endpoint.py](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_7_endpoint_script_out_showing_yes_no.png)

#### Step 8: updated the automl pipeline creation notebook with relevant keys, URI, dataset etc. Running this script creates, publishes, and consumes final pipeline.


####### Snapshots below show (in order) the running pipeline, pipeline endpoint, ACTIVE published pipeline with REST endpoint, Jupyter Notebook with RunDetailswidget, and the ML studio showing scheduled runs.
![Running pipeline](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_8_running_pipelie.png)
![Pipeline endpoint](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_9_pipeline_endpoint.png)
![Active pipeline with REST endpoint](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_10_dataset_automlmodule_Publ_PL_overview.png)
![Jupyter Notebook](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_11_RunDetails_StepRuns.png)
![ML Studio showing scheduled runs](https://github.com/Ranga2904/Second_Udacity_Proj/blob/main/Screenshot_12_ML_Studio_showing_Runs.png)


## Screen Recording - below is my description of the modeling, deployment, and consume efforts involved in creating an accessible model that predicts banking purchase behaviors.
https://www.youtube.com/watch?v=FcC4ktLLKIk

## Opportunities to improve the project going forward
I'd like to use the web interface for actually running the model i.e. input parameters to the website and get a result.  


