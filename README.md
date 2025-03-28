# devops-practical-test
Solutions to the practical test for devops job evaluation

# CI/CD Pipeline Tasks

## Task 1: Setup a Simple CI/CD Pipeline

### Steps to Complete

1. **Used a GitHub Actions Template**  
   - Picked a basic CI/CD workflow for Node.js and modified it for my needs.

2. **Cloned the Repository**  
   - Ran `git clone` to get the repo locally.

3. **Initialized a Node.js Project**  
   - Inside the `task1` folder, ran `npm init -y` to create a basic `package.json`.

4. **Updated `package.json` for Testing**  
   - Searched online for a simple way to make `npm test` work without real tests.
   - Added a basic test script:
     "scripts": {
       "test": "echo \"Tests passed!\""
     }
     ```

5. **Ran the Pipeline**  
   - Committed and pushed changes to GitHub.
   - The GitHub Actions pipeline installed dependencies and executed test steps.

6. **Checked the Results**  
   - Verified in GitHub Actions that everything ran successfully.
   - Saw the message **"Ready for Deployment"** confirming success.

## Task 2: Terraform Basics

### Steps to Complete

1. **Started with an Example `main.tf`**  
   - Followed the Terraform guide from [HashiCorp's tutorial](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build).

2. **Modified `main.tf` to Use Variables**  
   - Replaced hardcoded values with variables for `region` and `AMI ID`.

3. **Added a `variables.tf` File**  
   - Defined `aws_region` and `ami_id` as Terraform variables.

4. **Created `terraform.tfvars`**  
   - Added default values to configure the AWS region and AMI ID.

5. **Initialized Terraform**  
   - Ran `terraform init` to set up the working directory.

6. **Could Not Fully Test Deployment**  
   - Since I don't have an AWS account yet, I wasn't able to apply the Terraform configuration.


### Challenges Faced

- **Large File Size Issue**: Encountered a problem when pushing the repo because Terraform downloaded provider binaries inside `.terraform/`, which contained files larger than 100MB.
- **GitHub Rejecting the Push**: GitHub blocks files exceeding 100MB, causing push failures.
- **Solution Implemented**: Removed `.terraform/` from tracking using `.gitignore` and cleared it from the Git history using `git filter-repo`.
- **Time Consumption**: Debugging and fixing this issue took significant time.

## Task 3: Kubernetes Deployment

### Objective:
- Write a Kubernetes manifest file to deploy a simple app.

### Instructions:
1. **Generated Deployment YAML using Command**  
   ```sh
   kubectl create deployment nginx-deployment --image=nginx:latest --replicas=2 --dry-run=client -o yaml > deployment.yaml
   ```
   - This created a `deployment.yaml` file with an `nginx` deployment having 2 replicas.

2. **Created Service YAML Manually**  
   - Wrote a `service.yaml` file manually to expose the deployment using ClusterIP.


## Task 4: Docker and Kubernetes Files fixes
Steps to Complete

Identified and Fixed Errors in Dockerfile & Kubernetes YAML

Corrected the base image name, indentation, and syntax issues.

Explanation for This Task is in the Folder

Detailed explanation of the fixes is available in the respective folder.
