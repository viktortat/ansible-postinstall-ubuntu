
Предустановка полезностей на голую Ubuntu

```sh
# 1. Install Ansible: 
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install ansible
# 2. Add entry for localhost to your Ansible hosts file:

cat <<EOT >> /etc/ansible/hosts
[localhost] 
127.0.0.1
EOT

# 3. Become root:
sudo -i

## Usage Run the following command to pull and run the playbook: 
sudo ansible-pull -U https://github.com/viktortat/ansible-postinstall-ubuntu.git

# install in wsl2
sudo ansible-playbook local.yml

# Ansible Facts List 
ansible localhost -m setup
```