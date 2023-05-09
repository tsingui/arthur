u-uboot-2016 source code base on https://github.com/gl-inet/uboot-ipq60xx

## 1. build

```
cd u-boot-2016/
. ../env.sh

make ipq6018_defconfig
# make menuconfig
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

The uboot binary will be: u-boot-2016/u-boot.mbn
