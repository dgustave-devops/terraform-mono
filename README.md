# terraform-mono
This guide deploys the monolithic-deployment repo through the IaC tool Terraform.

### How to install Terreform on Ubuntu based Linux
1. Ensure that your system is up to date and you have installed the gnupg, software-properties-common, and curl packages installed. You will use these packages to verify HashiCorp's GPG signature and install HashiCorp's Debian package repository.
```bash
sudo apt-get update -y
sudo apt-get install -y gnupg software-properties-common
```
2. Downloading and saving the hashicorp PGP keys:
```bash
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
```
3. Add entry to the system's list of package providers:
```bash
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
```
4. Update package list and install terraform.
```bash
sudo apt update -y
sudo apt install terraform -y
```
5. Test to verify terraform was correctly installed.
```bash
terraform -version
```

### Declare infrastructure
1. Create directory in home
```bash
cd ~
mkdir 
```
