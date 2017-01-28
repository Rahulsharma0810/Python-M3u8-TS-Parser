# M3u8Parser
Python Script to Get Higher Stream Resolution and Concatenate TS Files Together

This Concatenate Script Will Download M3u8 Stream File from given server

>>`#EXTM3U`

>>`#EXT-X-VERSION:7`

>>`#EXT-X-STREAM-INF:CLOSED-CAPTIONS=NONE,PROGRAM-ID=1,BANDWIDTH=721673,AVERAGE-BANDWIDTH=595000,RESOLUTION=640x360,FRAME-RATE=25.000,CODECS="avc1.4D4016,mp4a.40.2"`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604324/playlist.m3u8`

>>`#EXT-X-STREAM-INF:CLOSED-CAPTIONS=NONE,PROGRAM-ID=1,BANDWIDTH=2019121,AVERAGE-BANDWIDTH=1319000,RESOLUTION=960x540,FRAME-RATE=25.000,CODECS="avc1.64001F,mp4a.40.2"`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604302/playlist.m3u8`

>>`#EXT-X-STREAM-INF:CLOSED-CAPTIONS=NONE,PROGRAM-ID=1,BANDWIDTH=3301670,AVERAGE-BANDWIDTH=1956000,RESOLUTION=1280x720,FRAME-RATE=25.000,CODECS="avc1.64001F,mp4a.40.2"`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604317/playlist.m3u8`

>>`#EXT-X-STREAM-INF:CLOSED-CAPTIONS=NONE,PROGRAM-ID=1,BANDWIDTH=5986861,AVERAGE-BANDWIDTH=2829000,RESOLUTION=1920x1080,FRAME-RATE=25.000,CODECS="avc1.640028,mp4a.40.2"`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604330/playlist.m3u8`

Then It will Find Higher Resolution `RESOLUTION=1920x1080` in this file Using Regex
Go to Higher Resolution File, Download it and Concatenate all TS File with Base URL 

###Sample 

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604330/segment_01.ts`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604330/segment_01.ts`

>>`https://sky.vimeocdn.com/1485613457-0xffc139082a255f69d54c0603ec95bf2a55c22fae/159463108/video/499604330/segment_256.ts`

and so on

###Anatonomy 

>>Create MasterPlaylist Folder Where Final Playlist will save.

>>Downloading Master Stream Playlist as 01_Master.m3u

>>Find Higher Resolution in 01_Master.m3u

>>Parse Reolution and its URL to 02_Master.m3u

>>Remove Scrap from 02_Master.m3u

>>Download Chucks Playlist using 03_Master.m3u URL.

>>Removing Extension and Filename From 02_Master.m3u to 04_Master.m3u

>>Finally Concatenate URL + Chucks to MasterPlaylist/01_Master.m3u8




