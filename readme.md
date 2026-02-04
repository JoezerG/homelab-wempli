# Homelab Wempli

## Servers

Host: 192.168.144.45

### Grafana

- http://grafana:3000

### Loki

- http://loki:3100

### Prometheus

- http://prometheus:9090

## Clients

En todos los nodos se debe instalar el deamon de alloy

Link de documentacion

[Instalacion Alloy](https://grafana.com/docs/alloy/latest/set-up/install/linux/)

Y copiar el archivo de config a la ruta /etc/alloy/config.alloy

### MariaDB

Se debe crear el usuario para el mysqld_exporter

```sql
CREATE USER 'exporter'@'localhost' IDENTIFIED BY 'STRONG_PASSWORD';
GRANT PROCESS, REPLICATION CLIENT, SELECT ON *.* TO 'exporter'@'localhost';
FLUSH PRIVILEGES;
```
