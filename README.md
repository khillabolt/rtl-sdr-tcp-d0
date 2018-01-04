# rtl-sdr-tcp-d0
init.d script to start/stop rtl_tcp as a service daemon (Debian9)

** Place script in `/etc/init.d/rtl-sdr-tcp-d0` **

Run
```
service "rtl-sdr-tcp-d0" start
systemctl daemon-reload
```
to verify service is running correctly:
```
service --status-all
```
## requirements
__package rtltcp__
http://osmocom.org/projects/sdr/wiki/rtl-sdr

Install the nessisary pre-requisites:

```
sudo apt-get update
sudo apt-get install cmake build-essential python-pip libusb-1.0-0-dev python-numpy git pandoc
```

Download, compile, and install rtl-sdr:

```
cd ~
git clone git://git.osmocom.org/rtl-sdr.git
cd rtl-sdr
mkdir build
cd build
cmake ../ -DINSTALL_UDEV_RULES=ON -DDETACH_KERNEL_DRIVER=ON
make
sudo make install
sudo ldconfig
```

### links to projects I used this service for

https://godoc.org/github.com/bemasher/rtltcp
https://github.com/bemasher/rtlamr