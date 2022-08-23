# aws-labs-jenkins-codedeploy
>This project is a rebuilding of following AWS blog.
>https://aws.amazon.com/blogs/devops/setting-up-a-ci-cd-pipeline-by-integrating-jenkins-with-aws-codebuild-and-aws-codedeploy/

## Step 1
### Provisioning required resources using CloudFormation template. Following resources will be created.
- VPC, RT, IGW, 2 Public Subnets
- AutoScalingGroup to spawn Tester instances fronted by ALB
- Fresh Jenkins Server running on Amazon Linux AMI
- CodeBuild Project
- CodeDeploy Application / Deployment Group
- S3 Bucket to store source and artifacts

## Step 2
### Create IAM Jenkins user for the project. 
- Go to IAM console
- Add new user with only "Access Key"
- Attach JenkinsPolicy to the user. The policy includes every permissions required for Jenkins project to interact with CodeBuild, CodeDeploy and Put/Get objects from S3 Bucket
- Note down access key and secret

## Step 3
### Configure Jenkins Server
- SSH to server to get password by
~~~
sudo more /var/lib/jenkins/secrets/initialAdminPassword
~~~
- Finish setting up
- Install plugins
    - CodeBuild Plugin
    - CodeDeploy Plugin
    - HTTP Request
    - File Operation

## Step 4
### Create Freestyle Project
- 

## Diagram
![diagram](diagram.jpg)