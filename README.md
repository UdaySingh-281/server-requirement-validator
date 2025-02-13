# Server Requirement Validator

This Ansible playbook ensures that all servers in your infrastructure meet the required system specifications before deployment. It validates memory and CPU requirements for different server groups (web servers, app servers, and database servers) and provides real-time feedback on any configuration mismatches.

## Features
- Checks system memory and CPU against predefined minimums.
- Uses **assert** to enforce compliance.
- Provides failure notifications and records validation status.
- Supports different server roles with dynamic requirement handling.

## Repository Structure

server-requirement-validator/ 
* │── 📄 playbook.yml # Main Ansible playbook
* │── 📄 vars.yml # Defines system requirements for each server group
* │── 📄 inventory.ini


## Prerequisites
- Ansible installed on the control node (`sudo apt install ansible -y`).
- SSH access to all target hosts.
- Properly configured Ansible inventory file.

## Setup & Usage
1. **Clone the repository**  
   * git clone https://github.com/your-username/ansible-env-validator.git
   * cd ansible-env-validator

## Run the playbook
* ansible-playbook -i inventory.ini playbook.yml
