# AWS Account Setup

After Signing Up, an IAM User has been created under the root user account and the necessary policies have been created.
A new tag was created and all the resources created by this IAM user has been tagged with that tag name.

![Screenshot (39)](https://user-images.githubusercontent.com/60065716/115720256-87965700-a39a-11eb-921f-3ec5e9e1ef9e.png)


# Creation of S3 Bucket

A new S3 Bucket named ‘1766-vigneshawsbucket’ was created in the ‘US_EAST-2’ region and made not open to the public.

![Screenshot (34)](https://user-images.githubusercontent.com/60065716/115718096-6e8ca680-a398-11eb-9c4e-9a1768c18a28.png)

Three folder - A, B, C was created and some files were put in those folders.

![Screenshot (35)](https://user-images.githubusercontent.com/60065716/115718671-f8d50a80-a398-11eb-9988-6bc2b416fe33.png)

![Screenshot (47)](https://user-images.githubusercontent.com/60065716/115719971-3b4b1700-a39a-11eb-9a80-cf6ef4eb30cf.png)


# Flask App Creation

A flask app to get the folder name present in the S3 Buckrt as the input and display the contents of that folder is created and tested locally.

![Screenshot (50)](https://user-images.githubusercontent.com/60065716/115719417-b06a1c80-a399-11eb-83b1-828076d0526b.png)

![Screenshot (46)](https://user-images.githubusercontent.com/60065716/115719495-c4158300-a399-11eb-97bd-9ca5598680d2.png)

# Creating an EC2 instance

An EC2 instance was created in the same region where the S3 Bucket was created.

![Screenshot (36)](https://user-images.githubusercontent.com/60065716/115720043-5027aa80-a39a-11eb-85fe-81dab3ee16f9.png)
