---
layout: post
---

Install AWS CLI Ubuntu 20.04
----------------------------
Reference 1: https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-linux.html

1. curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
2. unzip awscliv2.zip
3. sudo ./aws/install
4. verified `aws --version`

Copy Local folder to S3
-----------------------
1. Create the temporary specific pragmatic user with full s3 access permission.
2. Set credentials using `aws configure` cmd then Enter **Access key** and **Access secret** that received after creation of user.   
3. Verified using `aws s3 ls` cmd
4. Give permission for 'aws' cmd like `755` temp or set credentials for root user
4. Recursively copying local files to S3 using `aws s3 cp myDir s3://{bucket_name} --recursive` cmd or you can sync using `aws s3 sync myDir s3://{bucket_name}` (no need --recursive when sync)

How to use S3 References
------------------------
1. https://adamtheautomator.com/upload-file-to-s3/ (create user)
2. https://stackoverflow.com/a/41614752/4066205
3. https://docs.aws.amazon.com/cli/latest/reference/s3/cp.html


