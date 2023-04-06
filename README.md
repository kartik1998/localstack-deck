## LocalStack Cloud

<i> Run AWS locally </i>

#### Outline

1. Create a bucket from console
2. Static website from bucket created in the console
3. Create table in DynamoDB
4. Insert items in DynamoDB Table
5. Retrieve (scan) items in DynamoDB Table
6. Introduction to CDK
7. Lambda Function to get data from DynamoDB
8. API Gateway to call lambda from static website
9. Display data in static website from API Gateway

### Commands

```
create s3 bucket
aws s3 mb --endpoint-url http://localhost:4566 --region us-east-1 "s3://static-s3-bucket"

now block public access
aws s3api --endpoint-url http://localhost:4566 put-public-access-block \
	--bucket static-s3-bucket \
	--public-access-block-configuration "BlockPublicAcls=false,IgnorePublicAcls=false,BlockPublicPolicy=false,RestrictPublicBuckets=false"

```
