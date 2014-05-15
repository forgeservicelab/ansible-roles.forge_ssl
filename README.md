# FORGE SSL

A Simple role uploadign our certificate and key.

On must put the private key to ./files/forgeservicelab.fi.key before using it.

The certificate is already there.

It will upload the

The repo (git)ignores ./files/\*key.

simple

```
  roles:
    [...]
    - role: forge_ssl
    [...]
```

will make sure that you have the
- cert in /etc/ssl/forgeservicelab.fi.crt
- key in /etc/ssl/forgeservicelab.fi.key
