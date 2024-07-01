# CAUSW Backend

<!--
<a href="https://spring.io">
  <img src="https://img.shields.io/badge/spring-v2.4.1-green">
</a>
<a href="https://www.oracle.com/java/technologies/javase/11-0-9-relnotes.html">
  <img src="https://img.shields.io/badge/jdk-v11.0.9-blue">
</a>
<a href="https://github.com/CAUCSE/CAUSW_backend/actions">
  <img src="https://github.com/CAUCSE/CAUSW_backend/actions/workflows/ci.yml/badge.svg">
</a>

## Overview

해당 애플리케이션은 [중앙대학교 소프트웨어학부 동문네트워크 커뮤니티](https://causw.net) 서비스의 Backend 서비스를 구동합니다.

서비스 이용 중 불편한 사항 혹은 문의사항이 있으신 경우 개발팀에 연락 부탁드리며, 서비스 개선을 위한 다양한 의견은 언제든 환영입니다.

프로젝트에 참여하시고 싶으시다면, [Contributing Guide](CONTRIBUTING.md)를 참조하시어 issue 혹은 pull request를 생성해주세요!

본 서비스에 많은 관심 부탁드립니다 :)

## Architecture

해당 애플리케이션는 <a href="https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)">Hexagonal Architecture</a>를 따른다.

### Hexagonal Architecture

- 계층 구조(Layered Architecture) 의 대안으로써 사용자 인터페이스나 기반 요소(Infrastructure) 의 변경에 영향을 받지 않는 핵심 코드, 즉 비즈니스 로직을 만들고 이를 견고하게
  관리하기 위한 구조
- Ports and Adapters Architecture 라고 불리기도 함

<p align="center">
    <img src="./img/project_structure.png" width="600" height="266"/>
</p>

> 육각형 구조의 핵심은 비즈니스 로직이 다른 기술 영역의 영향을 받게 하지 않는 것

- **Adapters**
    - 외부 영역과 내부 영역을 이어주는 어댑터
    - `web` : 웹 클라이언트에서의 요청을 처리
    - `persistence` : 데이터베이스 접근하여 데이터 처리


- **Application**
    - 애플리케이션이 수행할 작업을 정의하고 표현력 있는 도메인 객체가 문제를 해결
    - 여기에는 도메인 로직이 없고, 오직 도메인의 여러 로직을 조합
    - `spi` : service provider interface (port interface) 를 관리, `port` 는 영속화 계층이 자신의 외부 영역과 상호 작용하는 방법을 정의


- **Domain**
    - 도메인에 관한 정보, 비즈니스 로직을 표현하는 일을 책임

-->

## 서비스 URL

**URL** : <a href="mailto:https://causw.co.kr">https://causw.co.kr</a>

## 프로젝트 소개

### 프로젝트 목적

- 학교 생활을 정보가 학교 포탈, 학생회 카카오톡 공지방, 각 동아리 카카오톡 공지방, 과 홈페이지, 오픈 채팅방으로 분산되어 있어 학생들이 원하는 정보를 열람하는데 혼란이 존재함
- 각종 공지, 동아리 관리, 사물함 관리등의 학생 편의 기능을 하나로 모아 혼란 해결 도모
- 개발 파트별 멘토링을 통해 서비스의 지속을 위한 개발진 양성
- 리팩토링을 통해 프로젝트의 코딩 컨벤션 제공으로 코드 지속성에 기여
- 통일된 코딩 컨벤션 내에서 사용자들의 위한 편의 기능 추가를 통해 서비스 활성화

### 프로젝트 구현

![홈화면](https://github.com/pstar987/CAUSW_backend/assets/63050966/5a74690c-f201-4279-8edd-99fca2285360)

홈화면

![학생회 공지 게시판](https://github.com/pstar987/CAUSW_backend/assets/63050966/ccedfed0-648a-4f2e-9ba3-2a2d037c7574)


학생회 공지 게시판 및 게시글 사용

![사물함 관리](https://github.com/pstar987/CAUSW_backend/assets/63050966/84a058cf-7067-43fb-ae8d-8377b89cc4fe)


사물함 관리 서비스

![동아리](https://github.com/pstar987/CAUSW_backend/assets/63050966/3f85ccf6-3100-4913-af4e-34f649d0abaf)


동아리 관리 서비스


### 진행상황
- 서비스 개발진 이외에도 B트랙, C트랙으로 구분하여 추가 개발자를 양성하는 멘토링 진행
- 실제 서비스 배포 후 현재 295명의 사용자가 존재
- 최초 배포 시의 피드백 사항 및 todo 사항을 고려하여 현재 ver.2 개발 중

### ERD Cloud

![2024 동문네트워크](https://github.com/pstar987/CAUSW_backend/assets/63050966/0e92133d-b99c-4e42-8fdf-c6211fe22364)


### Infrastructure

![동문네트워크 인프라](https://github.com/pstar987/CAUSW_backend/assets/63050966/331eac72-925a-4660-8518-e27943790f90)

## 참여 인원

### ver.1 개발진

| 역할 | 인원수 |
| --- | --- |
| Back-End | 4명 |
| Front-End | 2명 |
| 운영, 기획 | 1명 |

### ver.2 개발진

| 역할 | 인원수 |
| --- | --- |
| Back-End | 4명 |
| Front-End | 4명 |
| 기획 | 2명 |
| 디자인 | 2명 |
| 운영 | 1명 |
| 자문위원 | 3명 |
