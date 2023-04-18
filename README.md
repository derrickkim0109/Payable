# Payable (페이어블)
> 프로젝트 기간 2023.02.06 ~ 2023.03.12    
개발자 : [iOS- derrick](https://github.com/derrickkim0109), [Backend - Steve](https://github.com/stevejkang)

# 📋 목차
- [🔎 프로젝트 소개](#-프로젝트-소개)
- [📺 프로젝트 실행화면](#-프로젝트-실행화면)
- [🗂 App 구조](#-app-구조)
- [🚀 트러블슈팅](#-트러블슈팅)
- [📚 참고문서](#-참고문서)

## 🔎 프로젝트 소개
> 애플페이 출시에 맞춰 애플페이가 가능한 가맹점들을 지도를 통해서 찾을 수 있고 등록할 수 있는 어플리케이션입니다.

---

## 📺 프로젝트 실행화면

|메인시작화면|결제실패시 피드백하기|검색 및 취소 처리|
|--|--|--|
|<img src="https://i.imgur.com/NjunenR.gif" width="250">|<img src="https://i.imgur.com/4viNHyJ.gif" width="250">|<img src="https://i.imgur.com/WbUiyHP.gif" width="250">|


|모달 dismiss 처리| 제보하기 | 현 위치 다시 검색 및 여러 마커 중복처리|
|--|--|--|
|<img src="https://i.imgur.com/ahvPnRw.gif" width="250">|<img src="https://i.imgur.com/Ipe4tId.gif" width="250">|<img src="https://i.imgur.com/mUEmKJH.gif" width="250">|


|현위치 이동| Apple Wallet으로 이동 |
|--|--|
|<img src="https://i.imgur.com/zAidOJx.gif" width="250">|<img src="https://i.imgur.com/QZHkdSF.gif" width="250">|


---

## 🗂 App 구조

<img src="https://i.imgur.com/hzvXXDL.png" width="800">


### Layers

- **Domain Layer** = Entities + Use Cases + Repositories Interfaces
- **Data Repositories Layer** = Repositories Implementations + API (Network)
- **Presentation Layer (MVVM)** = ViewModels + Views

### Dependency Direction

<img src="https://i.imgur.com/O7ISX8z.png" width="600">

- Domain Layer에 다른 레이어(예: Presentation — UIKit, Data Layer — Mapping Codable)가 포함되지 않도록 처리하였습니다. 

### CleanArchitecture

•역할 분리가 명확하고 기능을 추가하거나 개선할 때 특정 레이어만 접근하기 때문에 확장성과 개발 편의성이 좋다고 생각하였습니다.

•역할 분리가 명확히 나뉘어 있기 때문에 테스트와 코드를 파악하는데 이점이 있다고 생각하였습니다.

---

## 🚀 트러블슈팅

