# 3.14 Package Vulnerability Scan


### Instructions:

1. Create a new Node.js application using the Express framework.
2. Set up automatic testing for the application using a testing framework such as Jest or Mocha.
3. Create new branch on your existing repository.
4. Set up a CI/CD pipeline using a tool such as Github Action, Jenkins, Travis CI, or CircleCI.
5. Configure the pipeline to automatically build and test the code whenever changes are pushed to the code repository.
6. Deploy the application to a serverless platform such as AWS Lambda or Google Cloud Functions.
7. Store some information using Secret Management on AWS, then get the information as part of the pipeline.
8. Add Package Vulnerability Scan on your CICD
9. Configure the pipeline to automatically deploy the code to the serverless platform whenever changes are pushed to the code repository and all tests pass.
10. Write a documentation explaining the steps you have done, including the tools and services used.

#### Deliverables:

- The Node.js application with automatic testing set up
- Code repository with the CI/CD pipeline configured
- Documentation explaining the steps taken to set up the pipeline.

## Assignment 3.14 submission

This repo runs a CI/CD pipeline in GitHub Action to deploy a Lambda function in AWS.  It also echo's out the variable stored in AWS Secrets Manager parameter store.  The output of the node.js application also contains the secret message.

#### Steps taken:
1. Create a repo and configure the AWS credentials in GitHub secrets and variables store
2. git clone the repo into local
3. create a github workflow yml file "secrets.yml" to define the workflow which includes:
- Pre-deploy - echoing a message on the automated job displaying the user 
- installing the dependencies required to perform the deployment
- perform an automated unit-testing to check for errors
- performing a vulnerability scan

  ![Screenshot 2023-09-03 at 4 06 50 PM](https://github.com/vincent8055/3.14_package_scan/assets/127754761/9f914def-6dda-4a7e-a333-d549d1fccf8c)

- displaying the secrets from AWS Secrets Parameter Store
- deploying the Lambda function into AWS
4. Install node dependencies such as node, serverless, serveless-offline, jest
5. Add in a index.test.js to test the application
6. Add in a function to extract the secret in AWS Secrets Manager parameter store
7. Include a function to display the secret in the Lambda function when invoked.
