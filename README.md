# FULLSTACK CONTAINERIZATION WITH TERRAFORM

## Introduction
Terraform is a powerful tool to use code to deploy, secure and manage repositories. This project is based on GitHub-repo below:

https://github.com/dhomi/fullstack_conteinerized 

### A scenario:
- As a DevOps specialist
- I would like to use an IaC tool in Windows OS
- In order to manage my complete fullstack container environment from a repo

## How-To
1) Download/Install [Docker Desktop](https://docs.docker.com/desktop/) 
2) Download/Install [NodeJS](https://nodejs.org/en/download/package-manager)
3) Download/Install [Terraform](https://developer.hashicorp.com/terraform/install)
4) Add "terraform.exe" into (Windows) environment variables
5) See for instructions starting the fullstack container environment: 
    - https://github.com/dhomi/fullstack_conteinerized 

## Start with Terraform

1) First set-up Terraform [GitHub provider](https://registry.terraform.io/providers/integrations/github/latest/docs)
2) 

## Design Overview

Terraform will be used to build different repositories located in different cloud platforms. The Terraform code is stored in this repository as a "Repo Manager" to manage the different repositories (see design overview below).

![terraform flow](terraform/img/terraform_repo_flow.jpg)