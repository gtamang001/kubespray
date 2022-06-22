## Setup your cloud architecture 
devk8slb     dns 
devmaster1  
devmaster2
devmaster3 
devworker1
devworker2
devworker3
devworker4

## SSH into control plane i.e devk8slb 
setup python pip 
Create kubernetes user as k8suser
create ssh key as k8suser

ssh-keygen 

copy ssh keys to all host created
```bash
ssh-copy-id -i ~/.ssh/other_key.pub k8s@<remote-host>
```
## Begin cluster create now 
1. Install Dependencies using pip 
```
sudo pip3 install -r requirement.txt
```
2. Copy inventory sample as inventory/mycluster 
```bash
cp -rfp inventory/sample inventory/mycluster
```
3. Update Ansible inventory file with inventory builder 
4. Update Inventory/mycluster/group_vars/all/all.yml file with created architecture vm details above 
5. Add cluster specific changes to various config files 
- contrib/inventory_build/inventory.py 
- 