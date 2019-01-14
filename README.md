![](https://i.snag.gy/amPTGo.jpg)

# Nicotine for raspberry pi

this is a fork of https://github.com/realies/soulseek-docker (they did all the work) and this is the really first version that need some cleaning. 

The goal is to have nicotine+ running on a RPI and access it via web. 

## Typical Usage

##### Using Docker CLI
```
docker run -d --name nicotine --restart=always \
-v "[your_host_config_dir]":"/root/.nicotine" \ #to preserve config and logs. Typically /home/pi/.nicotine
-v "[your_host_music_directory]":"/root/nicotine_downloads" \
-v "[your_host_upload_dir]":"/root/nicotine_uploads" \
-e resolution=1280x720 \
-p 6080:6080 \
kokmok/rpi-nicotine-novnc:latest
```

Just go to http://IP_OF_PI:6080
You'll have to choose /root/nicotine_downloads as download folder in the nicotine GUI on first start

