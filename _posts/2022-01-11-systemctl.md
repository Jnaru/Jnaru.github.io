---
title: Systemctl
categories:
  - Linux
tags:
  - Linux
toc: true
toc_sticky: true
---

## - systemctl이란?

- systemd를 관리하는 명령어

- /usr/lib/systemd/system의 .service 파일을 systemctl 명령을 통해 제어할 수 있다



## - systemd 서비스 파일 구성

| [Unit]<br/>Dscription= ** service<br/>After=**.target<br/>Requires=**_service<br/><br/>[Service]<br/>ExecStart=/usr/bin/env php /path/to.server.php<br/><br/>[Install]<br/>WantedBy=multi-user.target |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

- 위가 기본적인 서비스 파일의 구성 형태

- [Unit]에서 Dscription은 현재 해당하는 서비스에 대한 설명, After는 After에 오는 Service 이후 현재 서비스가 실행된다는 것을 말하고, Requires는 현재 서비스를 실행하기 위한 상위 의존성 서비스에 대해 기재한다.

- [Service]는 서비스가 어떻게 실행될 것인지 정의, ExecStart는 서비스의 실행 경로를 가지고 있음, 이외에도 유닛의 타입을 설정하거나,  시작/중지/조작 등 서비스에 대한 전반적인 설정을 할 수 잇다.

- [Install]섹션은 서비스를 등록/해제 할때 사용하는 설정값이다. Alias / WantedBy, RequiredBy / Also가 있고 각각 유닛의 별칭을 지정하거나, 유닛 등록시 필요한 유닛을 지정하거나, 해당 유닛을 등록할때 같이 등록할 유닛을 설정하거나 할 수 있다



## - Systemd 유닛 컨트롤 명령어

- systemctl start <unit> : 유닛 활성화

- systemctl stop <unit> : 유닛 비활성화

- systemctl restart <unit> : 유닛을 종료 후 재활성화

- systemctl enable <unit> : 유닛 등록

-  systemctl disable <unit> : 유닛 등록 해제

- systemctl enable --now <unit> : 유닛 등록 후 바로 활성화


