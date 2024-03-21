Hosting then Static website with S3 & Cloudfront.
----------------------------------------------------------------------
1: Set up an S3 bucket and upload the static website code to it.

2: Go to Properties and enable 'Static website hosting'. Set up the home page file.

3: When website hosting is enabled, navigate to 'Permission' and enable public access. The bucket policy should be configured as follows.


	{
	    "Version": "2012-10-17",
	    "Statement": [
	        {
	            "Sid": "pub-object",
	            "Effect": "Allow",
	            "Principal": "*",
	            "Action": "s3:GetObject",
	            "Resource": "arn:aws:s3:::1239test123/*"
	        }
	    ]
	}

 
4: To request a new certificate, go to the Certificate Manager dashboard and request one. Configuring the DNS record will validate the certificate (AWS Route 53).

5: Confirm the certificate and then go to the CloudFront dashboard to configure all necessary items and create the distribution. 

6: The public DNS end-point will be received after the distribution is created.

7: Creating an 'A' record with the aliase is necessary once we have the Cloudfront endpoint. 
