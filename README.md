# Insight Project
## Automated Chainlink Node Deployment

### Table of Contents
   - Introduction
   - Development
   - Engineering Challenges
    
### Introduction

   Decentralized networks require Chainlink nodes to act as middleware to the outside world. For instance, blockchains have no way of securely exchanging information with the      outside world this problem can be solved using the Chainlink node. But most of the Chainlink node deployments are often manual, unpredictable and needs a longer time. 
   
   My project focuses on the one-click deployment of robust Chainlink nodes on AWS.

### Development
   
   To deploy the Chainlink node, you will need the following dependencies:
   
   - Terraform
   - Ansible 
   - Docker
   - awscli
     
   Before deploying the Chainlink node, these are steps to follow to setup environment:
   
   1. git clone https://github.com/SravyaMuppala/postgres.git
   2. git clone https://github.com/SravyaMuppala/Automated_Chainlink_Node_Deployment.git
   3. Setup AWS Environment
      - **Edit main.tf:** Enter your AWS access key id and secret key, vpc_id = "Insert your default vpc id", key_name = "name of your key pair"
   4. Run Terraform
      – Deploys instance on AWS
   5. Setup Ansible Playbook
      - **Edit run-playbook.sh:** --private-key= "Add your private key path";
      - **Edit hosts:** Add your instance
   
 Run Ansible playbook
     - sh run-playbook.sh
 
### Engineering Challenges
 
  - Deployment of Postgres on Docker.
  
  - HTTP 400 - authentication error when deploying Chainlink node
     - Updated configuration of the environment variable ALLOW_Origin = * - By changing it to * instead of specific addresses/URLs it will allow all connections to the API on           CLIENT_NODE_URL
 
      

     
 
 
 
     



      

