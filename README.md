# CFV systemd backup

Backups of `/etc/systemd` from Titan machines, taken 2026-10-29.

Each archive was created on its machine with:

```sh
sudo tar -czvf "$(hostname)_systemd.tar.gz" /etc/systemd
```

## Machines

- `titan-dvt1-printer-rtec`
- `titan-dvt1-printer-sv`
- `titan-evt2-mcu-rtec`
- `titan-evt2-mcu-sv`
- `titan-evt2-vm-rtec`
- `titan-teststand-cv-devs`
- `titan-teststand-cir`

## Restoring

Archive paths are relative (`etc/systemd/...`), so extract from `/`:

```sh
sudo tar -xzvf <hostname>_systemd.tar.gz -C /
sudo systemctl daemon-reload
```
