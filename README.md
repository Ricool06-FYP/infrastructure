# infrastructure
## Ansible project to deploy infrastructure dependencies like docker-ce to the system host

### How to use:
1. Make sure the VPS is up, and set up with your root ssh key.
1. Run `export ANSIBLE_VAULT_PASSWORD_FILE=/path/to/vault/password/file`
>* If you don't remember the vault password, then you messed up.
1. Add both the main_ansible_user and root SSH key to ssh-agent.
1. If the VPS has just been reinstalled, run `ansible-playbook secure-ssh.yml -i vps.hosts` to make sure SSH configuration is secure, and the `main_ansible_user` has been created.
1. Run `ansible-playbook docker-ce.yml -i vps.hosts` to install the docker server.
