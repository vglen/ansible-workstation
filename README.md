# ansible-workstation

Thanks to https://opensource.com/article/18/3/manage-workstation-ansible for all the help!

This is my horrific/shoddy ansible setup to get my workstation setup, but it does what I need, good enough for now. This allows me to torch my workstation and build it up again without much worry.

First install ansible:
```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```
Force apply:
```
sudo ansible-pull --extra-vars "user=<USERNAME>" --verbose -U https://github.com/bobhenkel/ansible-workstation.git
```
Otherwise the cronjob will run this at whatever interval is set for the cronjob to run.

Run Manually:
```
ansible-playbook local.yml --check --extra-vars "user=<USERNAME>"
```


*test
