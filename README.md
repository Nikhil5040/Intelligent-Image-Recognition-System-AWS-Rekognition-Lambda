# Intelligent-Image-Recognition-System-AWS-Rekognition-Lambda

- Install aws-shell
```
pip install aws-shell
```

- Configure
```
aws configure
```

- Create a collection on aws rekognition
```
aws rekognition create-collection --collection-id famouspersons --region us-east-1
```

- Create table on DynamoDB
```
aws dynamodb create-table --table-name face_recognition --attribute-definitions AttributeName=RekognitionId,AttributeType=S --key-schema AttributeName=RekognitionId,KeyType=HASH --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1 --region us-east-1
```

- Create S3 bucket
```
aws s3 mb s3://famouspersons-images12 --region us-east-1
```
