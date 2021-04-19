# AWS Data Engineering Pipeline

Description: This project is to set up a data pipeline using AWS, replicating the structure below, which is from here: [https://github.com/noahgift/awslambda](https://github.com/noahgift/awslambda).

![data engineering pipeline](https://user-images.githubusercontent.com/58792/55354483-bae7af80-547a-11e9-9909-a5621251065b.png)

1. Create a new Cloud9 environment dedicated to this project.
2. Create a "fang" table in DynamoDB
3. Create an SQS queue
4. Create s3 bucket
5. Build product Lambda function
   -Use `sam init`
   -Select 1,2,4
   -Name your Lambda function "producer"
   -Set up virtual environment and source it
    -```python3 -m venv ~/.comprehendProducer source ~/.comprehendProducer/bin/activate```
   -Add code to `app.py`
   -Install requirements
   -Create repository in ECR and use its URI
   -Build and deploy using `sam -build` and `sam deploy --guided`
   -Navigate to Lambda in the console and ensure the Lambda has a user with appropriate permissions.
   -Deactivate environment
6. Build consumer Lambda function
   -Use `sam init`
   -Select 1,2,4
   -Name your Lambda function "producer"
   -Set up virtual environment and source it
    -```python3 -m venv ~/.comprehendProducer source ~/.comprehendProducer/bin/activate```
   -Add code to `app.py`
   -Install requirements
   -Create repository in ECR and use its URI
   -Build and deploy using `sam -build` and `sam deploy --guided`
   -Navigate to Lambda in the console and ensure the Lambda has a user with appropriate permissions.
   -Deactivate environment
7. Add triggers to the Lambda functions as seen [here](https://www.youtube.com/watch?v=zXxdbtamoa4), the producer trigger is at 30 min and the consumer trigger is at 42 min.
8. Review sentiment results in s3 bucket.


