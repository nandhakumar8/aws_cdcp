[Previous: Create Roles and User](IAM.md)


## EC2 Creation:
Create 2 ec2 instances with **Security Group: AllTraffic** and tags as dev and web
#### Install and prepare the CodeDeploy agent on webserver
Attach **EC2-S3** Role with web server
Give following commands as **User Data** 

```sh

#!/bin/bash
yum update
yum install ruby -y
yum install wget -y
wget https://aws-codedeploy-us-east-1.s3.amazonaws.com/latest/install
chmod +x install
./install auto

```

[Next: Code Files](CODE.md)
