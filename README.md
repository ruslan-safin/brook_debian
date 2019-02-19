# README

## What is Brook

Brook is a cross-platform proxy/vpn software.

Brook's goal is to keep it simple, stupid and not detectable.

## Version 19.02.18


## How do I get set up?

1. First step - download latest binary from [https://github.com/txthinking/brook](https://github.com/txthinking/brook/releases/)
1. Place downloaded binary to `/opt/brook` directory 
1. Change execution permission `chmod +x brook`
1. If you prefer use network port number smaller than 1024 `setcap CAP_NET_BIND_SERVICE=+eip /opt/brook/brook`
1. Copy `brook.service` file to `/lib/systemd/system/brook.service`
2. Copy `start.sh` file to `/opt/brook/start.sh`
3. Change execution permission `chmod +x start.sh`
1. Edit `StrongPass` to change password, `-l :443`to change listening port number, `--username user` to change username for socks5 connection in `start.sh` file
1. Enable service `systemctl enable brook`
1. Run service `systemctl start brook`
1. Verify starting service `systemctl status brook`
1. Check service `netstat -tulpan | grep brook`

Connect to Internet, enjoy

Who do I talk to?

Repo owner CyberManiac
