- ### Installing Ansible
    On Ubuntu / debian:
    - sudo apt update 
    - sudo apt install software-properties-common 
    - sudo add-apt-repository --yes --update ppa:ansible/ansible 
    - sudo apt install ansible

- ### Setting up SSH key-based authentication
    - Generate SSH Key
      -     ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    
      - Copy the Public Key to Host Machines
        
        -      ssh-copy-id your_username@server1 
        -      ssh-copy-id your_username@server2
        -      ssh-copy-id your_username@server3
    
    - Verify SSH Key authentication:
        - ssh your_username@server1
        - ssh your_username@server2
        - ssh your_username@server3

- ### Update Ansible Inventory 
  - Update the hosts file inside inventory directory with your corresponding IP addresses.

- ### Running the Playbook
  -     ansible-playbook -i inventory/hosts.ini playbook.yml --ask-become-pass
  - Use -vvv  for verbose output to get more details about what Ansible is doing.
