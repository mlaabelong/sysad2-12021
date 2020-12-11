## Ansible Configuration

_Reminder:_ Add or Install first the ansible to your PC.

For alpine:

>> `$ apk add ansible`

__How to create ansible configuration?__

__Step 1:__ Create a directory.

>>`$ mkdir <name of directory>`

>>`$ cd <name of directory>`

__Step 2:__ Create your own ansible.cfg file.

>>`$ vi ansible.cfg`

Insert
```Linux Alpine
[defaults]

inventory = ./inventory

remote_user = <server name of the other device>`
```

_By default you can check the content of ansible.cfg file_  `etc/ansible/ansibel.cfg`

See [ansible-configuration](https://docs.ansible.com/ansible/latest/cli/ansible-config.html#ansible-config) for more information.

## Ansible Inventory
__How to create ansible inventory?__

__Step 1:__ Create an inventory file.

>>`$ vi inventory`

Insert

>>`[device name]`

>>`IP Address of remote_user`

or simply put the IP address

>>`IP Address of remote_user` 

See [How to build your Inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html#intro-inventory) for more information.

## Ansible Ad-hoc Commands

__How to create ad-hoc ansible command with setup and shell module?__

ad-hoc commands look like this:

`$ ansible [pattern] -m ping -a "[module options]"`

__Step 1:__ Use `ls` command if you have the two files which are  the _ansible.cfg_ and _inventory_.

__Step 2:__ Try to ping the remote_user using this command `ansible -m ping <remote_user name>`.

The output should be like this:

![PING](https://user-images.githubusercontent.com/75326926/101939724-59508000-3c20-11eb-80d4-135c2c6627db.PNG)

__Step 3:__ Try to run a command in ubuntu. Run via shell module.

Example:

>> `$ ansible ubuntu -m shell -a "id"

![ID](https://user-images.githubusercontent.com/75326926/101940576-ac770280-3c21-11eb-8713-e077d5495e8c.PNG)



For more information visit the following:

   [Ansible Configuration](https://tip.instructure.com/courses/14414/pages/2-dot-2-ansible-configuration?module_item_id=810770)

   [Ansible Inventory](https://docs.ansible.com/ansible/latest/user_guide/basic_concepts.html)

   [Ad-hoc Commands](https://docs.ansible.com/ansible/latest/user_guide/intro_adhoc.html)
