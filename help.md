ansible-vault encrypt ./group_vars/secrets.yaml
ansible-vault view ./group_vars/secrets.yaml
ansible-vault edit ./group_vars/secrets.yaml

ansible rupl.org -m ping
# ansible rupl.org -m ping -i inventory.yaml

ansible-playbook --ask-vault-pass setup.yaml
ansible-playbook setup.yaml --vault-password-file="~/Desktop/ansible-vault-pass"
# ansible-playbook example-playbook.yaml --limit host1

openssl x509 -noout -text -in cloud1.crt