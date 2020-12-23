# Steps to take

1. Clean install of raspberry OS
2. Set static ip address at router
3. confugure hostname
4. Install services

# Setup

Run
```
sudo raspi-config
```

* Enable i2c in peripherals (I think this may be necessary for digi+)
* Set timezone and locale
* Change hostname
* Change password
* Enable ssh
* Reboot

Generate keys for ssh

# Services

## Music

### Spotify connect

https://pimylifeup.com/raspberry-pi-spotify/

### Bluetooth

https://www.raspberrypi.org/forums/viewtopic.php?t=235519

### DIGI+ (HIFiBerry clone)

* Kernel > 4 https://www.hifiberry.com/docs/software/configuring-linux-3-18-x/

## PiHole

```
curl -sSL https://install.pi-hole.net | bash
```

* Ensure the password is recorded
* Manage logs (rotate and delete)
* Change DNS server on router to point to pihole
* May want to configure conditional forwarding under DNS section of GUI of pihole
