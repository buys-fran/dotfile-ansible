# dotfile-ansible

## Steps after fresh install

### Updates
 * Update ubuntu `sudo apt-get update`.
 * Then upgrade OS `sudo apt-get upgrade -y`.

### Directories
 * Make a .dotfiles directory `cd ~ && mkdir .dotfiles`

### Ansible
 * Add required repository `sudo apt-add-repository ppa:ansible/ansible`.
 * Update OS again `sudo apt-get update`.
 * Install ansible `sudo apt-get install -y ansible`.
 * Ansible needs a Python interpreter `sudo apt-get install python -y`

### Ansible playboo
 * Clone dotfiles.
 * Run ansiable playbook `ansible-playbook --connection=local --inventory 127.0.0.1, playbook.yml`

### AWS Ports
 * Add custom UDP incoming ports 60000 - 61000 for mosh
 * Ensure security group is assigned to VPS


## Notes from for client machine

### SSH/MOSH
 * Mosh must be installed on client.
 * Connecting: `mosh --ssh="ssh -i 'ubuntu-salad.pem'" ubuntu@aws-domain-name.com
