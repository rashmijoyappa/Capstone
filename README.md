Capstone Hello world Project

In this project we will apply the skills and knowledge which were developed throughout the Cloud DevOps Nanodegree program. These include:

1) Working in AWS
2) Using Jenkins to implement Continuous Integration and Continuous Deployment
3) Building pipelines
4) Working with CloudFormation to deploy clusters
5) Building Kubernetes clusters
6) Building Docker containers in pipelines

About Project:

I created a CI/CD pipeline for a basic website that deploys to a cluster in AWS EKS which is Blue/Green Deployment.

Project Requirement: To be able to use this CI/CD pipeline you will need to install:

•	Jenkins 
•	Blue Ocean Plugin in Jenkins 
•	Pipeline-AWS Plugin in Jenkins 
•	Docker 
•	Pip 
•	AWS Cli 
•	Eksctl 
•	Kubectl

The files included are:

/Result-Screenshots : Screenshot the result of deploy.
/PipelineKubernetes : CloudFormation Script of Cluster Pipeline file
Jenkinsfile : Jenkinsfile for Creating Pipeline
Dockerfile : Dockerfile for building the image
green-controller.json : Create a replication controller green pod
green-service.json : Create the green service
blue-controller.json : Create a replication controller blue pod
blue-service.json : Create the blue service
index.html : Web site Index file.

Run the project:
Please follow to steps of screenshot in Images-of-result-deploy folder.
