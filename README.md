##Packages install using ansible-pull##

These Ansible playbooks will Install all playbook which you update in packages vars file.

Here we are use ansible-pull to get clone of our source code which help to deploy update packages of  variable file in all nodes.

In ansible-pull.yml 

We can set a cron job which help us to clone git code in server also we can have to provide git repo url to get clone from that repo and we have to set provide a directory path where the code is clone using ansible-pull

**schedule**: time to execute the playbook

**cron_user**: User to run ansible-pull as from cron

**workdir**: where repository will be cloned

**repo_url**: repository to clone

After providing all detail you can update your playbookfile name in **ansible-pull.j2** template file so while cron execute it get properfile to install all packages which update in vars file.

run playbook using **ansible-playbooks ansible-pull.yml**


