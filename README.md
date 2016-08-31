[![Build Status](https://travis-ci.org/terencewestphal/ansible-role-template.svg?branch=master)](https://travis-ci.org/terencewestphal/ansible-role-template)

Ansible Role: template
======================

A base template for Ansible Roles that can be imported on Ansible Galaxy. 

**Note:** The primary use case for this codebase is "Ansible Role Development". 
See the Development section below for more info.

Requirements
------------

- Python 2.7
- Ansible 2.x

Installation
------------

Installing roles from Ansible Galaxy:

    $ ansible-galaxy install {username}.{rolename}

Dependencies
------------

Install all dependencies needed for this role.

    $ ansible-galaxy install -r requirements.yml

Required dependencies: 
- none

Role Variables
--------------

|parameter  |required   |default    |choices    |comments               |
|---        |---	    |---	    |---	    |---                    |
|rolename   |yes        |   	    |   	    |ansible-role-template  |  

Example Playbook
----------------

    - hosts: localhost
      remote_user: root
      roles:
      - "{{ rolename }}"

Testing
-------

Testing on your local machine

    $ ansible-playbook roles/{rolename}/tests/test.yml --extra-vars "rolename=roles/{rolename}" --syntax-check
    
Testing with Travis CI

    $ ansible-playbook tests/test.yml -i tests/inventory --extra-vars "rolename=ansible-role-{rolename}" --syntax-check

Development
-----------
Clone this repository into your ansible-playbook environment.  
    
    $ git clone https://github.com/terencewestphal/ansible-role-template.git roles/{rolename}
    
    
Create a Github repository for your new role. 
- Stick to this naming convention for your roles: https://github.com/{username}/ansible-role-{rolename}

Rename the original repository to `upstream` and add your new remote (Github) repository as the new `origin`.

    $ git remote rename origin upstream
    $ git remote add origin https://github.com/terencewestphal/ansible-role-template

Push your commits to the new `origin`
    
    $ git push origin master  
        
To pull in patches from `upstream`, run:  
    
    $ git pull upstream master && git push origin master

Tip: Use Git-flow in your cloned role repositories to keep things clean and make `patching from `upstream` much easier.    

         
**Don't forget to replace `{username}` and `{rolename}` in these files to reflect your changes to the role!**
 - `README.md`
 - `meta/main.yml`
 - `.travis.yml`
 
 
License
-------

MIT

Author Information
------------------

- Author: Terence Westphal
- Company: 42 BV