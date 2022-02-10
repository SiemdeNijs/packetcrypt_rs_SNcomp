# 🌻⛏️👾 SNcomp packetcrypt miner
These packetcrypt miners are pre-compiled by Siem, with custom flags and tinkering. 

Use at your own risk. No warranty. **Expect no support**, but I do **try** my best to offer help on Discord, PKT.Chat & Reddit.

- include jemalloc flag for supported devices
 
- upward to ~100 % performance gains vs packetcrypt_rs pre-compiled miners
 
- different compiling workflow to achieve a more stable experience (hopefully)
 
- will be tinkered with in future releases for more custom optimizations

- Highest increasements seen by EPYC, 5950x, Intel E-series users reported via Discord/PKT Chat

- Your milegae may vary. But, every penny counts

- The official repo can be found here: https://github.com/cjdelisle/packetcrypt_rs 

## 🚀 Wish to install WSL for the best performance on a Windows host ?

The most convential way is described in detail here for Windows 10 & 11:

https://denijs.photography/pkt-how-to-install-wsl-compile-miner

Please ignore the instructions on how to compile the miner if you use my custom package/auto-comp provided here on GitHub. 

**The instructions on how to self-compile it above are different from what I'm doing with SNcomp:**

I'm personally editing the source & compile it with a very different method.

## 🤖 Use my SDNautocomp script to compile the official miner automatically [Linux/WSL/Android]
```
wget -O ~/sdnautocomp.sh -- url -- && sudo chmod +x ~/sdnautocomp.sh && sudo ~/sdnautocomp.sh 
```
The bash script is usable on native Linux systems, compatible with WSL & also tested on Android phones with UserLAnd (debian). 
It will try to automatically install the dependencies needed to compile the miner, grab the source & tries to compile it on your own machine with your chosen flags, then help you place the miner in "~/", and ask you if you want the minepkt.sh script to easily running the miner.

>Why would you want to self-compile ? As mentioned before (https://denijs.photography/pkt-how-to-install-wsl-compile-miner) self-compiling can drastically improve performance. >Each system is different and generic packages made to be 'compatible/portable' for most systems won't preform as well as a package specifically crafted for & on your own system.

**Again, these instructions above are different from what I'm doing with SNcomp:**
I'm personally editing the source & compile it with a very different method.

// This script is mainly offered so people can measure their performance on pre-compiled official, my compiled version (SNcomp) & their self compiled version.

## ⛏️ Usage:
1 Rename the file to "packetcrypt".

2 Use the miner commands as usual:

Linux

```
/path/to/packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world http://pool.chymera.it http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
```

Windows

```
/path/to/packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world http://pool.chymera.it http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
```

**⚠️Replace the address with your address⚠️**

## 👾 Optional one click run for Windows, WSL or Linx native systemd (tmux) service:

## **🪟 Windows native (running .exe directly on windows machine):**

>  1 Open notepad

>  2 Copy this: 
```
"/path/to/packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world http://pool.chymera.it http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
```

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run your miner.
 
## **🪟🐧 Windows WSL:**

>  1 Open notepad

>  2 Copy this:
```
wsl /path/to/packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world http://pool.chymera.it http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
```

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run your miner.

## **🐧 Linux native, option one: systemd (if unsure pick systemd option 1)**

```
wget -O /etc/systemd/system/pkt.service https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/pkt.service
```

```
wget -O ~/packetcrypt https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/packetcrypt_x8664_linux && sudo chmod +x ~/packetcrypt
```

```
wget -O ~/minepkt.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/minepkt.sh && sudo chmod +x ~/minepkt.sh
```

>sudo nano ~/minepkt.sh **⚠️ edit to your personal pkt address ! ⚠️** Optionally add "-t *number*" to limit the threads used.

> Hit CTRL + X To exit, "Y" to save when prompted.

> sudo nano /etc/systemd/system/pkt.service **⚠️ edit ~/minepkt.sh path to your path ! For example /root/minepkt.sh ! ⚠️**.
> 
> Hit CTRL + X To exit, "Y" to save when prompted.

> sudo systemctl enable pkt **⚠️only if you want to autorun it on boot, else ignore this command⚠️**

> Done. See commands below.

Run the above commands in order to get the the linux miner, bash file "minepkt.sh" , & "pkt.service".


Enable/Disable autorun: "systemctl enable pkt"

or "systemctl disable pkt"

Stop the miner: "systemctl stop pkt"

Start the miner: "systemctl start pkt"

Status of the miner: "systemctl status pkt"

## **🐧 Linux native, option two: systemd with tmux (if unsure pick systemd option 1)**

```
wget -O /etc/systemd/system/pkt.service https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/pkttmux.service
```
 
```
wget -O ~/packetcrypt https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/packetcrypt_x8664_linux && sudo chmod +x ~/packetcrypt
```

```
wget -O ~/minepkt.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/minepkt.sh && sudo chmod +x ~/minepkt.sh
```

```
wget -O ~/pkttmuxmine.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/pkttmuxmine.sh && sudo chmod +x ~/pkttmuxmine.sh
```

> sudo nano ~/minepkt.sh **⚠️ edit to your personal pkt address ! ⚠️** Optionally add "-t *number*" to limit the threads used

> Hit CTRL + X To exit, "Y" to save when prompted.

> sudo nano /etc/systemd/system/pkt.service **⚠️ edit ~/pkttmuxmine.sh path to your path ! For example /root/pkttmuxmine.sh ! ⚠️**.
> 
> Hit CTRL + X To exit, "Y" to save when prompted.

> sudo systemctl enable pkt **⚠️only if you want to autorun it on boot, else ignore this command⚠️**

> Done. See commands below.

Run the above commands in order to get the the linux miner, bash file "minepkt.sh" & "pkttmuxmine.sh", & "pkt.service".

Enable/Disable autorun: "systemctl enable pkt"

or "systemctl disable pkt"

Stop the miner: "systemctl stop pkt"

Start the miner: "systemctl start pkt"

Status of the miner: "systemctl status pkt"

**Tmux session is called "miner"**

Show miner session:
```
tmux attach-session -t miner
```

Detatch from session with ctrl + shift + b, then release and hit "d" to detatch.

[or find the corresponding tmux commands for your system]

## **🐧 Android phone UserLAnd mining, debian aarch64/armu package**

> Fist install UserLAnd app [https://play.google.com/store/apps/details?id=tech.ula], setup the debian distro. Look up how to "unrestrict battery usage" & "unrestrict data usage" in your phone settings (often under settings -> Apps -> UserLAnd), also make sure the app has all the correct permissions. Run sudo apt update & sudo apt upgrade upon first usage. In the notification from UserLAnd, be sure to enable "acquire wakelock".

```
sudo apt install wget && sudo apt install tmux && sudo apt install nano
```
### option 1A: if the command "dpkg --print-architecture" shows arm64 use this package
```
wget -O ~/packetcrypt https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/packetcrypt_aarch64_linux && chmod +x ~/packetcrypt
```
### option 1B: if the command "dpkg --print-architecture" shows armhf use this package
```
wget -O ~/packetcrypt https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/packetcrypt_armu_linux && chmod +x ~/packetcrypt
```
### Now continue, after getting the right package
```
wget -O ~/minepkt.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/mobile.sh && chmod +x ~/minepkt.sh
```

```
wget -O ~/pkttmuxmine.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/pkttmuxmine.sh && chmod +x ~/pkttmuxmine.sh
```

> nano ~/minepkt.sh **⚠️ edit to your personal pkt address ! ⚠️** 

> **⚠️ ! ON PHONES YOU SHOULD USE THE "-t 8" option and limit threads to about half of your available threads.
Edit, and try to find the sweet spot per phone. Performance is otherwise impacted greatly ! ⚠️**

> Hit CTRL + X To exit, "Y" to save when prompted.
 
> Done. See commands below.

Run the above commands in order to get the the aarch64 miner, bash file "minepkt.sh" & "pkttmuxmine.sh"

Stop the miner: "tmux attach-session -t miner" and hit CTRL + C

Start the miner: "~/pkttmuxmine.sh"

**Tmux session is called "miner"**

Show miner session:
```
tmux attach-session -t miner
```

Detatch from session with ctrl + shift + b, then release and hit "d" to detatch.

> Optionally, connect to your android phone over ssh with port 2022 and your set username/password.


## Cheers and have fun.

**📬Contact, questions, ideas, custom builds, general geeky-convos welcome:** 

> Siem🌻#4926 on the PKT Cash Discord: https://discord.gg/CkNJefwW52

> https://deNijs.xyz/

**💝If you're feeling especially kind or helped by my efforts to increase the PKT communities yield:**

>PKT: pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj

>PayPal: https://PayPal.me/SiemdeNijs
