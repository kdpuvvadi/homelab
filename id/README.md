# Zitadel

Generate master key for zitadel first with the following & save it as `ZITADEL_MASTERKEY`in `.env`.

```bash
tr -dc A-Za-z0-9 </dev/urandom | head -c 32
```

Add desired admin username and password.

```env
ZITADEL_FIRSTINSTANCE_ORG_HUMAN_USERNAME=
ZITADEL_FIRSTINSTANCE_ORG_HUMAN_PASSWORD=
```

Up on first login, password needs to changed.

To deploy,

```bash
docker compose up -d
```
