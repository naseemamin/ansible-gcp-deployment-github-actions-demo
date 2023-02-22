# Requirements:

install boto3
install ansible
ansible-galaxy collection install amazon.aws

## Steps:
1. Launch an AWS Sandbox environment via learn.acloud.guru/cloud-playground/cloud-sandboxes
2. Retrieve the Access Key ID and Secret Access Key
3. Create RSA keypairs to authenticate SSH into the EC2 instance (ssh-keygen), place them into ~/.ssh/
4. Use "ansible-vault create vault.yaml" to create an ansible vault, remember the password as you'll need this to run the playbook
5. Edit the contents of the vault.yaml (replacing Access Key ID and Secret Access Key with the details from step 2):
access_key: Access Key ID
secret_key: Secret Access Key
region: us-east-1
6. execute runbook using ansible-playbook ec2.yml --ask-vault-pass
- BECOME password can be anything, by default it's blank so you can enter anything
- Vault password is the same one that you set for step 4

ansible-vault edit vault.yaml can be used to edit the vault file