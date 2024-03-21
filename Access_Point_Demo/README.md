**Access Point Creation.**


Deligating the restricted access to respective S3 bucket folders, to the IAM users / roles, via _S3 Access Point_.

Login to AWS Console.
:: S3 End configuration ::
1- Navigate to S3 Service > Create Bucket.
2- Open Created Bucket > navigate to permission > Bucket Policy (Configure Bucket policy to apply all objects)
3- Access Point > Create Access Point > Fill all the desired details like (Acess point name, Network Origin VPC / Public(Intyernet), Access Point Policy). If we want to access within the VPC from EC2 we can restrict access to specific VPC.

:: IAM End Configuration ::
1- Navigate to IAM Dashboard > Users > Create user
2- Select "User group" from left side menu > Create group > provide the sensiable name > select appropriate policy
3- Open Neweluy crated user > Navigate to Add permission > select created group > add permission.

Ready to test.  
