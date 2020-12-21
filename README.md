# Steps to take

1. Clean install of raspian
2. Set static ip address
3. confugure hostname
4. Install services

# Services

## Music

### Spotify connect

https://pimylifeup.com/raspberry-pi-spotify/

### Bluetooth

https://www.raspberrypi.org/forums/viewtopic.php?t=235519

### DIGI+ (HIFiBerry clone)

* Kernel > 4
https://www.hifiberry.com/docs/software/configuring-linux-3-18-x/

## PiHole

### Host setup

https://medium.com/swlh/how-to-set-up-pi-hole-2293246dc8ed

Assign static IP and hostname
```
sudo nano /etc/dhcpcd.conf
```

Enable SSH server in raspi-config

### PiHole setup

```
curl -sSL https://install.pi-hole.net | bash
```

* Ensure the password is recorded
* Manage logs (rotate and delete)
* Change DNS server on router to point to pihole
* May want to configure conditional forwarding under DNS section of GUI of pihole
