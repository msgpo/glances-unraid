# Glances for unRAID
===============================

Modified version of adrien's glances-unraid docker container. This container allows you to specify args for glances rather than assuming you want to use the web version

```
docker run -d --name="glances-unraid" -e GLANCES_ARGS="--quiet --export-influxdb -C /tmp/glances.conf" --net="host" --pid host -e TZ="America/Chicago" -v "/var/run/docker.sock":"/var/run/docker.sock":rw -v "/mnt":"/mnt":ro -v "/tmp":"/tmp":rw drewster727/glances-unraid
```

To be used with [https://lime-technology.com/](https://lime-technology.com/)
