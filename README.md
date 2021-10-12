HOWTO:

- update ./hosts with valid servers ips
- check playbook with dryrun

`ansible-playbook playbook.yml -u root -i ./hosts --extra-vars "APACHE_PORT=80 --check`

- run playbook 

`ansible-playbook playbook.yml -u root -i ./hosts --extra-vars "APACHE_PORT=80`


useful comands
```bash
ansible-inventory --list -y -i ./hosts

ansible all -m ping -u root -i ./hosts

ansible all -u root -i ./hosts -a "lsb_release -a"
```

`Set authorized key for remote user` doesnt work in --check mode