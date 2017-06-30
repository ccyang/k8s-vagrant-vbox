# kubernetes-vagrant-ansible
Install Kubernetes on Vagrant using Ansible.

## Requirements

- Vagrant
- Virtualbox
- Ansible

## Steps

First, create the machines.

```
vagrant up
```

Then, provision the machines.

```
ansible-playbook /vagrant/playbook.yml -i /vagrant/inventory -e @/vagrant/vars.yml
```
