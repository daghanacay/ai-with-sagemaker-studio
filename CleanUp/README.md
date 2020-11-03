# Clean up

## Clean up Step 2 (bank data)
In order to avoid cost accruing after workshop please clean up your resources as follows

- Clean up the Sagemaker role: go to AWS AIM console and remove the Sagemaker role. you should have stored from the first step and it should like "AmazonSageMaker-ExecutionRole-20201102T121769" if you have not copied it search for Sagemaker role in the IAM console with today's date.
- Clean up Sagemaker S3 bucket: go to S3 bucket and delete the bucket you have created it should be similar to Sagemaker-us-east-1-[your account id]
- Clean up auto generated models: go to "Inference -> Models" and delete the models generated in this workshop
- Clean up your Sagmaker studio domain if you wish however this uses a minimal 

## Clean up Step 3 (image processing)

- Clean up endpoint configuration: 
- *Clean up endpoint*: *This very costly at AUD 7 per day* so please delete this before you leave today. Go to AWS Sagemaker Console “Amazon Sagemaker -> Inference -> Endpoints” and delete “DEMO-imageclassification-ep*” or delete from the Jupiter notebook, WARNING: you can only delete from workbook if you have not stopped the kernel.

## Clean up Sagemaker domain

- Clean up your Sagmaker studio domain using the instruction [here](https://docs.aws.amazon.com/sagemaker/latest/dg/gs-studio-delete-domain.html) 