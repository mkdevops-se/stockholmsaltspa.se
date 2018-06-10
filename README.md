
mjlife.se
=========

Provisioning of mjlife.se WordPress site.


Dev Environment
---------------

Create a virtualenv and install pip requirements:

    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt


Testing with Vagrant
--------------------

Assuming Vagrant and VirtualBox are installed:

    source venv/bin/activate
    vagrant up --provision
    # Then, to provision manually:
    ansible-playbook -l vagrant provision.yml

