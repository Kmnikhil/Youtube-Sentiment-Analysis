## Youtube Sentimental Analysis

### Plan
1, Data Collection

2, Data preprocessing & EDA

3, Building baseline models

4, Setup Mlflow server on AWS

5, Improve baseline model
    
    -> BOW, TF-IDF
    -> Max feature
    -> Handling imbalance data
    -> Hyperparameter Tuning with multiple models
    -> Stacking model
6, Build ml pipeline using dvc

7, Add model to model registry

8, CICD workflow

9, Dockerizing

10, Deploying - AWS

11, Github

## MLflow setup on AWS
1. Login AWS console
2. Create IAM user with Adminitrator Access
3. Export the credential in your aws cli by running 'aws configure'
4. create s3 bucket
5. create EC2 machine (ubuntu) & add security groups 5000 port.

### Run the following command on EC2 machine
1. sudo apt update
2. sudo apt install python3-pip
3. sudo apt install pipenv
4. sudo apt install virtualenv
5. mkdir mlflow
6. cd mlflow
7. pipenv install mlflow
8. pipenv install awscli
9. pipenv install boto3
10. pipenv shell
11. aws configure ## set aws credential

12. mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-bucket2805 --allowed-host * --cors-allowed-origin *    ##finally we need to connect with s3 bucket
