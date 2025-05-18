# TheGreatestYourManito (iOS 17.0+) 💘

> 너만을 위하는 너만의 마니또

<br>

## 💘 소개

> 💡 About 너마니또
>
> - 서비스 소개
>   - 누군가의 비밀 마니또가 되어 따뜻한 응원을 전하는 서비스 앱입니다.
> - 개발 인원
>
>   - 4인 프로젝트 | 기획(1) · 디자인(1) · 서버(1) · iOS(2)
>
> - 개발 기간
>   - 2024.10 - 2024.12 (10주, iOS 2인)

<br>

## 💘 About Developers

<div align=left>

| <img width="200px" src="https://avatars.githubusercontent.com/u/114901417?v=4"/> |
| :------------------------------------------------------------------------------: |
|                     [박신영](https://github.com/ParkSY0919)                      |
|                               iOS                                |

</div>

<br>

## 💘 주요 화면
|   로딩   |   홈   |   방 입장하기   |
| :-------------: | :-------------: | :-------------: |
| <img src = "https://github.com/user-attachments/assets/97e1e4f5-1cc4-4f1e-be19-4198dc63ced1" width ="160">| <img src = "https://github.com/user-attachments/assets/2655f3a8-6caa-430a-9cf3-be3f8b6942e6" width ="160">| <img src = "https://github.com/user-attachments/assets/8eb60ef7-ed30-414b-8037-b98e30cc1a58" width ="160">|


|   방 만들기   |   대기방   |   마니또(응원뷰)   |
| :-------------: | :-------------: | :-------------: |
| <img src = "https://github.com/user-attachments/assets/4ef2da0c-04bf-4995-a4c7-2fc656cffcc5" width ="160">| <img src = "https://github.com/user-attachments/assets/ff49ffcc-5669-4c24-800c-d2beae72981f" width ="160">| <img src = "https://github.com/user-attachments/assets/5f73d7a2-c642-4fcf-9b20-b44c568b4ffe" width ="160">|

<br>

## 💘 주요 기능

> 💡 협업 프로젝트의 담당 기능은 **Bold** 및 ✅ 표시하였습니다.
>
> - **나만의 마니또 방 생성 및 커스터마이징 ✅**
> - **간편한 방 참여를 위한 고유 코드 복사 및 공유 ✅**
> - 랜덤 배정된 마니또 대상자에게 익명의 응원 메시지 전송
> - 행운, 사랑, 열정, 선물 테마별 응원 메시지 선택
> - 일일 응원 활동 현황 및 통계 확인
> - 마니또 이벤트 D-day 카운트다운
> - **참여 중인 방 목록 및 참여자 현황 확인 ✅**
> - **종료일 마니또 신원 공개 및 특별 애니메이션 효과 ✅**
> - **마니또 활동 결과 및 주고받은 응원 내역 확인 ✅**
> - **기기 ID 기반 자동 로그인 및 프로필 관리 ✅**

<br>

## 💘 기술 스택 및 내용

> Framework: `SwiftUI`
>
> Architecture: `MVVM`
>
> Design Patterns: `API Router`, `DI/DIP`, `POP`
>
> Reactive Programming: `SwiftUI (내장 반응형 시스템)`
>
> Library: `Moya`, `Kingfisher`, `SwiftLint`

- IntroViewModel, MainViewModel 등에서 @Published를 활용, 복잡한 마니또 활동(방 생성/참여 등)의 UI 상태와 비즈니스 로직을 분리하여 반응형 UI 업데이트 및 사용자 경험을 개선했습니다.
- BaseTargetType 등으로 API 엔드포인트를 구조화하고 MoyaLoggingPlugin으로 디버깅 효율을 높여 마니또 방 정보 및 응원 메시지 등 실시간 데이터 교환의 안정성과 오류 처리 능력을 향상시켰습니다. 또한 NetworkActivityPlugin을 통해 API 통신 시도부터 이후 응답까지 로딩뷰가 올바르게 동작할 수 있도록 했습니다.
- NetworkService.shared를 통해 마니또 관련 데이터(사용자 식별, 방 관리, 메시지 전송)의 단일 접근점을 제공, 코드 가독성 및 유지보수성을 증진시켰습니다.
- UserDefaults 접근을 추상화한 LocalStorageManager를 구현, 참여 방 정보 및 사용자 ID를 로컬에 효율적으로 관리하여 앱 재실행 시에도 마니또 활동 정보의 연속성을 보장했습니다.
- 기기 UUID를 활용한 사용자 식별 방식을 Device 클래스로 구현하여, 별도 로그인 없이 익명성을 유지하며 앱 진입 장벽을 낮추고 사용 편의성을 증대시켰습니다.
- CopyToastView, YMLoadingView 등을 개발하여 마니또 활동 이벤트(메시지 전송, 방 참여)에 대한 즉각적이고 직관적인 사용자 피드백을 제공, 네트워크 지연 시 UX 저하를 방지했습니다.
- 마니또 방 코드 공유를 위해 ActivityViewController를 구현하여 Email 등을 통한 손쉬운 공유로 사용자 확장 및 활동 활성화를 지원했습니다.
- UserServiceProtocol, RoomServiceProtocol 등으로 네트워크 서비스 인터페이스와 구현을 분리, 모듈 간 의존성 감소, 테스트 용이성 및 유지보수 비용 절감을 달성했습니다.

<br>
