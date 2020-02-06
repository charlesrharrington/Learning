All building on AWS starts with creating an AWS account. The AWS homepage (https://aws.amazon.com) provides instructions on setting up an account after selecting "Create an Account".
  
  For this course the Basic plan is used.

The first step of building on AWS is understanding how to launch an EC2 instance. This is done through the EC2 dashboard, accessed by choosing "EC2" under the Services dropdown in the upper left.

Any region can be chosen, but it should remain consistent for all exercises within a project. The region can be changed in the upper right.

Launching an EC2 instance:
* On the EC2 dashboard, select "Launch Instance"
* On the next page, select the Linux AMI option. Linux 2 AMI is not advisable.
* t2.micro is suggested hardware configuration due to being free-tier eligible.
* Most instance details on the next page are best left as defaults. Expand the advanced details section and under "User data" copy over the [userdata.txt](https://github.com/charlesrharrington/Learning/blob/master/aws/edx/userdata.txt) file and choose next.
* Leaving the defaults for storage is suggested at this point and continuing on to the "Add Tags" page.
* Tags are a key/value pair, such as Name and (for this exercise) SamplePythonApp
* In the next section we add a security group. For now we'll be creating a new one - the name does not matter. For this new security group you can delete the roles such as the SSH role by clicking the X button at the end of its row.
* For this exercise, add in a new rule with a type of "Custom TCP Rule". The Port range should be 80, with a 0.0.0.0/0 Source.
* At this point we can review and launch the instance. Here we'll be proceeding without a keypair since this is just a sample EC2 instance.

The newly created EC2 instance will take a minute or two to set up fully. Once the status changes to "2/2 checks passed", select the instance and, under the description at the bottom, copy the IPv4 Public IP.

Open a new tab or window of the internet browser, paste in the IPv4 Public IP, and the resulting webpage should be running a sample python application.

To stay within free tier limits, it's recommended to terminate the sample EC2 instance at this point by selecting the instance, choosing Actions at the top, and terminating the instance.
