# lenses-ansible

Installs Lenses Dashboard on your VM

## Requirements

Java

## Role Variables

Set the protocol you are using in your Kafka cluster:  PLAINTEXT/SSL_AUTH/SSL_ENCRYPT/SASL_PLAINTEXT/SASL_SCRAM
At the moment only: PLAINTEXT and SASL_PLAINTEXT are supported. SASL_SCRAM should be as well, but its not tested.

    security_protocol: 

If trial is set to "yes" you have to change `trial_download_url` so that points to archive you got from Lenses with generated trail license.

    trial:

Otherwise change `templates/enterpise-license.json` with value you got from Lenses.

If you want create User home directory enable following var:
    
    create_home: yes

At the moment only LDAP and Basic security mode is supported. Change var to "BASIC" or "LDAP" in order to trigger filling of security.conf

    security_conf:
      mode: "BASIC"

## Suggestion

If you bought a license use [ansible-vault](https://docs.ansible.com/ansible/latest/user_guide/vault.html) to make little bit more secure. 

## TODO:

- [] add ssl_auth support 
- [] add ssl_encrypt support
- [] add sasl_ssl support



## Author Information

This playbook was created in 2019 by [iMajna](https://github.com/iMajna)
