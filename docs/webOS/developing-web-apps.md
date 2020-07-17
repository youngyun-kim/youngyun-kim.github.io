---
layout: default
title: 앱만들기
parent: webOS
nav_order: 2
---

# 앱만들기
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## 앱 만들기
webOS 앱을 만들어보자.<br>
우선 아래의 가이드에 따라서 CLI 설치 및 환경설정 추가.<br>
* 환경설정 : [https://www.webosose.org/docs/tutorials/web-apps/developing-external-web-apps/](https://www.webosose.org/docs/tutorials/web-apps/developing-external-web-apps/)
<br>
아래의 명령어를 그냥 윈도우 터미널에서 실행하면 error가 발생한다.<br>

```
D:\> ares-generate -t webapp sampleApp
? app id com.domain.app
? title new app
? version 1.0.0
ares-generate ERR! ares-generate: Error: 'git' command is not available on this machine.
```

ares-generate 를 실행하면 git에서 sample source를 가져오는 것 같다.<br>
그래서 윈도우용 git을 설치하였다. <br>
* git download : [https://git-scm.com/downloads](https://git-scm.com/downloads)

