# Notes

- Connect to running container:
  - determine container id by running `docker ps`
  - connect to the containers bash shell `docker exec -it afcc05100a61 bash`
- Login to influxdb shell
  - `influx -username LOGIN -password PASSWORD
- When volumes are mounted there are problems with saving data to it.
  - Possible solutions:
    - `sudo chown -R influxdb:influxdb /var/lib/influxdb`
  - Working but not safe solution: `sudo chmod -R 777 ~/docker-volumes/influxdb`
- Grafana needs ownership of its volume for the user 472:
  - `sudo chown -R 472:472 ./grafana`
