## TWRP device tree for OnePlus 5(cheeseburger)

Add to `.repo/local_manifests/cheeseburger.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/oneplus/cheeseburger" name="recovery_oneplus_cheeseburger" remote="antorya" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_cheeseburger-eng or lunch omni_cheeseburger-userdebug
make -j4 recoveryimage
```

Kernel sources are available at: https://github.com/Antorya/kernel_oneplus_msm8998