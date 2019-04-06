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
	* x86_64_linux_gnu is my operating system so if this folder  doesn't exist, you must check your operating system. [Go to Caution](#caution)

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


## Acknowledgments
* [Opera Forums](https://forums.opera.com/topic/22685/twitter-videos/5)
* [Youtube Supported Browser section](https://www.youtube.com/html5)
* [StackExchange Answer -1 ](https://askubuntu.com/a/214433/923958)
* [StackExchange Answer -2](https://askubuntu.com/a/384659/923958)

