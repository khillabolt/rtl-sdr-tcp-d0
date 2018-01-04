# rtl-sdr-tcp-d0
init.d script to start/stop rtl_tcp as a service daemon (Debian9)

** Place script in `/etc/init.d/rtl-sdr-tcp-d0` **

Run

`
service "rtl-sdr-tcp-d0" start
systemctl daemon-reload
`
to verify service is running correctly

`
service --status-all
`
## requirements
__package rtltcp__
http://osmocom.org/projects/sdr/wiki/rtl-sdr

### links to project I used this for
https://godoc.org/github.com/bemasher/rtltcp
https://github.com/bemasher/rtlamr