# Vaultwarden

Deploy `vaultwarden` with Docker compose behind `traefik` proxy and `Let's Encrypt` Certs.

## ENV Vars

Change Environment variables

```yaml
DOMAIN: https://vaultwarden.puvvadi.net # Change to fqdn & make sure DNS is pointed at traefik proxy server with valid CNAME entry
SMTP_HOST: smtp.example.com # smtp is optional
SMTP_FROM: email@example.com
SMTP_FROM_NAME: Vaultwarden
SMTP_SECURITY: TLS
SMTP_PORT: XXXX
SMTP_USERNAME: email@example.com
SMTP_PASSWORD: YourReallyStrongPasswordHere
SMTP_AUTH_MECHANISM: "Mechanism"
SIGNUPS_ALLOWED: true
```

Make sure to change `SIGNUPS_ALLOWED` to `false` after the account creation for the public instances. For alerts and email delivery, enable and add SMTP server details. Otherwise remove them.

## Deploy

```shell
docker compose up -d
```
