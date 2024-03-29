libzxing
========

A portable android studio library for zxing. This is a port of [zxing-android-minimal](https://github.com/embarkmobile/zxing-android-minimal)

Howto
-----
To use libzxing, put the following to your settings.gradle: (You should have created a android studio project before)

```
include ':libzxing:zxing-integration', ':libzxing:zxing-android', ':libzxing:zxing-android-legacy'
```


Then add the following denpendencies to your build.gradle:

```
dependencies {
    // Supports Android 4.0.3 and later (API level 15)
    compile project(':libzxing:zxing-android')

    // Supports Android 2.1 and later (API level 7), but not optimal for later Android versions.
    // If you only plan on supporting Android 4.0.3 and up, you don't need to include this.
    compile project(':libzxing:zxing-android-legacy')

    // Convenience library to launch the scanning and encoding Activities.
    // It automatically picks the best scanning library from the above two, depending on the
    // Android version and what is available.
    compile project(':libzxing:zxing-integration')
}
```


To run the zxing-samples, add the following to your setting.gradle

```
include ':libzxing:zxing-samples'
```

Usage
-----
See [zxing-android-minimal](https://github.com/embarkmobile/zxing-android-minimal) for details.
