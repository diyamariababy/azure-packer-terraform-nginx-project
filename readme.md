#  Immutable Infrastructure with Packer + Terraform on Azure

This project implements an immutable infrastructure model by automating the creation of a custom Ubuntu VM image with Nginx pre-installed using **Packer**, and deploying a Virtual Machine from that image using **Terraform** on Microsoft Azure. This approach ensures consistency, security, and repeatability across cloud environments.

---

## Project Overview

- **Cloud Provider:** Microsoft Azure  
- **Tools Used:** Packer, Terraform, Azure CLI  
- **Base OS:** Ubuntu 18.04 LTS  
- **Key Components:** Custom VM image, Virtual Network, Subnet, Network Security Group, Public IP, Network Interface, Linux VM  

This project demonstrates how to automate VM image creation and deployment for faster and more reliable infrastructure provisioning.

---

## Steps Performed

### 1. Created a Custom Image with Packer  
- Defined a Packer JSON template to build an Ubuntu image with Nginx installed  
- Used Azure ARM builder with service principal authentication  
- Executed `packer build ubuntu-nginx.json` to create a managed image in Azure  
> Screenshot: ![Packer Build](./Screenshots/Packer%20Build.png)
> Screenshot: ![Custom Image Verification in Portal](./Screenshots/Custom%20Image.png)

### 2. Configured Infrastructure with Terraform  
- Defined Azure resources: Resource Group, Virtual Network, Subnet, Network Security Group, Public IP, Network Interface, and Linux VM  
- Configured VM to use the custom image created by Packer  
- Opened ports 22 (SSH) and 80 (HTTP) in the Network Security Group  
- Ran `terraform init`, `terraform plan`, and `terraform apply` to deploy 
> Screenshot: ![Terraform Initialisation](./Screenshots/Terraform%20Initialisation.png)
> Screenshot: ![Terraform Apply](./Screenshots/Terraform%20Apply.png)


### 3. Verified Deployment  
- SSH’ed into the deployed VM  
- Confirmed Nginx was running by visiting the public IP in a browser or using `curl`  
> Screenshot: ![Curl Command](./Screenshots/Curl%20Command.png)
> Screenshot: ![Browser](./Screenshots/Nginx%20Browser.png)

---

##  This Project Showcases My Ability To

- Use **Packer** to automate image creation in Azure  
- Configure **Nginx** automatically during image building  
- Deploy infrastructure using **Terraform** in a modular and repeatable way  
- Handle Azure authentication using **Service Principals** securely  
- Design and configure **networking components** like NSG, Subnet, and Public IP  
- Open necessary ports (e.g., SSH 22, HTTP 80) securely for access  
- Demonstrate **end-to-end cloud provisioning and configuration automation**

---

## What I Learned

- Benefits of immutable infrastructure in cloud environments  
- Integration of Packer and Terraform for automated provisioning  
- Azure resource dependency management with Terraform  
- Securing Azure infrastructure by using NSGs and service principals  
- Practical experience with Azure CLI, Packer, Terraform toolchains  

---
