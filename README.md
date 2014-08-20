# Ansible Role for Sentry

[![Build Status](https://travis-ci.org/mortik/ansible-ruby.png?branch=master)](https://travis-ci.org/mortik/ansible-ruby)

A Simple Role to install Sentry

# Role variables

    sentry_user: sentry
    sentry_domain: sentry.dev
    sentry_protocol: http
    sentry_port: 9000
    sentry_db:
      name: sentry
      user: sentry
      password:
      host:
      port:
    sentry_secret:
    sentry_mail:
      default_from:
    sentry_smtp:
      host:
      password:
      user:
      port:
    sentry_superuser:
      name: "max"
      email: "max@mustermann.de"
      password: "nopass"
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


# Test

    ansible-playbook -i vagrant --private-key ~/.vagrant.d/insecure_private_key role.yml

## License

MIT

