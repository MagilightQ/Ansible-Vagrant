# Ansible web-server projekt

## Cíl
Zapomocí Ansible nakonfigurovat virtuální server(vagrant + virtualbox) Ubuntu 22.04

## Požadavky
- Vagrant
- VirtualBox
- Ansible
- Git

## Ansible config
Projekt využívá vlastní "ansible.cfg", aby automaticky našel správné složky.

## Spuštění
```bash
git clone https://github.com/USERNAME/ansible-vagrant-cv.git
cd ansible-vagrant-cv
vagrant up --provision
```

## Spuštění playbooku
"ansible-playbook playbooks/site.yml --ask-vault-pass"
heslo na vault:"vault"

##HTML
Nginx obsah bude na stránce "http://localhost:8080"


