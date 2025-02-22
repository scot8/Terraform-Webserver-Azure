# Terraform Azure Web Server Deployment

## 🚀 Project Overview
This project automates the deployment of an **Ubuntu 22.04 LTS virtual machine** on **Microsoft Azure** using Terraform. The VM is configured with **Apache Web Server** and is accessible via HTTP and SSH.

---

## 📂 Project Structure
```
📦 cst8918-w24-a06-scot0568
 ├── 📄 main.tf                 # Terraform configuration file
 ├── 📄 variables.tf            # Terraform variables
 ├── 📄 outputs.tf              # Terraform output values
 ├── 📄 init.sh                 # Cloud-init script to install Apache
 ├── 📄 README.md               # Project documentation
 ├── 📄 .gitignore              # Git ignored files
```

---

## 🛠️ **Technologies Used**
- **Terraform** (Infrastructure as Code)
- **Azure CLI**
- **Ubuntu 22.04 LTS**
- **Apache Web Server**
- **Cloud-Init** (for server configuration)

---

## 🌟 **Features**
✅ Deploys an **Ubuntu VM** on Azure  
✅ Configures **Apache Web Server**  
✅ Automates **infrastructure setup** using Terraform  
✅ Allows **SSH access** for remote management  
✅ Uses **Cloud-Init** for software installation  

---

## 📌 **Pre-requisites**
Make sure you have the following installed:
- [Terraform](https://developer.hashicorp.com/terraform/downloads)
- [Azure CLI](https://learn.microsoft.com/en-us/cli/azure/install-azure-cli)
- An **Azure account** with access to create resources
- An **SSH key pair** (`~/.ssh/id_rsa.pub`)

---

## ⚙️ **Setup Instructions**
### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/yourusername/cst8918-w24-a06-scot0568.git
cd cst8918-w24-a06-scot0568
```

### 2️⃣ **Initialize Terraform**
```bash
terraform init
```

### 3️⃣ **Deploy the Infrastructure**
```bash
terraform apply
```
When prompted for `var.labelPrefix`, enter your **college username**.

### 4️⃣ **Verify Deployment**
- Open a browser and visit:  
  ```
  http://<public-ip>
  ```
- SSH into the VM:
  ```bash
  ssh azureadmin@<public-ip>
  ```

---

## 📤 **Outputs**
After deployment, Terraform will display:
```bash
Outputs:
nic_name            = "<your-NIC-name>"
public_ip           = "<your-public-ip>"
resource_group_name = "<your-resource-group>"
vm_name             = "<your-vm-name>"
```

---

## 🗑️ **Destroying the Infrastructure**
To remove all resources:
```bash
terraform destroy
```
