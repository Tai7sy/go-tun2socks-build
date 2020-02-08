# go-tun2socks-build

Building and using `go-tun2socks` for V2Ray on Android. This library is used in [kitsunebi-android](https://github.com/Tai7sy/kitsunebi-android) for support V2Ray.

## Setup

* install go (only test under version 1.13.5)
* install gomobile and init with `gomobile init -v`
* Download Android SDK and NDK (only test under SDK 29 and NDK r20b)


## Build
```bash
export http_proxy=http://127.0.0.1:10809
export https_proxy=http://127.0.0.1:10809
export ANDROID_HOME=/path/to/Android/Sdk
export ANDROID_NDK_HOME=/path/to/Android/android-ndk-r20b

git config --global url."git@github.com:Tai7sy/v2ray-core.git".insteadOf "https://github.com/Tai7sy/v2ray-core.git"
go get -d ./...

# Build an AAR
make android

# Build a Framework (not test)
make ios

# Both
make
```
