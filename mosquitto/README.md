On some Linux distributions there could be problems with write permission to volume:

```Error: Unable to open log file /mqtt/logs/mosquitto.log for writing.```

then apply write permission to the volume, in my case:

```sudo chown -R 1883:1883 ~/docker-volumes/mosquitto```

and restart docker.