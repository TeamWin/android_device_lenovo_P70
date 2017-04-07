## TWRP device tree for Lenovo P70-A

Add to `.repo/local_manifests/P70.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<manifest>
	<project path="device/lenovo/P70" name="ccsysadmin/android_device_lenovo_P70-TWRP" remote="github" revision="android-5.1" />
</manifest>
```

Then run `repo sync` to check it out.

To build:

```sh
. build/envsetup.sh
lunch omni_p70-eng
make -j 9 recoveryimage
```