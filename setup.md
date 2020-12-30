# Setup working directory 

## create folder
mkdir dev
cd dev

# Snowflake Key Setup 

## generate private key 
run the command `openssl genrsa 2048 | openssl pkcs8 -topk8 -inform PEM -out rsa_key.p8`
provide pasphrase when prompted  `Welcome123`
creates file   `rsa_key.p8`


## generate public key
run the command   `openssl rsa -in rsa_key.p8 -pubout -out rsa_key.pub`
provides passphrase  `Welcome123` when prompted

# Connect to Github
`cd ~/.ssh`
run the commands 
- `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
- `sudo chmod 600 ~/.ssh/id_rsa.pub`
- copy file content `~/.ssh/id_rsa.pub`

## add key to github repo
Go to https://github.com/settings/keys and make a new ssh key. You can give it whatever title you want. Paste the key you just copied from id_rsa.pub within the ‘key’ text field and click ‘add ssh key.’ You are now connected to Github and won’t have to sign in every time you want to push to your ec2 instance.

## clone directory 
go to the project (git project)
go to ssh 
copy ssh under the clone and execute below statements in terminal 
 - `cd dev`
 - `git clone git@github.com:Pavan2909/snowflake_dbt.git`

# Linux commands 
print current working directory `pwd`
list files `ls`
print file in terminal `cat file.txt`

