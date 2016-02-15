# ansible-elixir-exrm

Dead simple Ansible playbook to deploy Elixir apps with exrm.

Usage:

```
site.yml

- hosts: production
  roles:
    - { role: exrm, git_url: "your_git_repo", app_name: "your_otp_app_name" }
```


```
inventory
[build_server]
your_build_server

[production]
your_production_server
```

It takes care of building the app on your `build_server`, uploading the latest
version to your production (or staging, or anything you want) server,
and starting or upgrading the app as needed.

If you also want to install Erlang easily, check out

https://github.com/tuvistavie/ansible-erlang
