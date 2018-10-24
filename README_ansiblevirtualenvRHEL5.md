## Instructions of Creating a RHEL 5 Virtual Env in Tower 3
The Docs Explain how to use Virtuaenv in Toswer 3.3 here
https://docs.ansible.com/ansible-tower/latest/html/upgrade-migration-guide/virtualenv.html

This Guide Walks you to thru doing this for managing RHEL5 Distributions


First Login to your Tower Environment and create a new Custom virtualenv

 mkdir -p /var/lib/awx/venv/rhel51
Initialize the virtual Environment

sudo virtualenv /var/lib/awx/venv/rhel51

Install the Base Dependencies that Tower Needs

sudo /var/lib/awx/venv/rhel51/bin/pip install python-memcached psutil

Since  ansible 2.4 there has been no support for RHEL we will build this virtual Environment
with Ansible 2.3  per https://access.redhat.com/solutions/3092521

We will be initializing this Environment with Ansible 2.3


sudo /var/lib/awx/venv/rhel51/bin/pip install -U "ansible == 2.3"

This Preps the Virtual Env and this virtual env is now ready to use
with Ansible Tower 3.3  for Accessing RHEL5 environments


 
