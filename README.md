# LineageOS for the AGM M7

Local manifest for LineageOS 24.0 on the AGM M7 (MT6739) with a mainline kernel.

| Path | Repository |
|---|---|
| `device/agm/m7` | [android_device_agm_m7](https://github.com/itsvic-dev/android_device_agm_m7) |
| `kernel/agm/m7` | [linux-mt6739](https://github.com/itsvic-dev/linux-mt6739) (`linux-7.2`) |
| `vendor/agm/m7` | [agm-m7-firmware](https://github.com/itsvic-dev/agm-m7-firmware) |
| `external/ccci-fsd` | [ccci-fsd](https://github.com/itsvic-dev/ccci-fsd) |
| `external/mesa` | [mesa](https://github.com/itsvic-dev/mesa) (`agm-m7-android`) |

The other projects are the LineageOS mainline device support.

## Build

```
repo init -u https://github.com/LineageOS/android.git -b lineage-24.0 --git-lfs
git clone https://github.com/itsvic-dev/android_local_manifests_agm_m7 .repo/local_manifests
repo sync
source build/envsetup.sh
lunch lineage_m7-cp2a-userdebug
m bootimage recoveryimage superimage
```

Flashing and the boot layout: [nixos-agm-m7](https://github.com/itsvic-dev/nixos-agm-m7).
