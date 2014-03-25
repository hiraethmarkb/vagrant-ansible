# Ansible: Provisioning for Vagrant by Mark Burns

Following on from Andrew's talk last month about using Vagrant for creating repeatable and shareable dev environments, this talk will look at using Ansible to provision a Vagrant box.

# Outline

  ## Recap

    - Vagrant tool for managing virtual machines via simple config files and the commandline
    - Really useful for create dev environments which cna be shared
    - Comes alive when when with a provisioning tool
      - Provisioning - setup, configuration

  ## Ansible

    - Another tool in the box
      - Really simple IT orchestration
      - Others Chef, Puppet, Shell scripts
    - Not just limited to use with Vagrant
      - Server, Workstation config
    - Playbooks (written in YAML)
      - YAML Ain't Markup Language
      - data oriented rather than document markup
    - Modules
      - Can be executed directly typically on remote hosts
      - Via Playbooks
      - Long list - http://docs.ansible.com/list_of_all_modules.html
    - Push based (with vagrant or ansible-playbook)
      - playbooks run from control host, pushing to recipients
      - host inventory file
    - Pull based (ansible-pull)
      - Ansible installed on each host
      - Playbooks in version control
      - Checks out playbook, and executes
      - Automate via cron

  ## Demo

    - How do you like them Gremlins?
  
  ## More Information

    - Vagrant
      - http://www.vagrantup.com/
    - Vagrant Documentation
      - https://docs.vagrantup.com/
    - Ansible
      - http://www.ansible.com/home
    - Ansible Documentation
      - http://docs.ansible.com/
    - YAML
      - http://www.yaml.org/
   
    - Loads of examples online, Google and Github are your friends

  ## Credits

    - PHPNW 2013: Talk by Micheal Heap
      - http://lanyrd.com/2013/phpnw/scqwwb/
    - Code Cumbria North
      - 2014.02: Talk by Andrew Donaldson http://lanyrd.com/2014/ccn1402/scxfgy/
    - Vagrant Anisble Provisioning Example from hnakamur
      - https://github.com/hnakamur/vagrant-ansible-provisioning-example
    - Ansible: Server configuration the easy way - Stefan Wienert
      - http://www.stefanwienert.net/blog/2013/09/28/ansible-server-configuration-the-easy-way/
    - Scalable and Understandable Provisioning with Ansible and Vagrant
      - http://julien.ponge.org/blog/scalable-and-understandable-provisioning-with-ansible-and-vagrant/

  ## Questions ?

