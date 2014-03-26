# Ansible: Provisioning for Vagrant




Mark Burns

Twitter: @hydrantmark

Slides: hydrantmark.github.io/vagrant-ansible

Github: github.com/hydrantmark/vagrant-ansible

---

# Recap

## Repeatable and shareable development environments with Vagrant - Andrew Donaldson
A session at Code Cumbria North - 2014.02
http://lanyrd.com/2014/ccn1402/scxfgy/

# Presenter Notes

- Vagrant: commandline tool for managing virtual machines via simple config files
- Really useful for creating dev environments which can be shared
- Comes alive when used with a provisioning tool
- Provisioning: setup, configuration management
- Brief introduction to Ansible, and then a demo

---

# Ansible

> Radically simple IT orchestration.

- Not just limited for use with Vagrant

# Presenter Notes

- Can be used for actual Server and/or Workstation configurations
- Push based (with vagrant or ansible-playbook)
  - playbooks run from control host, pushing to recipients
  - host inventory file
- Pull based (ansible-pull)
  - Ansible installed on each host
  - Playbooks in version control
  - Checks out playbook, and executes
  - Automate via cron

---

# Another Tool in the Box

- Chef, Puppet, shell scripts

---

# Inventory File

- The *Where*

# Presenter Notes

- Provides a list of hosts to connect to, and connection options

---

# Playbooks

- The *What*
- Just YAML files

> YAML is a human friendly data serialization standard for all programming languages.

# Presenter Notes

- YAML Ain't Markup Language
- Structured key value store
- Data oriented rather than document markup
- *Plays:* a playbook is made up of one or more 'plays' executed in sequence
- *Roles:* allow you to create more maintable collections of plays
- *Tags:* mark a section of a playbook, can be run on demand
- *Variables:* allows you set reusable values for use in playbooks
- *Conditional Actions:* execute something based upon some condition
- *Rolling Deploys:* run a playbook on more than one node, and set a maximum failure rate 

---

# Modules

- Loads available
- (Very) small selection
  - *Packaging:* apt, yum, pip, npm, gem, homebrew
  - *Files:* file, copy, template, lineinfile
  - *Notification:* campfire, hipchat, irc, jabber, email
  - *CLI:* command, shell
- Roll your own

# Presenter Notes

- Can be executed directly either locally, or remotely from the command line
- Or via Playbooks
- For full list http://docs.ansible.com/list_of_all_modules.html
- For writing modules, use any language you want, only file i/o and outputting to standard out are required 

---

# Demo




## How do you like them Gremlins?

# Presenter Notes

- Simple example
  - install ntpd (if not already), stop it, set the date, provide new config, and restart
  - and some extra repositories - makes use of variables

---

# More Information

Loads of examples online

- Vagrant http://www.vagrantup.com/
- Vagrant Documentation https://docs.vagrantup.com/
- Ansible http://www.ansible.com/home
- Ansible Documentation - http://docs.ansible.com/

---

# Questions?

---

# Credits

- Code Cumbria North 2014.02: Talk by Andrew Donaldson http://lanyrd.com/2014/ccn1402/scxfgy/
- PHPNW 2013: Talk by Micheal Heap http://lanyrd.com/2013/phpnw/scqwwb/
- Vagrant Anisble Provisioning Example from hnakamur https://github.com/hnakamur/vagrant-a
- Ansible: Server configuration the easy way - Stefan Wienert http://www.stefanwienert.net/blog/2013/09/28/ansible-server-configuration-the-easy-way/
- Scalable and Understandable Provisioning with Ansible and Vagrant http://julien.ponge.org/blog/scalable-and-understandable-provisioning-with-ansible-and-vagrant/

---

Mark Burns

Twitter: @hydrantmark

Slides: hydrantmark.github.io/vagrant-ansible

Github: github.com/hydrantmark/vagrant-ansible
