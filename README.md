My friend's bag got stolen overnight from our parked rental car. The security camera recorded everything, but the video files it saved on the SD card were .H264 elementary streams that weren't playable with regular video players (VLC & QuickTime). Luckily, the security camera app was able to play it back, but with a clunky interface it took ages to watch through hours of video. This is my attempt at decoding the elementary streams and transcoding them into a regular MP4 container.

`ffmpeg -loglevel trace` (see `ffreport.txt`) - used to read the NALs, PPS, and SPSs

A hex editor was used to modify the NAL units and IDCs, and add padding 00 bytes where needed
