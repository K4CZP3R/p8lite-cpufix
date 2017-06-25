p8lite-cpufix


CPU Fix for nougat based ROMs for Huawei P8 Lite.


To fix it, I needed to replace "0" to "0-7" to activate all cpu cores like this:
"""write /dev/cpuset/foreground/cpus 0-7
write /dev/cpuset/foreground/mems 0-7"""

