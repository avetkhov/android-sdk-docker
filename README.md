# Android SDK Docker

[![build](https://github.com/avetkhov/android-sdk-docker/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/avetkhov/android-sdk-docker/actions/workflows/build.yml)
![Docker Image Version (latest semver)](https://img.shields.io/docker/v/avetkhov/android-sdk?sort=semver&logo=docker&logoColor=white&label=version)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/avetkhov/android-sdk/tools?logo=docker&logoColor=white&label=tools%20size)
![Docker Image Size (latest semver)](https://img.shields.io/docker/image-size/avetkhov/android-sdk?logo=docker&logoColor=white&label=sdk%20size)
![Docker Pulls](https://img.shields.io/docker/pulls/avetkhov/android-sdk?logo=docker&logoColor=white&label=pulls)
![Docker Stars](https://img.shields.io/docker/stars/avetkhov/android-sdk?logo=docker&logoColor=white&label=stars)


## What is Android SDK?

The Android SDK (software development kit) is a set of development tools used to develop applications for the Android platform.

[developer.android](https://developer.android.com)

<img src="https://developer.android.com/static/images/brand/Android_Robot.png" width="400">

## How to use this image

The docker image with `tools` tag with preinstalled Android SDK Command-line tools. The `sdkmanager` is a command-line tool that lets you view, install, update, and uninstall packages for the Android SDK.
```
docker run -t --rm avetkhov/android-sdk:tools sdkmanager --list
```
The docker image with `X` tag with preinstalled Android SDK Platform, Platform-Tools, Build-Tools and Tools.
* The `platform` package is required to compile your app for that version;
* The `platform-tools` is a component for the Android SDK. It includes tools that interface with the Android platform, primarily `adb` and `fastboot`;
* The `build-tools` is a component of the Android SDK required for building Android apps;
* The `tools` is a component for the Android SDK. It includes development and debugging tools for Android.

To display installed packages use
```
docker run -t --rm avetkhov/android-sdk:X sdkmanager --list
```

## License

Android SDK is licensed under [Android Software Development Kit License Agreement][1].

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.

[1]: https://github.com/flutter/flutter/blob/master/LICENSE](https://developer.android.com/studio/terms