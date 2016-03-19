# cgminer 3.7.2 DCR Mods For ZTEX-15y1 FPGA

These modifications will allow you to use the Decred cgminer v0.0.5 with a ztex-15y1 fpga.  Below are the steps I used to get the miner running on my Raspberry Pi.

  <li>sudo apt-get update
  sudo apt-get install libusb-1.0-0-dev libusb-1.0-0 libcurl4-openssl-dev libncurses5-dev libudev-dev screen libtool automake pkg-config libjansson-dev
  git clone https://github.com/decred/cgminer
  cd cgminer
  sudo ./autogen.sh
  sudo ./configure --disable-adl --enable-icarus
  copy .c and .h files to cgminer directory
  copy .bit to cgminer\bitstreams
  sudo make
  New Command Line: cgminer --disable-gpu --blake256 -o <pool url : port> -u <username> -p <password> --verbose --ztex-clock 100:100</li>
 
Note: This miner only works on Getwork pools.  It does not have the Stratum logic incorporated yet.

<b>Issue: This miner seems to work fine for up to 4 ztex boards.  More than 4 boards is causing the cgminer to crash after 10 minutes.</b>
 
