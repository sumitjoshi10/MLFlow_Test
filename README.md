# MLFlow_Test

## For Dagshub

MLFLOW URL = https://dagshub.com/sumit.joshi9818/MLFlow_Test.mlflow

Use the following code for dagshub and mlflow
```bash
import dagshub
dagshub.init(repo_owner='sumit.joshi9818', repo_name='MLFlow_Test', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

```

## For AWS

1. Login to AWS Console
2. Create IAM User with Administrative Access
3. Get the access key it will require
4. Export the Crediential in AWS Cli by running command 'aws config'
5. Create one s3 Bucket
6. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command in EC2
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv

sudo pip3 install virtualenv

mkdir mlfow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

#Provide the credentials like in AWSCLI
aws config

mlflow server -h 0.0.0.0 --default-artifact-root s3://{bucket_name}

# set the aws uri into local terminal code
export MLFLOW_TRACKING_URI={URL_FROM_EC2}

```
