All building on AWS starts with creating an AWS account. The AWS homepage (https://aws.amazon.com) provides instructions on setting up an account after selecting "Create an Account".
  
  For this course the Basic plan is used.

The first step of building on AWS is understanding how to launch an EC2 instance. This is done through the EC2 dashboard, accessed by choosing "EC2" under the Services dropdown in the upper left.

Any region can be chosen, but it should remain consistent for all exercises within a project. The region can be changed in the upper right.

Launching an EC2 instance:
* On the EC2 dashboard, select "Launch Instance"
* On the next page, select the Linux AMI option. Linux 2 AMI is not advisable.
* t2.micro is suggested hardware configuration due to being free-tier eligible.
* Most instance details on the next page are best left as defaults. Expand the advanced details section and under "User data" copy over the userdata.txt file.
