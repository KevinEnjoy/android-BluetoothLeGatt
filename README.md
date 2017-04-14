
Android BluetoothLeGatt Sample
===================================

This sample demonstrates how to use the Bluetooth LE Generic Attribute Profile (GATT)
to transmit arbitrary data between devices.

Introduction
------------

This sample shows a list of available Bluetooth LE devices and provides
an interface to connect, display data and display GATT services and
characteristics supported by the devices.

It creates a [Service][1] for managing connection and data communication with a GATT server
hosted on a given Bluetooth LE device.

The Activities communicate with the Service, which in turn interacts with the [Bluetooth LE API][2].

[1]:http://developer.android.com/reference/android/app/Service.html
[2]:https://developer.android.com/reference/android/bluetooth/BluetoothGatt.html

Pre-requisites
--------------

- Android SDK 25
- Android Build Tools v25.0.2
- Android Support Repository

Screenshots
-------------

<img src="screenshots/1-main.png" height="400" alt="Screenshot"/> <img src="screenshots/2-detail.png" height="400" alt="Screenshot"/> 

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

修改内容
---------------
1. ListView的样式
2. 显示收数据的时间戳
3. 对于`写服务`，点击特征值，会写入值： `android ping ble.`
4. 在小米手机发生的启动失败问题（其他手机和模拟器都没问题），加上全路径等都无法解决。应该是项目环境的问题，代码是没问题的。错误信息如下：
```
java.lang.RuntimeException: Unable to instantiate activity ComponentInfo{com.example.android.bluetoothlegatt/com.example.android.bluetoothlegatt.DeviceScanActivity}: java.lang.ClassNotFoundException: Didn't find class "com.example.android.bluetoothlegatt.DeviceScanActivity" on path: DexPathList[[zip file "/data/app/com.example.android.bluetoothlegatt-2/base.apk"],nativeLibraryDirectories=[/data/app/com.example.android.bluetoothlegatt-2/lib/arm64, /vendor/lib64, /system/lib64]]
	at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2334)
	at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:2483)
	at android.app.ActivityThread.access$900(ActivityThread.java:153)
	at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1349)
	at android.os.Handler.dispatchMessage(Handler.java:102)
	at android.os.Looper.loop(Looper.java:148)
	at android.app.ActivityThread.main(ActivityThread.java:5441)
	at java.lang.reflect.Method.invoke(Native Method)
	at com.android.internal.os.ZygoteInit$MethodAndArgsCaller.run(ZygoteInit.java:738)
	at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:628)
Caused by: java.lang.ClassNotFoundException: Didn't find class "com.example.android.bluetoothlegatt.DeviceScanActivity" on path: DexPathList[[zip file "/data/app/com.example.android.bluetoothlegatt-2/base.apk"],nativeLibraryDirectories=[/data/app/com.example.android.bluetoothlegatt-2/lib/arm64, /vendor/lib64, /system/lib64]]
	at dalvik.system.BaseDexClassLoader.findClass(BaseDexClassLoader.java:56)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:511)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:469)
	at android.app.Instrumentation.newActivity(Instrumentation.java:1068)
	at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2324)
	... 9 more
	Suppressed: java.lang.ClassNotFoundException: com.example.android.bluetoothlegatt.DeviceScanActivity
		at java.lang.Class.classForName(Native Method)
		at java.lang.BootClassLoader.findClass(ClassLoader.java:781)
		at java.lang.BootClassLoader.loadClass(ClassLoader.java:841)
		at java.lang.ClassLoader.loadClass(ClassLoader.java:504)
		... 12 more
	Caused by: java.lang.NoClassDefFoundError: Class not found using the boot class loader; no stack trace available

```

Support
-------

- Google+ Community: https://plus.google.com/communities/105153134372062985968
- Stack Overflow: http://stackoverflow.com/questions/tagged/android

If you've found an error in this sample, please file an issue:
https://github.com/googlesamples/android-BluetoothLeGatt

Patches are encouraged, and may be submitted by forking this project and
submitting a pull request through GitHub. Please see CONTRIBUTING.md for more details.

License
-------

Copyright 2016 The Android Open Source Project, Inc.

Licensed to the Apache Software Foundation (ASF) under one or more contributor
license agreements.  See the NOTICE file distributed with this work for
additional information regarding copyright ownership.  The ASF licenses this
file to you under the Apache License, Version 2.0 (the "License"); you may not
use this file except in compliance with the License.  You may obtain a copy of
the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  See the
License for the specific language governing permissions and limitations under
the License.
