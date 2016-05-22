# cgminer 3.7.2 DCR Mods For ZTEX-1.15y FPGA

These modifications will allow you to use the Decred cgminer v0.0.5 with a ztex-1.15y fpga.  Also, support has been added for simple serial FPGA boards such as the BeMicroCVA9 ( or any other single chip FPGA using serial comms ).

Below are the steps I used to get the miner running on my Raspberry Pi.
<ul>
<li>sudo apt-get update</li>
<li>sudo apt-get install libusb-1.0-0-dev libusb-1.0-0 libcurl4-openssl-dev libncurses5-dev libudev-dev screen libtool automake pkg-config libjansson-dev</li>
<li>git clone https://github.com/decred/cgminer</li>
<li>cd cgminer</li>
<li>sudo ./autogen.sh</li>
<li>sudo ./configure --disable-adl --enable-icarus</li>
<li>copy .c and .h files to cgminer directory</li>
<li>copy .bit & .bin to cgminer\bitstreams</li>
<li>make</li>
</ul>

To run the Miner (ZTEX)

    sudo ./cgminer --disable-gpu --blake256 -o < url:port > -u < username > -p < password > --ztex-clock 116:116 --scan-time 6 --queue 4

To run the Miner (Serial FPGA)

    sudo ./cgminer --disable-gpu --blake256 -o < url:port > -u < username > -p < password > -S /dev/ttyUSB0 --scan-time 6 --queue 4
    
Note: This miner only works on Getwork pools.  It does not have the Stratum logic incorporated yet.

Also, I have posted the link to a ztex-1.15y DCR bistream in this github, it gets about 1Gh/s.

________________________________________________________________________________________________

BTC: 14QcqFWZ9Y1j1aUHeUNySoMr4t9ZWJYt2a

DCR: Dsj6WcnPYDPxDr99pQkTKeFsfh55KBJS2jY


 
