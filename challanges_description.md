## Challanges and solutions

During the completion of this task, I encountered challenges that took more time compared to other parts.

### 1. Didn't understand how to load files to EFS.
#### Solution:
> I manually created EC2 with ECS security group rights and mounted EFS using the NFS client. Then went to the mounted folder /mnt and created index.html using cat.

### 2. Couldn't resolve ECS service failures.
#### Error:
> ResourceInitializationError: failed to invoke EFS utils commands to set up EFS volumes: stderr: Failed to resolve "filesystem-id.efs.us-east-1.amazonaws.com".

#### Solution:
> VPC had the parameter Enable DNS hostnames: false. I changed to true and everything mounted perfectly.

### 3. Had difficulties during automation of pushing index.html to EFS using EC2
#### Challenge:
> EC2 was created using CloudFormation, and UserData was executed, but index.html was not pushed to EFS.

#### Solution:
> To troubleshoot I added script to stdout and stderr to files. Then manually connected to EC2 and checked the contents of these files.

### 4. Had difficulties with creating list parameters
#### Challenge:
> I wanted to create a list parameter (e.g. for public subnets CIDRs) with two default values and use the Select function to refer to each by indexes. I tried various solutions (including list\<string\>, CommaDelimitedList) but could not resolve an error.

#### Error:
> ValidationError - Template format error: Every Default member must be a string.

#### Solution:
> I still could not finally resolve that error, so I used a more straightforward approach: used only separate string and number parameters without lists. 