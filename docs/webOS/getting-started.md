---
layout: default
title: 시작하기
parent: webOS
nav_order: 1
---

# 시작하기
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 우선 해보자
webOS에 대해 잘 몰라도 우선 시작해볼 수 있다.<br>
build 환경이 없어도 release 되는 이미지를 다운로드 받아서 해볼 수 있으며,<br>
Raspberry Pi 4 와 같은 device가 없어도 emulator로 실행해 볼 수 있다.<br>
* 이미지 다운로드 : [http://build.webos-ports.org/webosose/](http://build.webos-ports.org/webosose/)
* 에뮬레이터 설정 : [https://www.webosose.org/docs/tools/sdk/emulator/virtualbox-emulator/emulator-user-guide/](https://www.webosose.org/docs/tools/sdk/emulator/virtualbox-emulator/emulator-user-guide/)

에뮬레이터로 실행하면 아래와 같이 실행되는 것을 확인할 수 있고,<br>
Web Browser와 Youtube 를 실행해 볼 수 있다.<br>
<br>
<small>* 아래의 이미지는 webos-image-qemux86-master-20200528044350.wic.vmdk 버전으로 실행한 결과</small>
![](./vbox_emulator_image.jpg)

## build
이미지 빌드를 위해 개발환경을 설정하고 빌드를 해보자.<br>
* 참고 : [https://www.webosose.org/docs/guides/setup/building-webos-ose/](https://www.webosose.org/docs/guides/setup/building-webos-ose/)
local pc에 ubuntu 18.04 LTS를 설치하거나, 학교나 회사에 서버가 있다면 계정을 하나 받아서 사용하면 된다.<br>
난 학교에서 계정을 하나 받았으므로...<br>

```
# build 소스 받기
$ git clone https://github.com/webosose/build-webos.git
$ cd build-webos

# 필요한 package 설치하기
$ sudo scripts/prerequisites.sh

# Configuring the Build for the Target Device

$ ./mcf -p 4 -b 4 qemux86 (emulator)
$ ./mcf -p 4 -b 4 raspberrypi4 (for webOS OSE 2.0 or higher)

# Build the Image
$ make webos-image
```

역시 한방에는 안된다.<br>

```
ERROR: The following required tools (as specified by HOSTTOOLS) appear to be unavailable iease install them in order to proceed:
  chrpath makeinfo
```

이런 경우 아래와 같이 2개의 package를 추가로 설치해줘야 한다.

```
sudo apt install chrpath texinfo
```
build 중.....<br>
