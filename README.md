# tm-test-task

## Deployment:
1. Clone this repository using ```git clone https://github.com/olehratinskiy/tm-test-task.git```
2. Log in to AWS Management Console and navigate to CloudFormation.
3. Select "Create stack" "With new resources".
4. In the block "Specify template" choose "Upload a template file".
5. Upload "task-template.yaml" from dir where you cloned this repo and click "Next" at the bottom of the page.
6. In the block "Provide a stack name" input the name for deploying the stack and click "Next" at the bottom of the page.
7. Scroll to the bottom of the page and click "Next".
8. Scroll to the bottom of the page, select "I acknowledge that AWS CloudFormation might create IAM resources with custom names." and click "Submit".
9. Wait until you see <stack-name> CREATE_COMPLETE.
10. Navigate to tm-devops-trainee-alb and access the public DNS.