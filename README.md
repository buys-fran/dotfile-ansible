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

 Not sure about these
 * Move hosts file for reference `sudo mv /etc/ansible/hosts /etc/ansible/hosts.orig`
 * Make a new hosts file `sudo touch /etc/ansible/hosts`
 * [MANUAL STEP]
  - Add the following to hosts:
  ```
  [local]
  127.0.0.1
  ```

### Ansible playboo
 * Add playbook.yml `touch playbook.yml`
 * Run ansiable playbook `ansible-playbook --connection=local --inventory 127.0.0.1, playbook.yml`
