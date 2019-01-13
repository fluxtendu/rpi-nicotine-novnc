![](https://i.snag.gy/amPTGo.jpg)

# Nicotine for raspberry pi

this is a fork of https://github.com/michaelmiklis/docker-rpi-monitor (they did all the work) and this is the really first version that need some cleaning. 

The goal is to have nicotine+ running on a RPI and access it via web. 

## Typical Usage

##### Using Docker CLI
```
docker run -d --name nicotine --restart=always \
-v "[your_host_wanted_logs_save]":"/root/.nicotine/logs" \
-v "[your_host_music_directory]":"/root/nicotine" \
-e resolution=1280x720 \
-p 6080:6080 \
kokmok/rpi-nicotine-novnc:latest
```

Just go to http://IP_OF_PI:6080
You'll have to choose /root/nicotine as download folder in the nicotiune GUI on first start

