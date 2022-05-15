Ansible role: zh2s.install_postfix
=========

Install MTA — postfix. It's use ONLY FOR sending email. Also this role rename hostname of yout machine for creating aliases for redirecting system message from `root`
and `postmaster` entities.

Role Variables
--------------

    domain: enter your domain here
    admin_email: enter your main email adress (xxxxxxxxxx@gmail.com or something else)

Example Playbook
----------------

    - hosts: all
      vars:
        domain: foo.com
        admin_email: foo@gmail.com

      roles:
         - { role: zh2s.install_postfix }
