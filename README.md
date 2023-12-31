# DHCP Server 

## Configure

First change the dhcp config file `data/dhcpd.conf`

## Run

### Docker

```sh
docker run --rm --name dhcp-server --init --net host -v "$(pwd)/data":/data aisuhua/dhcp-server:latest <INTERFACE>
```

### Docker Compose

Change the interface

```yaml
# docker-compose.yaml
dhcp-server:
  command: <INTERFACE>
```

Run

```sh
docker-compose up
```

## Refs

- https://github.com/3mdeb/dhcp-server
- https://github.com/networkboot/docker-dhcpd
