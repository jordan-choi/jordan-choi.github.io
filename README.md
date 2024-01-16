# 안녕하세요, 프론트엔드 개발자 최윤영입니다.

[블로그]() / [github](https://github.com/jordan-choi) / [yyoungbest@gmail.com](mailto:yyoungbest@gmail.com)

이펙티브 엔지니어링을 지향하여, 빠르게 제품을 개선할 수 있는 개발 환경을 만들기 위해 고민합니다.
동료와 함께 성장하는 것이 더 큰 성장을 향한 길이라 믿습니다.

## Work Experience

### [iPortfolio](https://www.iportfolio.co.kr/) (2022.01 - 현재)

국내/외 영어 교육 서비스를 제공하는 에듀테크 스타트업입니다. 국내 b2c 서비스인 [리딩앤](https://www.readingn.com/)과 b2b 서비스인 [리딩앤 LMS](https://lms.readingn.com/)를 담당하는 리딩앤 개발팀에서 프론트엔드 개발을 담당하였습니다.
| | |
| -------- | --------------------------------------------------- |
| position | 리딩앤 개발팀 (사내 프로덕트 프론트엔드 개발) |
| projects | Design System, 공통 패키지 운영, 리딩앤 CRM, 스피킹앤 Admin |
| Tech stack | TypeScript, React, Next.js, styled-components |

### Design System

- 추상화 레벨에 따른 디자인시스템 계층화
  - 어드민용 디자인시스템을 디자인시스템 하위 디자인시스템으로 구축
  - 도메인 종속 컴포넌트를 디자인시스템에서 하위 도메인 라이브러리로 분리
- 컴포넌트별 버전 관리 방식으로 개선하여 디자인과 개발 간 컴포넌트 버전 동기화
- 파편화된 인터페이스 용어 동기화
- 디자인시스템 컴포넌트 인터페이스 개선
  - 개발자에게 친숙한 native element와 비슷한 인터페이스로 개선
  - Compound Component 패턴 적용
- 어드민용 디자인시스템 구축
  - [glide-data-grid](https://grid.glideapps.com/)를 활용해 편집 가능한 엑셀 UI를 제공하는 DataGrid 컴포넌트 신규 개발
    - DataGrid 셀별로 validation message를 툴팁 형태로 제공
    - 칼럼별로 validation 룰을 커스텀할 수 있는 인터페이스 제공

### 공통 패키지 운영

#### 모노레포 구축 및 개선

- 각 프로젝트에서 중복으로 만들어 사용하고 있던 공통 함수들을 monorepo 멀티 패키지 구조로 변경
- 초기 앱과 라이브러리 통합 관리하던 방식에서 앱과 라이브러리별 모노레포로 분리
  - 이 과정에서 모노레포 도구를 [Nx](https://nx.dev/)에서 [turborepo](https://turbo.build/repo)로 이관
- [changesets](https://github.com/changesets/changesets)을 이용한 문서화 및 버전 관리
- Github actions을 이용한 CI/CD 구성
  - 워크플로우를 재사용하여 서비스별 배포 파이프라인 구축
- [msw](https://github.com/mswjs/msw), [testing-library](https://testing-library.com/), [storybook](https://storybook.js.org/)을 이용한 패키지 간 동일한 테스트 환경 구성

#### 도메인별 공통 라이브러리 제공

- 학습 리포트 도메인 공통 라이브러리 rs-report 개발
  - 비즈니스 레벨에서 정의한 차트 컴포넌트를 여러 서비스에서 사용할 수 있도록, 공통 라이브러리로 제공
  - 차트 엘리먼트 > 차트엘리먼트를 조합한 내부 차트 컴포넌트 > 내부 차트 컴포넌트를 조합한 비즈니스 차트 컴포넌트, 총 3단계로 분류하고 각 레이어의 책임을 정의
  - [chart.js](https://www.chartjs.org/)를 래핑하여 내부 차트 컴포넌트 Bar, Doughnut (Half Doughnut 포함), Line 구현
- 수업 도메인 공통 라이브러리 rs-class 개발
  - 수업 예약 관리 관련 비즈니스 로직, 컴포넌트를 모듈화
- 도메인에 종속되지 않는 공통 유틸을 rs-common 패키지로 제공

### 리딩앤 CRM

- Feature별(account, class, report) 디렉토리 구조 구성
- [React Query](https://tanstack.com/query/v3/)를 활용한 서버 상태 관리
  - 위계를 한 눈에 파악할 수 있도록 queryKey 네이밍 규칙 도입 및 feature별 colocation
- 도메인 공통 라이브러리를 활용해 수업 예약 관리, 주간/월간 학습리포트 관리 기능 개발

### 스피킹앤 Admin (현재 서비스 종료)

- [swr](https://swr.vercel.app/ko)를 이용한 서버 상태 관리
- [Antd Table](https://ant.design/components/table/)을 래핑하여 Table 컴포넌트 모듈화
  - xlsx 파일로의 export 기능 및 Clipboard API를 활용한 Table 복사 기능 제공
- requestAnimationFrame을 이용한 실시간 수업 관전 기능 개발

## Communities

- 2021 두굿해커톤 대상 수상 (2021.08.13 - 08.15)
- 2021 GDG 썸머 해커톤 유니콘상 수상 (2021.07.10 - 07.11)

## Education

- 건국대학교 전자정보통신공학과 석사 졸업 (2018.03 - 2021.02)
  - "Collision Avoidance Geographic P2P-RPL in Multi-Hop Indoor Wireless Networks."; Choi, Y.; Park, J.; Jung, J.; MDPI Electronics, 2021 [[Link]()].
  - "Location-Aware Point-to-Point RPL in Indoor IR-UWB Networks."; Jung, J.; Choi, Y.; Park, J.; MDPI Electronics, 2020 [[Link]()].
- 건국대학교 전자정보통신공학과 학사 졸업 (2014.03 - 2018.02)
