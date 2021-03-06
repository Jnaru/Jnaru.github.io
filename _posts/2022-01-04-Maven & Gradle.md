---
title: Maven과 Gradle
categories:
  - Spring
tags:
  - Spring
toc: true
toc_sticky: true
---

# - Maven & Gradle

## - Maven

- 프로젝트의 전체적인 라이프 사이클을 관리하는 도구

- 외부에서 필요한 라이브러리와 플로그인들을 다운로드해서, 로컬 시스템의 캐시에 모두 저장한다.

- pom.xml을 사용하며 이 파일은 프로젝트 정보, 빌드 설정, 빌드 환경 등 다양한 정보를 담고 있다.

## - Gradle

- 빌드 배포 도구이며, 구글의 안드로이드 공식 빌드시스템, JAVA, C/C++, Python 등을 지원한다.

- maven과 다를게 Groovy 언어 기반의 빌드스크립트를 활용해서 어플리케이션, 라이브러리 관리 등이 가능하다.

- xml의 구조를 벗어나 변수선언, 조건문 사용 등으로 간결한 정의가 가능

- Maven, Ivy등으로 만들어진 프로젝트에 대해 간편한 Migration 제공

  

## - Gradle, Maven 차이점

| Gradle                                                                                          | Maven                                   |
|:----------------------------------------------------------------------------------------------- | --------------------------------------- |
| -  빌드 자동화 시스템                                                                                   | - 프로젝트 라이프 사이클 관리 도구                    |
| - Groovy 기반 DSL(도메인 특정 언어)를 <br/>사용하는 빌드 스크립트 사용해 <br/>프로젝트, 라이브러리, 필수 플러그인 등을 관리               | - xml을 이용하여 프로젝트, 라이브러리, 필수 플러그인 등을 관리  |
| - 작업 종속성 그래프를 기반                                                                                | - 고정적, 선형적 단계의 모델을 기반                   |
| - Task의 업데이트 확인을 함으로 <br/>Incremental Build 허용, 업데이트된 내용에 대해서 작업이 실행되지 않음으로 빌드 시간이 maven에 비해 단축 | - 업데이트 내용 확인을 못함으로 빌드 시간이 Gradle에 비해 느림 |

## - 결론

Maven은 여전히 Gradle에 비해 많은 사용자수와 사용 빈도를 가지고 있지만, Gradle이 Maven과 Ant의 장점을 모아서 만들어진 만큼 편리한 부분들이 많기 때문에 추후 점점 Gradle이 더 폭 넓게 사용될것으로 보인다.

Maven 프로젝트에서 Migration도 지원하고 있으므로 가능하면 Gradle로 넘어가는것이 차후를 위해서 도움이 될 것으로 보임
