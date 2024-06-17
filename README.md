🍫 cacao: CA Certification Automated with One-click
===================================================================

Overview
--------
cacao is a script for generating TLS certificates with a custom Certificate Authority (CA). The project aims to simplify the process of creating and managing TLS certificates using a custom CA, with minimal setup and execution effort.

Requirements
------------
Basic requirements are:
- xonsh
- OpenSSL

For automatically downloading CA certificate:
- BitWarden CLI

Installation
------------
```
git clone https://github.com/concertypin/cacao
```

Usage
-----
`create-certificate <target> [keylen]`
- This script generates a new TLS certificate using the custom CA.
- `<target>` is either FQDN or IP address.
- `[keylen] determines RSA key length. Default is 4096-bit.
- If there is no `rootCA.pem` and `rootCA.key` file, it runs `generate-rootCA`.

`generate-rootCA`
- This script creates a new root CA which will be used to sign the TLS certificates. By default, key is RSA 4096-bit.

`download-rootCA`
- This script allows you to download the root CA certificate from BitWarden.

Before running these scripts, you need to configure your credentials in the example.* files. Rename the example.* files after filling in your credentials:

- Open the example.* files in a text editor.
- Fill in the required credentials. Required credentials is masked with `<here>`.
- Rename the files accordingly.

Support
-------
If you encounter any issues or have any questions, please contact the project maintainers.

