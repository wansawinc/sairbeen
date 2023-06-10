## Input source

Facebook , Youtube and Instagram does not allow live stream with audio only using ffmpeg. \
Created 2 videos seperate for Instagram and for others .

in.mkv is used on Instagram ( 720x1280 ) \
fb.mkv is used for all others
```
ffmpeg -i fb.mp4 -s 1280x720 -c libx265 -tune animation -r 2 -preset ultrafast hls/fb.mkv
```

ffmpeg -i in.mp4 -i http://air.pc.cdn.bitgravity.com/air/live/pbaudio136/chunklist.m3u8 -c:a copy c:v copy -f flv rtmp://live.onestream.studio/live/live_183859_2rrvsrgmb

fb.mkv link : https://raw.githubusercontent.com/wansawinc/sairbeen/main/source/fb.mp4 \
in.mkv link : https://raw.githubusercontent.com/wansawinc/sairbeen/main/source/in.mp4 \
Audio stream: https://raw.githubusercontent.com/wansawinc/sairbeen/main/source/audio.m3u8 \
Audio Default: http://air.pc.cdn.bitgravity.com/air/live/pbaudio136/chunklist.m3u8


