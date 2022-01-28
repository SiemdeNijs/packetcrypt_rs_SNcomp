# SNcomp version of packetcrypt_rs packetcrypt miner [v0.1] Latest
These packetcrypt miners are pre-compiled by Siem, with custom flags and tinkering. Use at your own risk. No warranty. No support.
* include jemalloc flag for supported devices
* upward to ~50% performance gains vs packetcrypt_rs pre-compiled miners
(highest increasements seen by EPYC, 5950x, Intel E-series users)
* different compiling workflow to achieve a more stable experience (hopefully)
* will be tinkered with in future releases for more custom optimizations

Look for the version which fits your system. No other packages available at the moment.

Request can be made through PKT Cash's Discord, hit me up there if you need it compiled for a specific target.

### Usage:
1 Rename the file to "packetcrypt"

2 Use the miner as usual:

Linux

> /path/to//packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in

Windows

> /path/to//packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in

**Replace the "pkt1......" address with your address.**

### Usage:
1 Rename the file to "packetcrypt".

2 Use the miner command's as usual:
Linux
> /path/to//packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in
Windows

> /path/to//packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in

**Replace the "pkt1......" address with your address.**

### Optional one click run for Windows / systemd service (Linux):

**Windows native (running .exe directly on windows machine):**

>  1 Open notepad

>  2 Copy this: "/path/to//packetcrypt.exe ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in"

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run our miner.
 
**Windows WSL:**

>  1 Open notepad

>  2 Copy this: "wsl /path/to//packetcrypt ann -p pkt1qc4l3wgtkx3t4qez6pun5k73cktcdczkqqutwnj http://pool.pkt.world/master/2048 http://pool.pktpool.io http://pool.pkteer.com http://pktco.in"

>  3: Change the /path/to, to the actual path. Change it to your address. Optionally add "-t *number*" to limit the threads used.

>  4: Click "Save as", and select "all files" instead of the ".txt" extension. As a name, name it "whatever" but be sure to end it with "**.cmd**".

>  5: if successfully saved, you can now double click the icon to run our miner.

**Linux native:**


Run the above commands to get the the linux miner (amd64), bash file "minepkt.sh" , & "pkt.service". It will also try to enable the systemd service (so it runs on boot). You can disable this behavior by typing: "sudo systemctl disable pkt".

**Be sure to type: "sudo nano ~/minepkt.sh" after installation and change your address !**

Stop the miner: "systemctl stop pkt"
Start the miner: "systemctl start pkt"
Status of the miner: "systemctl status pkt"
Place the minepkt.sh anywhere you'd like. In this example: /home/username/minepkt.sh
