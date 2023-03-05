Ansible

We will use Ansible playbook to set user in two raspberry pi running ubuntu.

Steps

Install ubuntu server in two raspberry pi and get the ip’s

Ubuntu server 32 bit
192.168.xxx.xxx

Ubuntu Desktop 64 bit
192.168.xxx.xxx

Install Ansible in local system
python3 -m pip install --user ansible





To get started, access your home folder and create a new directory to hold your Ansible files:
	mkdir /usr/local/etc/ansible

Move to that directory and open a new inventory file using your text editor of choice. Here, we’ll use nano:
Sudo nano inventory

A list of your nodes, with one server per line, is enough for setting up a functional inventory file. Hostnames and IP addresses are interchangeable:

/usr/local/etc/ansible
203.0.113.111
203.0.113.112
203.0.113.113
server_hostname

Once you have an inventory file set up, you can use the ansible-inventory command to validate and obtain information about your Ansible inventory:
	ansible-inventory -i inventory --list

Note: To automate ssh login in Mac run below cmd-
brew install hudochenkov/sshpass/sshpass

Create Rasplaybook.yml

Execute using below cmd-
ansible-playbook -i /usr/local/etc/ansible Rasplaybook.yml -u tanuser -kK