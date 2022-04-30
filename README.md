# obs-nvidia-low-latency-setup

```nvidia-smi```

if that shows 510.60.02 then you can use this script.
else, do not use this script.
```sudo pacman -S obs-studio
git clone https://github.com/keylase/nvidia-patch
cd nvidia-patch
./patch.sh
./patch-fbc.sh
sed -i 's/\xc7\x84\x24\xfc\x01\x00\x00\x00\x00\x40\x00/\xc7\x84\x24\xfc\x01\x00\x00\x00\x10\x40\x00/' "/usr/lib64/libnvidia-fbc.so.510.60.02"
yay -s obs-nvfbc v4l2loopback-dkms```
