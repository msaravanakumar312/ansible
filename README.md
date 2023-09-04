# ansible
.............
Ansible is a configure management tool which works both push and pull machanisims.

**''''''''''''''**
#Incentory file
Inventory is nothing but the list of machine ip and dns names that you want ansible to manage.
....

Ansible by defaukt install's 2.9 as by defaut on AMI's will gt pythin2.
Always go with the latest version, which can be installed from tools/ansible/install.sh

'all' is a grup which included all entries in INVETORY files.
..........

## Automated approch : this uses playbook

....
Playbook are written using a laungauge called YAML
YAML is just markup laungauge; markup laungauge is nothing presentation laungauge.

...........
## What is playbook?

*Playbook: A play book is a list of plays (and that's why it always start with -)
Play:  A play is a list of task.
Task : A task is nothing but that we wish to perform 

..............

# Varibles should be passed to ansible bu using the flag -e
.........
e.g  ansible -i INVENTORY all -e ansible_user=usename -e ansible_password=password
$ansible -i inv all -e ansible_user=centos -e ansible_password=DevOps321 -m shell -a uptime

..................
# Note: If you would just like to print a varriable, then enclose the varriable {{varname}} and there is no    single quots concepts.
# and if the varriable is present in between the string of words, you don't have to enclose them in quotes.

# No two task of a play can have the same name.

.................

# When to use ansible Push and Pull?

..........
1> when your infrastructure is static, then we will host an ANSIBLE server and will target configuration management on all the nodes from your ansible server.

2>when your infrastructure is not static, which mean on cloud we often scale out and down the infra, in this case maintaining the inventory is quite challenging and to avoid this , what we do is, as a part of the BOOTSTRAPPING, we will let the ansible-Pull command to run.

Points to be notes when using Pull:

* Ensure your nodes running ansible has ansible installed.
* Pull only work from GIT.

.........

# How to use PULL?
.......


............

