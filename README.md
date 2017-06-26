# Huawei P8 Lite Nougat CPU fix

This repo contains edited ramdisk files (Thanks @OpenKirin!) which are fixing cpu issue on nougats 
ROMs (LineageOS and Resurrection Remix)

### Changes

Two files are edited: init.hi6210sft.power.rc and init.rc / Thanks for it @dominj97

init.hi6210sft.power.rc:
```
#before
write /dev/cpuset/foreground/cpus 0
write /dev/cpuset/foreground/boost/cpus 0
write /dev/cpuset/background/cpus 0
write /dev/cpuset/system-background/cpus 0

#after
write /dev/cpuset/foreground/cpus 0-7
write /dev/cpuset/foreground/boost/cpus 0-7
write /dev/cpuset/background/cpus 0-7
write /dev/cpuset/system-background/cpus 0-7
```

There are almost the same changes in init.rc.

Here some screenshots and video from a game:
![Antutu benchmark on RROS](https://user-images.githubusercontent.com/16763276/27516953-c6de0e96-59c3-11e7-9160-76fca0f16dea.png)
![Antutu benchmark on LOS](https://user-images.githubusercontent.com/16763276/27516954-cd8d1a7a-59c3-11e7-9013-147d9ce25008.png)
https://drive.google.com/file/d/0B-5Wqqs1Gx_od0xNZHhoRVg5X1k/view Real Racing 3 after CPU Fix
