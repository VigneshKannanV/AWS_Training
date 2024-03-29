# AWS Account Setup
<br/>After Signing Up as a new root user, an IAM User has been created under the root user account and the necessary policies have been created.
<br/>A new tag was created [Tag Name - Hartford, Tag Key - Training].
<br/>All the resources created by this IAM user has been tagged with that tag name.

![Screenshot (39)](https://user-images.githubusercontent.com/60065716/115720256-87965700-a39a-11eb-921f-3ec5e9e1ef9e.png)


# Creation of S3 Bucket
<br/>A new S3 Bucket named ‘1766-vigneshawsbucket’ was created in the ‘US_EAST-2’ region and made not open to the public.

![Screenshot (34)](https://user-images.githubusercontent.com/60065716/115718096-6e8ca680-a398-11eb-9c4e-9a1768c18a28.png)

<br/>Three folder - A, B, C was created and some files were put in those folders.

![Screenshot (35)](https://user-images.githubusercontent.com/60065716/115718671-f8d50a80-a398-11eb-9988-6bc2b416fe33.png)

![Screenshot (47)](https://user-images.githubusercontent.com/60065716/115719971-3b4b1700-a39a-11eb-9a80-cf6ef4eb30cf.png)


# Flask App Creation
<br/>A flask app to get the folder name present in the S3 Bucket as the input and display the contents of that folder is created (using boto3) and tested locally.

![Screenshot (50)](https://user-images.githubusercontent.com/60065716/115719417-b06a1c80-a399-11eb-83b1-828076d0526b.png)

![Screenshot (46)](https://user-images.githubusercontent.com/60065716/115719495-c4158300-a399-11eb-97bd-9ca5598680d2.png)


# Creating an EC2 instance 
<br/>An EC2 instance was created in the same region where the S3 Bucket was created.

![Screenshot (37)](https://user-images.githubusercontent.com/60065716/115723977-23759200-a39e-11eb-8c79-a2373db5c837.png)

<br/>The Security Group is configured to allow incoming traffic only through 8085.

![Screenshot (48)](https://user-images.githubusercontent.com/60065716/115729976-81f13f00-a3a3-11eb-9c4c-a74dba228759.png)

<br/>A connection was made to the instance using it's public DNS via the Ubuntu app installed on the local machine.

![Screenshot (38)](https://user-images.githubusercontent.com/60065716/115725645-aa773a00-a39f-11eb-88c5-81d36dabddd2.png)

![Screenshot (40)](https://user-images.githubusercontent.com/60065716/115727091-ec54b000-a3a0-11eb-9eee-1e4a7690aa86.png)


# Deploying the Flask app
<br/>All the following requirements are installed to deploy and run the flask application

* AWS CLI V2
  <br/>The AWS CLI V2 is installed so that it can read all the credentials from a config file to avoid hard codind credentials in the code.
  <br/>The following commands are used to install it - 
  <br/>-- curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
  <br/>-- unzip awscliv2.zip
  <br/>-- sudo ./aws/install
  <br/>To craete a new configuration file use the following command and enter the credentials - 
  <br/>-- aws configure
  
* Python 3 
  <br/>Python 3 and the package management system is installed using the following commands -
  <br/>-- sudo apt-get update
  <br/>-- sudo apt-get install python3
  <br/>-- sudo apt-get insatll python3-pip
  
 * Packages 
  <br/>The required packages to run the flask application such as boto3 are installed using the following commands 
  <br/>-- pip3 install boto3
  
![Screenshot (53)](https://user-images.githubusercontent.com/60065716/116087722-c68c1b80-a6be-11eb-8ac4-cd788b87f35a.png)

<br/>Here, then codes are successfully migrated to that instance.(Simple file creation and copy)

![Screenshot (54)](https://user-images.githubusercontent.com/60065716/116088903-f0920d80-a6bf-11eb-8514-f592dbca5aaf.png)

![Screenshot (55)](https://user-images.githubusercontent.com/60065716/116088923-f4be2b00-a6bf-11eb-9490-0a095bbc4bcc.png)

<br/>The flask app was deployed and run app.py file to run the application

![Screenshot (41)](https://user-images.githubusercontent.com/60065716/115730619-18256500-a3a4-11eb-933c-1cf66236de22.png)

<br/>The flask application ran successfully and accessed via the EC2-public URL at the port 8085 (https://3.143.170.33:8085)

![Screenshot (42)](https://user-images.githubusercontent.com/60065716/115730642-1cea1900-a3a4-11eb-90b4-88093fde7d98.png)

![Screenshot (44)](https://user-images.githubusercontent.com/60065716/115730711-296e7180-a3a4-11eb-8027-fa8614895580.png)


# Billing Status
<br/>Below are the screenshots attached for estimated total and the costs grouped by services and tags. 

![Screenshot (45)](https://user-images.githubusercontent.com/60065716/115730884-4efb7b00-a3a4-11eb-9daa-0588b3e997a2.png)

![Screenshot (51)](https://user-images.githubusercontent.com/60065716/116087553-98a6d700-a6be-11eb-899d-b348d14844c9.png)

![Screenshot (52)](https://user-images.githubusercontent.com/60065716/116087567-9d6b8b00-a6be-11eb-8c7c-f4700b496c3e.png)

