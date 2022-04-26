**Building Linux kernel with modules:**

Mandatory options to export:

Depending on your HW `TARGET_BOARD_PLATFORM=r8a779[5,6]`

`BUILD_CONFIG=common/build.config.xenvm`


Optional options:

`SKIP_DEFCONFIG=1` - skip defconfig stage

`SKIP_MRPROPER=1` - skip mrproper stage

`EXT_MODULES=imagination` - to build closed source PVR kernel driver

```
repo init -u https://github.com/arminn/android_kernel_manifest -b common-android12-5.4-xt-master -g all
repo sync -c
./build/build.sh
```

Built products could be found at `out/android12-5.4/dist`
