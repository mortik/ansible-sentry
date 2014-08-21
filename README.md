# Ansible Role for Sentry

[![Build Status](https://travis-ci.org/mortik/ansible-ruby.png?branch=master)](https://travis-ci.org/mortik/ansible-ruby)

A Simple Role to install Sentry

## Dependencies

required:
* postgres

optional but recommended:
* nginx

This Role needs a postgres database, you can install one on your own or set the ```sentry_with_postgres``` variable to ```True```.
If you set ```sentry_with_nginx``` to ```True``` this role install a basic nginx setup with a vhost file (http only) for sentry.

This Role installs supervisor by default to start and watch the sentry process. You can disable this by setting ```sentry_with_supervisor``` to ```False```.

## Role variables

### default

```
sentry_user: sentry
sentry_home: "/home/{{ sentry_user }}"
sentry_domain: sentry.dev
sentry_registration: False
sentry_social_auth_create_users: False
sentry_protocol: http
sentry_port: 9000
sentry_db: sentry
sentry_db_user: sentry
sentry_db_password:
sentry_db_host: ""
sentry_db_port: ""
sentry_secret:
sentry_mail_default_from:
sentry_smtp_host:
sentry_smtp_password:
sentry_smtp_user:
sentry_smtp_port:
sentry_smtp_tls: True
sentry_superuser:
sentry_superuser_username: "admin"
sentry_superuser_email: "admin@fake.com"
sentry_superuser_password: "nopass"
sentry_github:
  id:
  secret:
sentry_twitter:
  key:
  secret:
sentry_facebook:
  id:
  secret:
sentry_google:
  id:
  secret:
sentry_trello:
  key:
  secret:
sentry_bitbucket:
  key:
  secret:
sentry_plugins:
  - "sentry-github"
  - "sentry-pivotal"
  - "sentry-slack"
  - "sentry-trello"
sentry_with_supervisor: True
sentry_with_nginx: False
sentry_with_postgres: False
```

# Test

```
ansible-playbook -i vagrant --private-key ~/.vagrant.d/insecure_private_key role.yml
```

## License

MIT

