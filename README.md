
stockholmsaltspa.se
===================

Provisioning of stockholmsaltspa.se WordPress site.


Dev Environment
---------------

Create a virtualenv and install requirements:

    virtualenv venv
    source venv/bin/activate
    pip install -r requirements.txt
    ansible-galaxy install -r requirements.yml


Testing with Vagrant
--------------------

Assuming Vagrant and VirtualBox are installed:

    source venv/bin/activate
    vagrant up --provision
    # Then, to provision manually:
    ansible-playbook -l vagrant provision.yml

