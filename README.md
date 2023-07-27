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

![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/fc7b1cfb-ce8a-4aa6-91a9-04d51a3791fa)

Make sure to test the test-event to see if lambda function is working
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/a6965f6a-377e-4875-b25c-6455605b9fc8)

Configure a CloudWatch rule to trigger a lambda function - > CloudWatch -> Events -> Rule - > Create Rule
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/f6b3e3f5-033f-4d8d-8f03-89b66266100b)

Attach the target lambda function (ebs-volume-check)
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/8c61b88b-266e-4251-ada5-611d0a7dd79a)

![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/853fa9e6-e90c-478b-9e38-dc85915b34b1)

Add the script to convert to gp3 in lambda
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/126961c4-43da-45fd-a482-7e3f27798a18)

GO to IAM to give the role
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/bf4188a1-6175-4fd7-a3ca-23982e2ad6e4)

give the actions
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/4975ad79-bad0-4f65-a2ac-00b34f7b0452)

![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/c3b5f7de-d9fa-4e84-a29b-7dd812d6e9e0)

Now create a gp2 volume
![image](https://github.com/Skillz619/Manage-compliance-on-AWS-cloud-using-Python-AWS-Lambda-/assets/43133388/828aaa34-3df4-4ff1-97c2-69589177d9bb)




    
