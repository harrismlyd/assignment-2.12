# Assignemnt 2.12

Given a Lambda function that is triggered upon the creation of files in an S3 bucket, answer the following:

1. What is the purpose of the execution role on the Lambda function?
2. What is the purpose of the resource-based policy on the Lambda function?
3. If the function is needed to upload a file into an S3 bucket, describe (i.e no need for the actual policies)
   - What is the needed update on the execution role?
   - What is the new resource-based policy that needs to be added (if any)?

Create a public github repository that has a README.md file, containing the above answers.

Submission is the url to your public github repository.

Answer : 

1. The execution role defines the permission that the function has when it runs.
For example, reading from the S3 bucket, writing to S3 or other services or accessing other AWS resources.

2. A resource based policy defines who or what can invoke the Lambda function.

3. For the execution policy, we need to grant the Lambda function to perform the s3:PutObject to upload the file. We should also specify the bucket resource arn where the Lambda function is allowed to upload the file to. 

For the resource based policy, we need to allow S3 permissions to invoke the Lambda function.
