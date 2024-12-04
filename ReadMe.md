KEY PERMISSION ERROR 
fixing error : git@github.com Permission denied (public key)
git couldn't authenticate the ssh key with github 
STEP.1
Check if you have an existing key = (ls -al ~/.ssh) if not run ssh-keygen -t ed25519 -C "your email"
STEP .2
start the SSH Agent = eval "$(ssh-agent -s)"
STEP.3
add ssh private key to the agent = ssh-add ~/.ssh/id_rsa , to add new key ssh-add ~/.ssh/id_ed25519
STEP.4
display and copy key = cat ~/.ssh/id_ed25519.pub
STEP.5 
login github -settings paste it add write Permission 
STEP.6
TEST run = ssh -T git@github.com