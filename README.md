# Collection of AAP demos for managing OpenShift 

## Requirements 
    ansible-core >=2.14 
    oc >= 4.14
## setup 
1. Copy ansible.cfg.template and name it ansible.cfg.  Get the token from here: https://console.redhat.com/ansible/automation-hub/token

2. Copy extra_vars.yml.template and name it extra_vars.yml. 
Fill out the required information in the file.  You will 
need the OCP API endpoint, and a cluster-admin username 
and password 

3. Install the required ansible collections.  This assumes you have a functioning ansible.cfg setup to access the Automation Hub.
From this repository's root directory run `ansible-galaxy collection install -r collections/requirements.yml`

4. Install the required python libraries `pip3 install -r requirements.txt`

5. Run the playbook `ansible-playbook -e @extra_vars.yml upgrade_ocp_416-417.yml` 

