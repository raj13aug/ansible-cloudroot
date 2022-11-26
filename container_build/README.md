Step 1: Configuring Docker Registry username and password to docker-credential.yaml

Step 2: Create an Ansible Vault file to keep the Docker Registry credentials.
        ansible-vault create docker-credential.yaml

Step 3: Building container images using Ansible
        ansible-playbook container-build.yaml -e 'NODES=localhost' --ask-vault-password

####################################################
Git Command:

This will remove all uncommitted changes and then pull:

git reset --hard HEAD
git pull        
         
To delete all the images,

docker rmi -f $(docker images -aq)

######################################################
