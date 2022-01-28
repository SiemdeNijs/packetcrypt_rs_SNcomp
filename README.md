# SNcomp version of packetcrypt_rs annminer
These packetcrypt miners are pre-compiled by Siem, with custom flags and tinkering. Use at your own risk. 
No warranty. No support.

* include jemalloc flag for supported devices
* upward to ~50% performance gains vs packetcrypt_rs pre-compiled miners
(highest increasements seen by EPYC, 5950x, Intel E-series users)
* different compiling workflow to achieve a more stable experience (hopefully)
* will be tinkered with in future releases for more custom optimizations
 
Wish to compile it yourself instead ? 
The most convential way is described in detail here for WSL/Linux: https://denijs.photography/pkt-how-to-install-wsl-compile-miner

Request can be made through PKT Cash's Discord, hit me up there if you need it compiled for a specific target.

### ⛏️ Usage:
1 Rename the file to "packetcrypt".

2 Use the miner command's as usual:
Linux
> /path/to//packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
Windows

> /path/to//packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in

**⚠️Replace the "pkt1......" address with your address⚠️**

### 👾 Optional one click run for Windows, WSL or systemd service (Linux):

**🪟 Windows native (running .exe directly on windows machine):**

>  1 Open notepad

>  2 Copy this: "/path/to//packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in"

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run our miner.
 
**🪟🐧 Windows WSL:**

>  1 Open notepad

>  2 Copy this: "wsl /path/to//packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in"

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run our miner.

**🐧 Linux native:**

> wget -O /etc/systemd/system/pkt.service https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/pkt.service
 
> wget -O ~/packetcrypt https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/packetcrypt_amd64_linux && sudo chmod +x ~/packetcrypt

> wget -O ~/minepkt.sh https://github.com/SiemdeNijs/packetcrypt_rs_SNcomp/releases/download/release/minepkt.sh && sudo chmod +x ~/minepkt.sh

> sudo nano ~/minepkt.sh **⚠️ edit to your personal pkt address ! ⚠️**. Hit CTRL + X To exit, "Y" to save when prompted.

> sudo systemctl enable pkt **⚠️only if you want to autorun it on boot, else ignore this command⚠️**

> Done. See commands below.

Run the above commands in order to get the the linux miner (amd64), bash file "minepkt.sh" , & "pkt.service".
**⚠️Be sure to type: "sudo nano ~/minepkt.sh" as mentioned above to change your address⚠️**

Enable/Disable autorun: "systemctl enable pkt" or "systemctl disable pkt"

Stop the miner: "systemctl stop pkt"

Start the miner: "systemctl start pkt"

Status of the miner: "systemctl status pkt"


Cheers and have fun.
### -Siem

**📬Contact, questions, ideas, custom builds, general geeky-convos welcome:** 

> Siem🌻#4926 on the PKT Cash Discord: https://discord.gg/CkNJefwW52

> https://deNijs.xyz/

**💝If you're feeling especially kind or helped by my efforts to increase the PKT communities yield:**

>PKT: pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj

>PayPal: https://PayPal.me/SiemdeNijs
