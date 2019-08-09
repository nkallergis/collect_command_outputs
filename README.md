# Collect command outputs (IOS, IOS-XE, NXOS)
Collect and parse command outputs from Cisco network devices

## Usage tips
- All configurable variables are stored in **group_vars/all.yml**. They can either be changed in-file or temporarily overriden with **--extra-vars**.
- Hosts are to be declared as per [Ansible documentation](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html).
- The list of commands is by default under **commands.txt**.
- Parsing of raw command output is performed using **ntc_show_command** module. Therefore, dependencies include **ntc-ansible, ntc-templates** among others.
- Raw & parsed files are by default exported in **outputs**.
- Parsed files can be exported in CSV, YAML & JSON format. Configure **parse_into** variable accordingly (lowercase).
- If **clear_previous** variable is set to True (False by default), all previously collected outputs will be erased prior to collecting new ones.
