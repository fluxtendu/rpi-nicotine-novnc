![](https://i.snag.gy/8dpAbV.jpg)

# Nicotine for raspberry pi

this is a fork of https://github.com/michaelmiklis/docker-rpi-monitor and this is the really first version that need some cleaning. 

The goal is to have nicotine+ running on a RPI and access it via web. 

## Typical Usage

##### Using Docker CLI
```
docker run -d --name nicotine --restart=always \
-v "/persistent/appdata":"/root/.SoulseekQt" \
-v "/persistent/logs":"/root/Soulseek Chat Logs" \
-v "[your_host_music file]":"/root/nicotine" \
-e resolution=1280x720 \
-p 6080:6080 \
kokmok/rpi-nicotine-novnc:latest
```

Just go to http://IP_OF_PI:6080
You'll have to choose /root/nicotine in the nicotiune GUI on first start

