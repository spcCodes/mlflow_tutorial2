# mlflow_tutorial2


MLFLOW_TRACKING_URI=https://dagshub.com/spcCodes/mlflow_tutorial2.mlflow \
MLFLOW_TRACKING_USERNAME=spcCodes \
MLFLOW_TRACKING_PASSWORD=3f7a9c79d5525e15df189302054536f641f31cfa \
python script.py



export MLFLOW_TRACKING_URI=https://dagshub.com/spcCodes/mlflow_tutorial2.mlflow

export MLFLOW_TRACKING_USERNAME=spcCodes 

export MLFLOW_TRACKING_PASSWORD=3f7a9c79d5525e15df189302054536f641f31cfa


# set up mlflow in aws


## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
Also install aws cli in your local machine
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv


sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-2

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-23-22-147-111.compute-1.amazonaws.com:5000/
```