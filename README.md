Role Name
=========

A simple role that configures common things on all servers.

Requirements
------------

To provision users

Information on how to generate a password can be found [here](http://docs.ansible.com/ansible/faq.html#how-do-i-generate-crypted-passwords-for-the-user-module).


Role Variables
--------------

No role variables defined by default. You will need to define users if you want any users to be provisoned.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      vars:
        users:
        - name: user1
          password: $6$rounds=100000$/SK7so1fc7j96kpp$hGBMwK/.IWwpyLMCd94hVqVdbO78aooIEqWfNAfaTfF6QfM/.rcjC90twEHMSew7XV4EhS53j2PYsmKf.qjYl.
          groups: wheel,adm
        - name: user2
          password: $6$rounds=100000$/SK7so1fc7j96kpp$hGBMwK/.IWwpyLMCd94hVqVdbO78aooIEqWfNAfaTfF6QfM/.rcjC90twEHMSew7XV4EhS53j2PYsmKf.qjYl.

      roles:
         - opuk.common

You may want to consider putting your users in a group_vars files instead.

License
-------

BSD
