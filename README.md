# DHCP

## Configure

First change the dhcp config file `data/dhcpd.conf`

## Run

### Docker

```sh
docker run --rm --net host -v "$(pwd)/data":/data aisuhua/dhcp:latest <INTERFACE>
```

### Docker Compose

Change the interface

```yaml
# .env
INTERFACE=xxx
```

Run

```sh
docker-compose up
```

## Refs

- https://github.com/3mdeb/dhcp-server
- https://github.com/networkboot/docker-dhcpd
