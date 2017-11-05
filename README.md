# Ghost Blog with Docker Playbook

Setup HTTPS Ghost Blog using Docker container and nginx

## Usage
Change `group_vars/all.yml` as you wish. `letsencrypt_email.yml` should contain
variable named `letsencrypt_email`. Please encrypt it using Ansible Vault.

```
ansible-galaxy install -r requirements.yml
ansible-playbook -i production site.yml --ask-vault-pass
```

## Author
Ricky Kurniawan

## Known Issue
* In certain Docker version, docker volume creation will fail if there is no docker volume yet in host.
