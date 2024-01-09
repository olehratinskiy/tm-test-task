# tm-test-task

## Deployment:
1. Clone this repository using ```git clone https://github.com/olehratinskiy/tm-test-task.git```
2. Log in to AWS Management Console, navigate to S3, and create a new bucket with your specific bucket name.
3. Open root_stack_template.yml and change the S3BucketName parameter default value to your S3 bucket name.
4. Then navigate to S3 and load all files from the templates folder.
5. After that go to the CloudFormation service, and select "Create stack" "With new resources".
6. In the block "Specify template" choose "Amazon S3 URL".
7. Input URL to your root template in S3 bucket ```https://s3.amazonaws.com/<bucket-name>/root_stack_template.yaml```
8. In the block "Provide a stack name" input the name for deploying the stack and click "Next" at the bottom of the page.
9. Scroll to the bottom of the page and click "Next".
10. Scroll to the bottom of the page, select all checkboxes, and click "Submit".
11. Wait until you see \<stack-name\> CREATE_COMPLETE.
12. Navigate to tm-devops-trainee-alb and access the public DNS.
