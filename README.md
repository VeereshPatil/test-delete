# example-dvc-mlflow-s3

## In case of new S3 bucket [PreRequisite step]
1. Clone repository and create dataset folder in parent directory and add wine-quality.csv in the dataset folder
2. Set AWS S3 credentials in .dvc/config file or set using "dvc remote modify {key value}" command
3. dvc add dataset
4. dvc push to remote

## Steps to pull data from existing remote dvc s3 cache:
1. Clone Repository
2. Set AWS S3 credentials in .dvc/config file or set using "dvc remote modify {key value}" command
3. dvc pull

### .dvc/config file:

[core]

    remote = s3remote
    
['remote "s3remote"']
    
    url = S3://dvc-example
    
    endpointurl = http://{AWS_S3_URL}:{PORT}/
    
    access_key_id = admin
    
    secret_access_key = admin
    
    use_ssl = false
   
