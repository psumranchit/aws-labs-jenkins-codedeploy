# aws-labs-jenkins-codedeploy
>This project is a rebuilding of following AWS blog.
>https://aws.amazon.com/blogs/devops/setting-up-a-ci-cd-pipeline-by-integrating-jenkins-with-aws-codebuild-and-aws-codedeploy/

## Step 1
### Provisioning required resources using CloudFormation template. Following resources will be created.
- Fresh Jenkins Server running on Amazon Linux AMI
- AutoScalingGroup to spawn Tester instances fronted by ALB
- VPC, RT, IGW, 2 Public Subnets
- CodeBuild Project
- CodeDeploy Application / Deployment Group
- S3 Bucket to store source and artifacts



## Diagram
![diagram](diagram.jpg)