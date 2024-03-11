# s3-website-codepipeline-cicd
This Repo targets to create S3 static website hosting through Codepipeline

Codecommit -----> Codepipeline ----> Code deploy (S3 Bucket)



#Step 1 : Create Codecommit repo

#Step 2 : Create Git Credentials for IAM to clone repo, provide access.

#Step 3 : add required files

#Step 4 : Create codepipeline, add repo from code commit as source

#Step 5 : skip code build 

#Step 6 : Code deploy through S3


# When you create S3 bucket for s3 website hosting, Enable public access and enable s3 website hosting in properties and add Below Bucket Policy 
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::s3-website-prod-bucket-01/*"
        }
    ]
}
