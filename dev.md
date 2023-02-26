```
ansible-playbook facts/ansible_var.yml
ansible-playbook local.yml
```
```sh
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock-frontend
sudo rm /var/lib/dpkg/lock

sudo apt-get update && sudo apt-get upgrade -y 
sudo apt-get install ansible -y

sudo -i

cat <<EOT >> /etc/ansible/hosts
[localhost]
127.0.0.1
EOT

ansible-pull -U https://gitlab.com/viktortat/playbook-postinstall-ubuntu.git
```


