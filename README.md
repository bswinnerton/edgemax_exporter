edgemax_exporter [![GoDoc](http://godoc.org/github.com/mdlayher/edgemax_exporter?status.svg)](http://godoc.org/github.com/mdlayher/edgemax_exporter) [![Build Status](https://travis-ci.org/mdlayher/edgemax_exporter.svg?branch=master)](https://travis-ci.org/mdlayher/edgemax_exporter) [![Coverage Status](https://coveralls.io/repos/mdlayher/edgemax_exporter/badge.svg?branch=master)](https://coveralls.io/r/mdlayher/edgemax_exporter?branch=master)
================

This is a fork of `mdlayher/edgemax_exporter`, which is no longer maintained. It has been updated to include support for running in a Docker container, similar to mdlayher's unifi_exporter project.

It can be used with something like this:

```
sudo docker run -d \
    --name="edgemax_exporter" \
    --restart=always \
    --publish=9132:9132 \
    -v /etc/ssl/certs:/etc/ssl/certs \
    bswinnerton/edgemax_exporter \
    -edgemax.addr https://10.0.0.1 \
    -edgemax.username metrics \
    -edgemax.password correcthorsebatterystaple
```

Command `edgemax_exporter` provides a Prometheus exporter for a Ubiquiti EdgeMAX
devices.

Package `edgemaxexporter` provides the Exporter type used in the `edgemax_exporter`
Prometheus exporter.

MIT Licensed.
