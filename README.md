# FORGE SSL

A Simple role uploading our certificate and key.

One must put the private key to ./files/forgeservicelab.fi.key before using it.

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
- key in /etc/ssl/forgeservicelab.fi.key
- cert in /etc/ssl/forgeservicelab.fi.crt
- cert chain necessary for Sonera certs in /etc/ssl/forgeservicelab.fi.crt.chain. Useful for Apache SSLCertificateChainFile directive.
- the whole chain (cert for *.forgeservicelab.fi plus the Sonera chain) in /etc/ssl/forgeservicelab.fi.crt.wholechain. Useful for nginx ssl_certificate directive.

It's possible to rewrite above paths with variables forge\_ssl\_key,
forge\_ssl\_cert, forge\_ssl\_cert\_chain, forge\_ssl\_cert\_wholechain
-
