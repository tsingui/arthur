## 1. build

```
cd uboot-ipq60xx/
. ../env.sh

make ipq6018_defconfig
make menuconfig
make V=s
```

## 2. strip elf
```
arm-openwrt-linux-strip u-boot
```

## 3. convert elf to mbn

```
python2.7 scripts_mbn/elftombn.py -f ./u-boot -o ./u-boot.mbn -v 6
```