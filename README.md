# icloud-bypass-2.0
all developments will be add here and http://idevicetool.eu ( colab web ) educational purposes

This is a guide to compiling iDeviceRestore by @p0sixninja on debian linux. It has been tested on Ubuntu 12.04 (and even the raspberry pi on raspbian!) and is working.

Do any required upgrades on apt.
sudo apt-get update
sudo apt-get upgrade
First, we need to get the dependencies
sudo apt-get install build-essential automake cmake \
libreadline6 autotools-dev libcurl4-openssl-dev autoconf \
libplist1 libplist-utils libplist-dev libplist++-dev \
libzip-dev git curl libgnutls-dev libreadline-dev libusb-dev \
libtool libusb-1.0-0-dev libusbmuxd-dev libglib2.0-dev libimobiledevice-dev
 
Install libirecovery
mkdir ~/idevicerestore
cd ~/idevicerestore
git clone http://git.sukimashita.com/libirecovery.git
cd libirecovery
./autogen.sh
make && sudo make install
Finally to get idevicerestore
cd ~/idevicerestore
git clone git://github.com/tcf38012/idevicerestore.git
cd idevicerestore
./autogen.sh
make && sudo make install
sudo ldconfig
Also, you might want iDeviceactivate, to activate after you have restored
cd ~/idevicerestore
git clone http://github.com/posixninja/ideviceactivate.git
cd ideviceactivate
make

http://idevicetool.eu
