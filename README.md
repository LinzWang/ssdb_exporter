# Prometheus SSDB Exporter
support auth variables 

This repository is a fork of [kys1230/ssdb_exporter](https://github.com/kys1230/ssdb_exporter). I've just made some changes to enable succesfull dockerization and a collection of replication parameters. It has now two ways of configuration, which are described below.

## Usage

The Prometheus SSDB Exporter use command line flags , as well as environment variables. If the environment variables are set, values from flags are overwritten.

### Flags
- `-bind-addr string` - bind address for the metrics server (default ":9142")`
- `-log-level string` - log level (default "info")`
- `-metrics-path string` - path to metrics endpoint (default "/metrics")
- `-ssdb-list string` - host1:port1,host2:port2 for ssdb socket (default "localhost:8888")`
- `-ssdb-auth string` - auth ssdb (default "")
### Environment variables
- `BIND_ADDR` - same as `-bind-addr`
- `LOG_LEVEL` - same as `-log-level`
- `METRICS_PATH` - same as `-metrics-path`
- `SSDB_LIST`  - same as `-ssdb-list`
- `SSDB_AUTH` - same as `-ssdb-auth`

## Grafana Dashboard

I've created some Grafana Dashboard to use with Prometheus. You can find it [here.](https://grafana.com/grafana/dashboards/11332)

## Docker images

The ssdb exporter is also built as a docker image, available [here.](https://hub.docker.com/r/sgrzemski/ssdb_exporter)
