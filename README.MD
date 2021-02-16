# Shadowsocksr server using docker-compose

This project simplifies starting a shadowsocksr server using docker

# Setup

Initial setup:

- Copy `.env.example` to `.env`
- Set env variables as per your needs in `.env`
- Run `./docker-compose up --build`

Example `.env` file content:

```shell
SERVER_ADDR="0.0.0.0"
SERVER_PORT=443
PASSWORD=password
METHOD=aes-256-cfb
PROTOCOL=origin
PROTOCOLPARAM=32
OBFS=tls1.2_ticket_auth_compatible
TIMEOUT=300
DNS_ADDR="1.1.1.1"
DNS_ADDR_2="1.0.0.1"
```

# Configuration help

### Supported ciphers:

- none
- aes-256-cfb
- aes-192-cfb
- aes-128-cfb
- aes-256-cfb8
- aes-192-cfb8
- aes-128-cfb8
- aes-256-ctr
- aes-192-ctr
- aes-128-ctr
- chacha20-ietf
- chacha20
- salsa20
- xchacha20
- xsalsa20
- rc4-md5

### Supported protocols:

- origin
- verify_deflate
- auth_sha1_v4
- auth_sha1_v4_compatible
- auth_aes128_md5
- auth_aes128_sha1
- auth_chain_a
- auth_chain_b

### Supported obfuscators:

- plain
- http_simple
- http_simple_compatible
- http_post
- http_post_compatible
- tls1.2_ticket_auth
- tls1.2_ticket_auth_compatible
- tls1.2_ticket_fastauth
- tls1.2_ticket_fastauth_compatible
