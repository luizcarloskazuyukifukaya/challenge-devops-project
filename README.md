# sample-devops-pipeline (created by Kazuyuki Fukaya)
This is a sample project for a DevOps pipeline

## Challenge Statement
Company A is a Tech company that develops and operates many web applications. The
company has decided to configure its applications using Kubernetes.
Since Company A had not implemented Kubernetes before, the company decided to verify
what a DevOps pipeline using Kubernetes would look like with a simple configuration.
## Details
As a DevOps engineer, you have decided to develop the following as the minimum
configuration.
### Application
● Consist of a web application framework (e.g. Node.js, Flask, etc.) and a DB (e.g.
RDBMS, DocumentDB, etc.)
● Those configurations are defined using Helm Chart
● “Hello world” page that shows the framework is properly communicating with the DB
### Infrastructure
● One node in the Kubernetes cluster
● Use a cloud Kubernetes provider including AWS, GCP, Azure or others
● The configuration is defined using Terraform
### CI/CD
● Application, HelmChart, and Terraform codes are managed on GitHub and
automatically deployed after merging into the main branch

