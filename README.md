# Ansible

## Few commands used:
    $pwd
    
    $ansible-inventory --list -y -i  /home/ubuntu/ansible

    $/.ssh/ansible-key
    
    $chmod 700 ~/.ssh

    $chmod 600 ~/.ssh/ansible-key

    $ansible all -m ping -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

    $ansible all -a "free -h" -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

    $ansible servers -a "uptime" -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

