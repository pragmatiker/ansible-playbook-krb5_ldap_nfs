## Deploy droplets, user root to create initial non root user account
    ansible-playbook --vault-password-file vaultpw  playbook.yaml -uroot

## Encrypt your API Token
   ansible-vault encrypt_string --vault-password-file vaultpw --stdin-name 'DO_API_TOKEN'
  
## Tear down your Lab
    ansible-playbook --vault-password-file vaultpw  playbook.yaml -e 'destroy_droplets=True'
