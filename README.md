## How to leverage with_subelements and seperate yaml for variables
This script can be used when you are required to read values of array of array i.e. double "for" loop. This playbook contains an example where user wants to execute command on various types of instances/servers.

### Script can referenced for learning
* Ansible roles
* Seperate config file to maintain variable
* Host groups and their children
* Global varibles using all file
* Host specific variables under host_vars

### Attention please
1. Global ansible variable are defined in __group_vars/all__. Please amend appropriately.
2. Host specific ansible variabled can be setup at __host_vars__. Example: host_vars/kafka_2. Please amend approprietly.
3. Host Key Checking is disabled in ansible.cfg at root level
4. Hosts are maintained  in __host__

#### How to execute
ansible-playbook -i hosts master.yml -e "host=int-kafka" -e "@dynatrace_config.yaml"
