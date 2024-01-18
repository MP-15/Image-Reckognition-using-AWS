# E-Curio
Cloud Deployment Model Project

AWS (Amazon Web Services) is a cloud computing platform that offers infrastructure as a service (IaaS) and platform as a service (PaaS) service. AWS services provide scalable computing, storage, databases, analytics, and other services. AWS helps businesses grow up by providing database storage, computational capacity, content distribution, and networking, among other services. It allows you to pick and choose your desired solutions while only paying for the services you use. AWS is cost-effective, which means it lets you save money while delivering more value without sacrificing application speed or user experience. AWS provides various remote cloud services for application development, such as analytics, blockchain, and artificial intelligence (AI), and can support individuals and businesses in their development and long-term success. This project is completed using Amazon Web Services. The project is related to image detection/recognition. We used following of the services while creating this project: -

# 1. Amazon IAM
AWS Identity and Access Management is the tenth and final service on our list of the most popular AWS services (IAM). Without a doubt, access and what is accessed have a lot to do with security. This service 
ensures that sensitive data and AWS resources are adequately protected. It can also be utilized in conjunction with your company's two-factor authentication and multi-factor authentication systems. It's just another layer of protection that never hurts

# 2. Amazon EC2 
You don't have to spend money on expensive physical services. Instead, you may use Amazon EC2 to build virtual machines while also managing other server functions like ports, security, and storage. Spend less time on server maintenance and more time on key projects. Amazon EC2 is unquestionably one of the most popular and fastest-growing AWS offerings.

# 3. Amazon S3
We now live in the Big Data era. It's been dubbed "the never-ending data flood" by some. As a result, we require more storage than we have in the past. S3 (Amazon Simple Storage Service) has saved the day. Understandably, this would be included in our top ten AWS services list. It provides a file storage solution that is both secure and redundant. It also keeps data in three data centers in different parts of the country. There's even more. Amazon S3 also has PCI-DSS, HIPAA/HITECH, and FedRAMP connections to assist in avoiding breaches. You have data flexibility while experiencing near-zero latency.

# 4. Amazon Rekognition
Amazon Rekognition is a cloud-based computer vision technology that provides software as a service. Amazon Rekognition extracts information and insights from your photographs and videos using pre-trained and configurable computer vision (CV) capabilities. Adding image and video analysis to your applications is simple with Amazon Rekognition. Simply upload a photo or video to the Amazon Rekognition API, and the service will recognize objects, people, text, scenes, and activities. It can also detect any offensive content.

# Working 

1. We created a S3 bucket “ecurio” in Amazon S3 management console and uploaded the images we wanted to use for the image detection.
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/20fb1bac-0ab4-4ee4-8111-13f0b6db8f56)

2.	We logged into IAM management console to create roles for our respective project bucket.
3.	We used “AWSLambdaExecute”; “AmazonRekognitionFullAccess” and “
4.	Lambda execute will give access to cloud virtual logs to lambda function and the access to S3 buckets so that we don't need to provide read only access to S3 bucket explicitly.
   
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/fe90057b-24e6-4704-839d-20364e9812d1)

5. We used Lambda function from AWS Service of IAM Roles.
6. We used “AWSLambdaExecute”; “AmazonRekognitionFullAccess”.
7. Lambda execute will give access to cloud virtual logs to lambda function and the access to S3 buckets so that we don't need to provide read only access to S3 bucket explicitly.
   
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/c690e93f-d12a-4b9d-ad46-96a774253375)
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/388cb239-881f-4688-8e92-844b7e547be3)

8.	Next, we created “ecurio_role”.
    
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/4c5bdcc9-8f6d-467d-b08f-8d9dc7614383)
   ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/03de4098-4156-4884-af7a-e248864c4a19)

9.	Creating “mycdmprojectfunc” for Python 3.9 runtime.
    
    ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/3f2fadda-c026-475c-817e-2ec2b7d79df6)
    ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/b4a62e2b-b620-425d-a904-a57698cb4eb5)
  	
10.	We uploaded our source code and tested the code.
    
    ![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/25bad001-dda7-4193-96e6-1046bba2a5ff)
   	![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/c931f88b-f5db-4df0-b700-56ffa6319cd8)
   	![image](https://github.com/MP-15/Image-Reckognition-using-AWS/assets/80661516/1fe0d28a-f4fa-4e6f-b9fb-09f8f04d5be0)

# All Label output that we got in our project:
{'Labels': [{'Name': 'Person', 'Confidence': 99.44908905029297, 'Instances': [{'BoundingBox': {'Width': 0.5324793457984924, 'Height': 0.8127124309539795, 'Left': 0.19544893503189087, 'Top':
0.1143421158194542}, 'Confidence': 99.44908905029297}], 'Parents': []}, {'Name': 'Human', 'Confidence': 99.44908905029297, 'Instances': [], 'Parents': []}, {'Name': 'Sitting', 'Confidence': 97.13262176513672, 'Instances': [], 'Parents': [{'Name': 'Person'}]}, {'Name': 'Furniture', 'Confidence': 75.2845458984375, 'Instances': [], 'Parents': []}, {'Name': 'Indoors', 'Confidence': 74.0599365234375, 'Instances': [], 'Parents': []}, {'Name': 'Table', 'Confidence': 72.97395324707031, 'Instances': [], 'Parents': [{'Name': 'Furniture'}]}], 'LabelModelVersion': '2.0', 'ResponseMetadata': {'RequestId': 'eeb55713-746f-4abd-a13b-98ef68433da6', 'HTTPStatusCode': 200, 'HTTPHeaders': {'x-amzn-requestid': 'eeb55713-746f-4abd-a13b- 98ef68433da6', 'content-type': 'application/x-amz-json-1.1', 'content-length': '693', 'date': 'Wed, 16 Mar 2022 19:09:43 GMT'}, 'RetryAttempts': 0}}








   


