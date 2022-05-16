Ansible role: zh2s.install_postfix
=========

Install MTA — postfix. It's use ONLY FOR sending email. Also this role rename hostname of yout machine for creating aliases for redirecting system message from `root`
and `postmaster` entities.

:warning: You should stop your web server before start this role
--------------

If you have running web server that bind to 80 port, you should first stop web server and ONLY then start this ansible role. After installation you can start web server again. This restriction is needed to generate Let's encrypt certificate

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
