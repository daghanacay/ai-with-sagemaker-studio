# AI/ML with Sagemaker-studio

## What is Sagemaker studio?

Amazon SageMaker is a cloud machine-learning platform that was launched in November 2017. SageMaker enables developers to create, train, and deploy machine-learning models in the cloud. SageMaker also enables developers to deploy ML models on embedded systems and edge-devices.

Sagemaker Studio is released Dec 2019 and integrates serverless principles of AWS and makes collaboration and training much more easy with less cost. We will look into 3 aspects of Sagemaker Studio

1. Autopilot: first inspects your data set, and runs a number of candidates to figure out the optimal combination of data preprocessing steps, machine learning algorithms and hyperparameters. Then, it uses this combination to train an Inference Pipeline, which you can easily deploy either on a real-time endpoint or for batch processing.
1. Existing algorithms (image processing): In this section, you’ll work your way through a Jupyter notebook that demonstrates how to use a built-in algorithm in SageMaker. More specifically, you’ll use SageMaker’s image classification algorithm, a supervised learning algorithm that takes an image as input and classifies it into one of multiple output categories. It uses a convolutional neural network (ResNet) that can be trained from scratch, or trained using transfer learning when a large number of training images are not available. In this section you’ll train the image classification algorithm from scratch on the Caltech-256 dataset.
3. Deploying models to production system: This is where you can expose your model to the world so anyone can benefit from it.
 

# AI/ML workflow

![image](images/ml-concepts.png)

Here is a high level view of AI/ML workflow.

## Generate example data
To train a model, you need example data. The type of data that you need depends on the business problem that you want the model to solve (the inferences that you want the model to generate). For example, suppose you want to create a model to predict a number given an input image of a handwritten digit. To train such a model, you need example images of handwritten numbers.

Data scientists often spend a lot of time exploring and preprocessing, or “wrangling,” example data before using it for model training. To preprocess data, you typically do the following:

- Fetch the data— You might have in-house example data repositories, or you might use datasets that are publicly available. Typically, you pull the dataset(s) into a single repository.

- Clean the data—To improve model training, inspect the data and clean it up as needed. For example, if your data has a country name attribute with values United States and US, you might want to edit the data to be consistent.

- Prepare or transform the data—You might perform additional data transformations to improve performance. For example, you might choose to combine attributes. If your model predicts the conditions that require de-icing an aircraft, instead of using temperature and humidity attributes separately, you might combine them into a new attribute to get a better model.

In Amazon SageMaker, you preprocess example data in a Jupyter notebook on your notebook instance. You use your notebook to fetch your dataset, explore it and prepare it for model training. You’ll create a Notebook Instance in the next section.

## Train a model
Model training includes both training and evaluating the model, as follows:

- Training the model—To train a model, you need an algorithm. The algorithm you choose depends on a number of factors. For more information, see the Amazon SageMaker documentation. 

- Evaluating the model—After you’ve trained your model, you evaluate it to determine whether the accuracy of the inferences is acceptable. You can evaluate your model using historical data (offline) or live data:

## Deploy the model
Traditionally, you do some re-engineering of a model to integrate it with your application, before deploying the model into production. With Amazon SageMaker hosting services, you can deploy your model independently, decoupling it from your application code. For more information, see Deploying a Model on Amazon SageMaker Hosting Services.

# Next Step

Now you are ready to go to (next step)[Step1-SetupSagemaker/README.md] 

# Requirements

In order to complete this workshop you’ll need an AWS Account, and an AWS IAM user in that account with at least full permissions to the following AWS services:

- AWS IAM
- Amazon S3
- Amazon SageMaker

# Costs: 

Some, but NOT all, of the resources you will launch as part of this workshop are eligible for the AWS free tier if your account is less than 12 months old. See the AWS Free Tier page for more details. An example of a resource that is not covered by the free tier is the ml.m4.xlarge notebook instance used in some workshops. To avoid charges for endpoints and other resources you might not need after you’ve finished a workshop, please refer to the [Cleanup Module](CleanUp/README.md).

This workshop should cost you around 1 AUD. if you leave your Sagemaker instances on it will cost daily AUD 5. In addition your Endpoint will cost AUD 7 per day at a total cost of ~AUD 15 per day. So please do not forget to do the clean up. 


# References

- [Sage maker auto pilot](https://aws.amazon.com/blogs/aws/amazon-sagemaker-autopilot-fully-managed-automatic-machine-learning/)
- [Sagemaker workshop](https://sagemaker-workshop.com/introduction/concepts.html)
- [Sagemaker workshop github](https://github.com/awslabs/amazon-sagemaker-workshop)
- [Sagemaker Studio Product page](https://docs.aws.amazon.com/sagemaker/latest/dg/studio.html)