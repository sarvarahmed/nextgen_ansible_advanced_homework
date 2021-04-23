A brief description of the playbooks and roles elated to AWS PROD Environment goes here.
========================================================================================

Playbook Name
=============


- aws_creds.yml           -->  Playbook to install ansible-tower-cli on bastion node and cretate AWS Credentials
- aws_provision.yml       -->  Plabook to provision AWS Prod Environment
- aws_status_check.yml    -->  Playbook to check the status of the AWS instances
- site-3tier-app-prod.yml -->  Gather facts to get internal IPs of the servers
                          -->  Setup database tier for prod env
                          -->  Setup app tier for prod env
                          -->  Setup load-balancer tier for prod env
- site-smoketest-aws.yml  -->  Smoke Test For AWS Prod Environment



Role Name
=========


- base-config             -->  Role to Add internal repo to the aws instances
- app-tier-prod           -->  Role to setup app servers in AWS Prod Environment
- db-tier-prod            -->  Role to setup db servers in AWS Prod Environment
- lb-tier-prod            -->  Role to setup frontend servers in AWS Prod Environment



A brief description of the playbooks and roles elated to OSP QA Environment goes here.
========================================================================================

Playbook Name
=============


- site-osp-instances.yml  -->  Playbook to provision instances in OSP Environment
- site-3tier-app.yml      -->  Playbook Role to provision 3tier APP
                          -->  Setup database tier for QA env
                          -->  Setup app tier for QA env
                          -->  Setup load-balancer tier for QA env
- site-smoke-osp.yml      -->  Smoke Test For osp QA Environment


Role Name
=========


- base-config             -->  Role to Add internal repo to the OSP instances
- app-tier                -->  Role to setup app servers in OSP QA  Environment
- db-tier                 -->  Role to setup db servers in OSP QA Environment
- lb-tier                 -->  Role to setup frontend servers in OSP QA Environment




Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
