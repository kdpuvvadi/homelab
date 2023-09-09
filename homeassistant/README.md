## homeassistant

homeassistant config files. only `configuration.yaml` exists in the control node. Others are just placeholders.

### rclone config

```rclone
[hass]
type = sftp
host = 10.20.20.115
user = root
key_file = ~/id_ed25519
pubkey_file = ~/id_ed25519.pub
```
# sync config with rclone

```shell
rclone sync ./homeassistant hass:/root/config
```
