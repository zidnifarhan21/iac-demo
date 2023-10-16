# Cloudformation Demo


## Add your files

- [ ] [Create](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#create-a-file) or [upload](https://docs.gitlab.com/ee/user/project/repository/web_editor.html#upload-a-file) files
- [ ] [Add files using the command line](https://docs.gitlab.com/ee/gitlab-basics/add-file.html#add-a-file-using-the-command-line) or push an existing Git repository with the following command:

```
cd existing_repo
git remote add origin https://gitlab.com/zidni.farhan/cloudformation-demo.git
git branch -M main
git push -uf origin main
```

## Integrate with your tools

- [ ] [Set up project integrations](https://gitlab.com/zidni.farhan/cloudformation-demo/-/settings/integrations)

## Collaborate with your team

- [ ] [Invite team members and collaborators](https://docs.gitlab.com/ee/user/project/members/)
- [ ] [Create a new merge request](https://docs.gitlab.com/ee/user/project/merge_requests/creating_merge_requests.html)
- [ ] [Automatically close issues from merge requests](https://docs.gitlab.com/ee/user/project/issues/managing_issues.html#closing-issues-automatically)
- [ ] [Enable merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/approvals/)
- [ ] [Set auto-merge](https://docs.gitlab.com/ee/user/project/merge_requests/merge_when_pipeline_succeeds.html)

## Test and Deploy

Use the built-in continuous integration in GitLab.

- [ ] [Get started with GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html)
- [ ] [Analyze your code for known vulnerabilities with Static Application Security Testing(SAST)](https://docs.gitlab.com/ee/user/application_security/sast/)
- [ ] [Deploy to Kubernetes, Amazon EC2, or Amazon ECS using Auto Deploy](https://docs.gitlab.com/ee/topics/autodevops/requirements.html)
- [ ] [Use pull-based deployments for improved Kubernetes management](https://docs.gitlab.com/ee/user/clusters/agent/)
- [ ] [Set up protected environments](https://docs.gitlab.com/ee/ci/environments/protected_environments.html)

***

## Description

This CloudFormation template creates an Autoscaling group of EC2 instances, a load balancer, an RDS database, an S3 bucket, and a VPC. The Autoscaling group is configured to scale up or down based on CPU utilization. The load balancer distributes traffic across the Autoscaling group. The RDS database is used to store application data. The S3 bucket is used to store static files and other resources. The VPC provides a private network for the application components.

## Requirements

An AWS account
The AWS CLI or AWS Console
Usage:

To deploy the stack, run the following command:
```
aws cloudformation deploy --template-file template.yaml --stack-name my-stack
```
This will create a new stack with the name my-stack. The stack will contain all of the resources defined in the CloudFormation template.

To view the status of the stack, run the following command:

```
aws cloudformation describe-stacks --stack-name my-stack
```
Once the stack is deployed, you can access the application through the load balancer. The DNS name of the load balancer will be displayed in the output of the describe-stacks command.

Outputs:

The stack outputs the following information:

LoadBalancerDNSName: The DNS name of the load balancer
RDSInstanceEndpoint: The endpoint of the RDS database

Troubleshooting:

If you encounter any problems deploying the stack, you can view the stack events to get more information. To view the stack events, run the following command:

```
aws cloudformation describe-stack-events --stack-name my-stack
```
The stack events will show you the status of each resource in the stack and any errors that occurred.

## Contributing

If you would like to contribute to this project, please open a pull request. Your suggestions and feedback are welcome.