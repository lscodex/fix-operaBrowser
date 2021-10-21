# Opera issue
I worked for 2 weeks to find a solution :)
### youtube: your browser does not currently recognize any of the video formats available
 * if you can not open to a video that in youtube live or twitter
 * if you haven't a file that /usr/lib/x86_64-linux-gnu/oxide-qt/

### Caution 

My ubuntu is: 
Distributor ID:	Ubuntu
Description:	Ubuntu 18.04.2 LTS
Release:	18.04
Codename:	bionic

if you want to check yours: 

```
lsb_release -a 
```

My ubuntu is running on ** x86_64 **

if you want to check yours: 

```
uname -m
```
### Prerequisites 
* Firstly, you must check the file that /usr/lib/chromium-browser/
	* if it does not exist, you can download or install it,
	* or you can download folder from my repo and cp to /usr/lib
	```
	cd && sudo cp -r "DOWNLOAD_FILE" /usr/lib/chromium-browser
	```


* Secondly, you must check the file that /usr/lib/x86_64-linux-gnu/opera/
	* x86_64_linux_gnu is my operating system so if this folder  doesn't exist, you must check your operating system.
	[Go to Caution](#caution)

## INSTALL 
* sudo apt-get install ubuntu-restricted-extras
* sudo apt-get install h264enc

## COPY 
Finally, you copy libffmpeg.so to opera folder :

```
cd && sudo cp -r /usr/lib/chromium-browser/libffmpeg.so /usr/lib/x86_64-linux-gnu/opera/libffmpeg.so
```
### RESTART OPERA
```
sudo killall -s KILL opera 
```
and reopen the browser 

### FOR THE ISSUE THAT ON UBUNTU 16.04

All the suggestions above were for ubuntu 18. 
So, I faced this issue again when I swapped ubuntu 18 to ubuntu 16. I searched google. And h264ecnc is not supported ubuntu 16. And I don't know what chroium-browser is. But found this path in the [stackoverflow](https://askubuntu.com/a/1067267) (oo my gosh)

Firstly: 
I get the backup file that /usr/lib/x86_64_linux_gnu/opera/libffmpeg.so

```
cp /usr/lib/x86_64_linux_gnu/opera/libffmpeg.so /usr/lib/x86_64_linux_gnu/opera/libffmpeg.so.bak
```

But this path is not the same for my pc. So, I searched chromium step by step and  I found these folders in /snap/chromium-ffmpeg/23/ in my pc: 

example for folders in the path:
	
- /chromium-ffmpeg-1033551/chromium-ffmpeg/libffmpeg.so
- /chromium-ffmpeg-1041895/chromium-ffmpeg/libffmpeg.so
- /chromium-ffmpge-95241/chromium-ffmpeg/libffmpeg.so

And finally, from all the above files one by one I tried to copy step by step file that libffmpeg.so to /usr/lib/x86_64_linux_gnu/opera.

one of them is works successfully.

```
/snap/chromium-ffmpeg/23/chromium-ffmpeg-95241/chromium-ffmpeg/libffmpeg.so
```



## Acknowledgments
* [Opera Forums](https://forums.opera.com/topic/22685/twitter-videos/5)
* [Youtube Supported Browser section](https://www.youtube.com/html5)
* [StackExchange Answer -1 ](https://askubuntu.com/a/214433/923958)
* [StackExchange Answer -2](https://askubuntu.com/a/384659/923958)

