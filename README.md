# rpi

> Instructions to setup my Raspberry Pi

---

## Step 1. Download [Raspbian](http://www.raspbian.org/) with pre-compiled [Jasper](http://jasperproject.github.io/)

I like [Raspbian](http://www.raspbian.org/) and [Jasper](http://jasperproject.github.io/).
You can [download the pre-compiled disk image of Jasper for Model B](http://sourceforge.net/projects/jasperproject/files/jasper-disk-image.tar.gz/download)

## Step 2. Install Raspbian Image to SD Card

### Get Disk Identifier of SD Card

![image](https://cloud.githubusercontent.com/assets/1885333/7262303/d5718bce-e84e-11e4-90a8-2e8e4114b930.png)

### Install Pipe Viewer (`pv`)

This will allow you to see progress of `dd`. 
See http://askubuntu.com/a/215590

#### Ubuntu

```bash
sudo apt-get install pv
```

#### Mac

```bash
brew install pv
```

### Image to SD Card

See https://www.raspberrypi.org/documentation/installation/installing-images/mac.md 
and http://askubuntu.com/a/215590

Use `pv` (Pipe Viewer) and `dd` to copy the Image to the SD card while showing progress.

- `image` - path to the image
- `diskn` - disk identifier

```bash
pv {image}.img | sudo dd of=/dev/{diskn} bs=1m
```

For example, my `image` is `./jasper-disk-image.img` and `diskn` is `disk2`.

```bash
pv ./jasper-disk-image.img | sudo dd of=/dev/disk2 bs=1m
```
