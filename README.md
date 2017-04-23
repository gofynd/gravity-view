# Gravity View for Android

[![API](https://img.shields.io/badge/API-11%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=11) [![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Gravity%20View-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/5477)

Gravity View is an Android adaptation of Facebook instant articles. The concept behind the library is to utilize the motion sensors of an Android device and allow the end user to explore the product by rotating his device. It uses gyroscope motion sensor readings to scroll the image.

You can read more about Gravity View article [here](https://blog.gofynd.com/introducing-gravity-because-swiping-is-so-yesterday-4aebd89f0e21)


[![Gravity View video](http://img.youtube.com/vi/IrNr-J1s8f8/0.jpg)](http://www.youtube.com/watch?v=IrNr-J1s8f8)

## Demo

Install [Demo](https://github.com/gofynd/gravity-view/releases/download/v1.0/gravityview-1.0.apk) app or APK from [Releases](https://github.com/gofynd/gravity-view/releases) on your device and experience the gravity view.

### Requirements
  - Android 3.0 or higher

## Usage
### Gradle dependency

```
dependencies {
    compile 'co.gofynd.library:gravity-view:1.0'
}
```

### Sample Code:

#### Inside Layout XML File:

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/activity_main"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">
    <HorizontalScrollView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:scrollbars="none">
        <ImageView
            android:id="@+id/bg"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />
    </HorizontalScrollView>
</RelativeLayout>
```

#### Inside Activity or Fragment:

```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        gravityView = GravityView.getInstance(this)
                .setImage(bg, R.drawable.landingbg)
                .center();
    }
    @Override
    protected void onResume() {
        super.onResume();
        gravityView.registerListener();
    }
    @Override
    protected void onStop() {
        super.onStop();
        gravityView.unRegisterListener();
    }
```

### Check if device is supported:

```
boolean is_supported = gravityView.deviceSupported();
```

## Roadmap

- Multiple image support
- Support for Non-Gyroscope devices using Accelerometer sensor

## Contributions

Any contributions are welcome!
Please check the [contributing guideline](https://github.com/gofynd/gravity-view/blob/master/CONTRIBUTING.md) before submitting a new issue.


## Developed By

* Fahim Sakri


## License
    Copyright 2017 Shopsense Retail Technologies Pvt Ltd.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
