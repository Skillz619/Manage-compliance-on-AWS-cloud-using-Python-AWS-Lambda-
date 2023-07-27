# Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-

As a cloud engineer team we take care of AWS env and make sure it is in compliance with the organizational policies.
We use AWS Cloud Watch in combination with AWS Lambda to govern the resources according to the policies.
For Ex: We trigger a Lambda Function when an Amazon Elastic Block Store(EBS) volume is created. We use CloudWatch events.
It allows us to monitor and respon to EBS volumes that are of type Gp2 and convert them to GP3.


So the company policy is to use gp3 type only as it is faster and other things. So anyone who is creating an EBS will need to make gp3 itself and if they don't for any reason it should automatically trigger a event and create the right type - gp3.

# Pre - Req:
1)We need to create a Lambda function

2)Create Aws cloudwatch 

3)Integrate cloudwatch with Lambda function - so that lambda function gets triggered by cloudwatch when EBS volume is created.



Create a Lambda Function
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/32a358cd-bd62-4c0e-a99e-3ac2d9f708c8)
