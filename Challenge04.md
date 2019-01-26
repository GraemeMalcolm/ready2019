# Challenge 5 - A Run in the Clouds

## Background

It's not just enough to be able to build a world class machine learning model, you need to know how to deploy it so that it can be consumed by team members, developers, and third parties to provide useful functionality to applications and services for Adventure Works customers.

In this challenge you will use *Azure Machine Learning Services* and the *Azure Machine Learning SDK* to operationalize your model as a scoring endpoint in the cloud (specifically, as a containerized web service), so that developers at Adventure Works and elsewhere can write consumer applications and use this scoring endpoint for prediction.

## Prerequisites

* A Data Science Virtual Machine (DSVM).
* Your code to train an image classification model (you can use your model from either of the previous two challenges).

## Challenge

Use the Azure Machine Learning SDK to:

1. Provision an Azure Machine Learning Workspace.
2. Deploy your model as a web service in a container.
3. Write Python code that uses your deployed model to predict the class of an image that was not included in the training or validation data (use Bing to find an appropriate image).

### Hints

* Your deployment must include a scoring script that loads your model, uses it to generate a prediction from the input data, and returns the prediction. Remember that you must apply any data transformations that were used to pre-process the training data to the input data.
* You need to specify the Python libraries used by your scoring script in a .yml file, so that they are installed in the container image when it is deployed.
* Pay careful attention to the expected formats for input and output data, which is exchanged over HTTP when using the deployed model.

## Success Criteria

* Deploy a working container image that hosts your model.
* Run Python code that successfully calls your deployed web service with new image data, and displays the prediction that it returns.

## References

* <a href="https://docs.microsoft.com/en-us/azure/machine-learning/service/overview-what-is-azure-ml" target = "_blank">What is Azure Machine Learning Service?</a>
* <a href="https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-deploy-to-aci" target="_blank">Deploy models with the Azure Machine Learning service</a>