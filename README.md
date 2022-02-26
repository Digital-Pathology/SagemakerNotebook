# SagemakerNotebook

Before initiating a training job, make sure you have completed the steps mentioned in SagemakerTemplate repository. 

## Hyperparameters

In the TrainingJob.ipynb, populate the hyperparameters dictionary with the hyperparameters you would like to pass to your algorithm. 

Make sure you have written code for parsing command line arguments in your algorithm for every hyperparameter you pass. 

## Data location

In the empty strings "train_data" and "test_data", input the location of your train and test data. Make sure to use only S3 URIs (s3://). 

## Instance Type

I have prepopulated the instance_type variable with the basic GPU instance. Available options are: 

- ml.g4dn.xlarge   (RAM: 16 GiB , CPU: 4 , Price: $0.7364/hr)
- ml.g4dn.2xlarge  (RAM: 32 GiB , CPU: 8 , Price: $0.94/hr)
- ml.g4dn.4xlarge  (RAM: 64 GiB , CPU: 16, Price: $1.505/hr)
- ml.g4dn.8xlarge  (RAM: 128 GiB, CPU: 32, Price: $2.72/hr)
- ml.g4dn.12xlarge (RAM: 192 GiB, CPU: 48, Price: $4.89/hr)
- ml.g4dn.16xlarge (RAM: 256 GiB, CPU: 64, Price: $5.44/hr)

## Unique Image Identifier

Populate the unique_image_identifier variable with the identifier you used while building and pushing the image in SagemakerTemplate. It is imperative that this variable be same that you used earlier so sagemaker can pull the correct image. 

## Start the training job

And that's it! Go ahead and run the Jupyter Notebook to initiate the training job. 

You can monitor the status of the training jobs by going to AWS Management Console > Amazon Sagemaker > Training (in the navigation menu) > Training Jobs. 

## Troubleshooting

While you should strive to solve your own problems in life, it is understandable that not everyone is as smart as I am so feel free to reach out to Ritik for help. 