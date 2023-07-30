# Ansible

## Few commands used:
    $cd .ssh

    $vim ansible_key
    
         and paste the private key there copied by opening it in vs code

    $sudo ssh -i ~/.ssh/ansible_key ubuntu@I.P      // replace I.P with server I.P

    $exit //this was ssh :entering from one server to another

    $cd ..

    $mkdir ansible

    $vim hosts

           [servers]
           
           server1 ansible_host=3.7.68.152   //replace with ur server I.P
           
           server2 ansible_host=3.7.69.180    //replace with ur server I.P
           
           server3 ansible_host=13.127.145.213   //replace with ur server I.P

           [all:vars]
           
           ansible_python_interpreter= /usr/bin/python3
    
    Save and exit
      
    $pwd
    
    $ansible-inventory --list -y -i  /home/ubuntu/ansible

    $/.ssh/ansible-key
    
    $chmod 700 ~/.ssh

    $chmod 600 ~/.ssh/ansible-key

    $ansible all -m ping -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

    $ansible all -a "free -h" -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

    $ansible servers -a "uptime" -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key

