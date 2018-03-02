# vault

download vault from the below link
https://www.vaultproject.io/downloads.html

set an environment variable so the Vault CLI knows the address of the Vault server
export VAULT_ADDR='https://services'

To authenticate with Vault, use your user ID and password
vault auth -method=userpass -path=ping username=<USER>

Some Windows users have reported being unable to enter their password at the prompt using the command above, alternate command
echo 'Password : ';read -s pw; vault auth -method=userpass -path=ping username=<username> password="$pw";unset pw
 
ssh-keygen 
vault write -field signed_key ssh/sign/username public_key=@.ssh/id_rsa.pub > $HOME/.ssh/id_rsa-cert.pub  

Creating/Updating your SSH config file
ssh jenkins-master
