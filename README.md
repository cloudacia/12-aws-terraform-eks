# AWS EKS Cluster

This project aims to deploy a Kubernetes cluster using AWS EKS service.

**Built with**

Terraform manages AWS infrastructure deploymenet.
Ansible manages Wordpress deploy on an EC2 instance

**Requirements**

1. AWS account
2. IAM user with admin privileges
3. Access and secret keys
4. AWS CLI
5. Terraform installed

**AWS resources created**

* 1 x VPC
* 3 x Private subnets
* 3 x Public subnets
* 1 x Internet Gateway
* 3 x EC2
* 7 x Security Groups
* 1 EKS cluster

**Getting started**

Clone the repository locally in your system:

`git clone`

Deploy the code in your AWS account with Terraform

`cd directory`

`terraform init`

`terraform validate`

`terraform plan`

`terraform apply`

`aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)`

`terraform destroy`

**Folder structure options and naming conventions for software projects**
```
.
|-- main.tf                 # AWS provider's configuration
|-- eks-cluster.tf          # EKS cluster configuration
|-- kubernetes.tf           # Kubernetes provider
|-- computing_ec2.tf        # EC2 instances setting
|-- security.tf             # Security groups
|-- versions.tf             # Versions of the modules in use
|-- variables.tf            # Variables
|-- output.tf               # Output values
|-- vpc.tf                  # Networking configuration
|-- diagram01.jpeg          # AWS network layout
|-- LICENSE.txt
|-- README.md
```

**Architecture**

![Screenshot](diagram01.jpeg)

**Contributing**

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated.

If you have a suggestion to improve this, please fork the repo and create a pull request. You can also open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!

**License**

It is distributed under the MIT License. See LICENSE.txt for more information.

**Contact**

Name: Eugenio Duarte

Email: eduarte@cloudacia.com
