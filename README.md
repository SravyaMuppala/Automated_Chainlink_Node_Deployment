# Terraform-ansible-chainlink

### 1) Install Terraform
    $ wget https://releases.hashicorp.com/terraform/0.12.26/terraform_0.12.26_linux_amd64.zip
    $ unzip terraform_0.12.26_linux_amd64.zip
    $ sudo mv terraform /usr/local/bin
    
### 2) Install Ansible
     $ sudo apt install ansible
      
### 3) Install python-boto library
     $ sudo apt-get install python-boto
     
### 4) Clone Chainlink_node_deployment
     $ git clone https://github.com/SravyaMuppala/chainlink_node_deployment.git
     $ cd chainlink_node_deployment
     
### 5) Setting Up your AWS Environment
  **Edit main.tf** - 
      Add your AWS access key id and secret key (For security, Don't commit your credentials TO GITHUB),
      vpc_id = "Insert your default vpc id",
      key_name = "name of your key pair"
      
### 6) Run Terraform
        Terraform init
        Terraform apply
      
### 7) Setting Up your Ansible playbook
   **Edit run-playbook.sh** - 
      --private-key= "Add your private key path";
   **Edit hosts** - 
    Add your instance
      
### 8) Run Ansible playbook
     sh run-playbook.sh
      

     
 
 
 
     



      

