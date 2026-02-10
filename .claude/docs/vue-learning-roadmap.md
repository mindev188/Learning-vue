# Vue 2 단기 학습 로드맵 (4주)

> **대상**: Java Spring 백엔드 개발자 | **목표**: Vue 2 Options API 기반 풀스택 개발
> **학습 방식**: 이론 → 코드 예제 → 미니과제 → 복습

---

## 📅 1주차: 기초 (Vue 기본 문법)

> 💡 Spring 비유: Vue 인스턴스 = Spring의 ApplicationContext, 디렉티브 = JSP 태그 라이브러리

### Day 1-2: Vue 인스턴스와 데이터 바인딩
- [ ] CDN으로 Vue 2 프로젝트 세팅 (빌드 도구 없이 시작)
- [ ] `new Vue()` 인스턴스 생성 및 `el`, `data` 이해
- [ ] 텍스트 보간법 (`{{ }}`) — Mustache 문법
- [ ] `v-bind` 디렉티브로 속성 바인딩
- [ ] 단방향 vs 양방향 데이터 바인딩 개념

**📝 미니과제**: 자기소개 카드 만들기 (이름, 나이, 취미를 data로 관리)

### Day 3-4: 조건부 렌더링과 리스트 렌더링
- [ ] `v-if` / `v-else-if` / `v-else` 조건부 렌더링
- [ ] `v-show`와 `v-if`의 차이
- [ ] `v-for`로 리스트 렌더링 (배열, 객체)
- [ ] `:key` 바인딩의 중요성

**📝 미니과제**: 할 일 목록(Todo) 화면 구성 (추가/삭제는 아직 X, 렌더링만)

### Day 5: 이벤트 핸들링과 양방향 바인딩
- [ ] `v-on` (또는 `@`) 이벤트 핸들링
- [ ] `v-model` 양방향 바인딩
- [ ] 이벤트 수식어 (`.prevent`, `.stop`, `.enter`)
- [ ] methods에 함수 정의

**📝 미니과제**: Todo 리스트에 입력 & 추가/삭제 기능 구현

### Day 6-7: computed, watch, methods
- [ ] `computed` 속성 — 캐싱되는 계산된 값
- [ ] `watch` 속성 — 데이터 변화 감지 (API 호출 등)
- [ ] `methods` vs `computed` vs `watch` 사용 시점 구분
- [ ] 필터링, 정렬 등 computed 실전 활용

**📝 미니과제**: Todo 리스트에 필터링 기능 추가 (전체/완료/미완료)

### ✅ 1주차 완료 체크
- [ ] Vue 인스턴스의 `data`, `methods`, `computed`, `watch` 역할을 설명할 수 있다
- [ ] 주요 디렉티브 6개(`v-bind`, `v-if`, `v-show`, `v-for`, `v-on`, `v-model`)를 사용할 수 있다
- [ ] Todo 리스트 앱을 직접 만들 수 있다

---

## 📅 2주차: 핵심 (컴포넌트와 라우팅)

> 💡 Spring 비유: 컴포넌트 = Spring Bean, Props = 생성자 주입, $emit = 이벤트 퍼블리싱

### Day 1-2: 컴포넌트 기초
- [ ] Vue CLI 설치 및 프로젝트 생성 (`vue create`)
- [ ] `.vue` 파일 구조 (template / script / style)
- [ ] 전역 등록 vs 지역 등록
- [ ] 컴포넌트 분리 기준과 설계 원칙

**📝 미니과제**: Todo 리스트를 컴포넌트로 분리 (TodoItem, TodoList, TodoInput)

### Day 3-4: Props와 $emit (부모-자식 통신)
- [ ] Props — 부모 → 자식 데이터 전달
- [ ] Props 타입 검증 및 기본값
- [ ] `$emit` — 자식 → 부모 이벤트 전달
- [ ] 단방향 데이터 흐름 원칙 이해

**📝 미니과제**: TodoItem에서 완료/삭제 이벤트를 부모로 전달

### Day 5: 컴포넌트 생명주기 (Lifecycle Hooks)
- [ ] `created` / `mounted` / `updated` / `destroyed`
- [ ] 각 훅의 실행 시점과 활용 사례
- [ ] `mounted`에서 API 호출하는 패턴

**📝 미니과제**: 컴포넌트 마운트 시 콘솔에 생명주기 로그 출력

### Day 6-7: Vue Router
- [ ] SPA 개념 이해 (vs 전통적 MPA)
- [ ] `vue-router` 설치 및 설정
- [ ] `<router-view>`, `<router-link>` 사용
- [ ] 동적 라우트 (`:id` 파라미터)
- [ ] 중첩 라우트 (Nested Routes)
- [ ] 슬롯(slot) 기초 — 컴포넌트 콘텐츠 분배

**📝 미니과제**: 멀티페이지 Todo 앱 (홈, Todo목록, Todo상세)

### ✅ 2주차 완료 체크
- [ ] `.vue` 싱글 파일 컴포넌트를 작성할 수 있다
- [ ] Props와 $emit으로 부모-자식 통신을 구현할 수 있다
- [ ] Vue Router로 페이지 전환을 구현할 수 있다
- [ ] 생명주기 훅의 실행 순서를 설명할 수 있다

---

## 📅 3주차: 실무 (상태관리와 API 연동)

> 💡 Spring 비유: Vuex = 전역 서비스 레이어, axios = RestTemplate/WebClient

### Day 1-2: Vuex 상태관리
- [ ] Vuex가 필요한 이유 (Props drilling 문제)
- [ ] `state` / `mutations` / `actions` / `getters` 개념
- [ ] Vuex 스토어 생성 및 컴포넌트에서 사용
- [ ] `mapState`, `mapGetters`, `mapActions` 헬퍼

**📝 미니과제**: Todo 앱의 상태를 Vuex로 이관

### Day 3-4: axios HTTP 통신 + Spring REST 연동
- [ ] axios 설치 및 기본 사용법 (GET, POST, PUT, DELETE)
- [ ] async/await 패턴
- [ ] Spring Boot REST API 서버 준비 (간단한 Todo CRUD)
- [ ] Vue에서 Spring API 호출
- [ ] CORS 설정 (Spring: `@CrossOrigin`, Vue: proxy 설정)

**📝 미니과제**: Spring 백엔드와 연동되는 Todo CRUD 완성

### Day 5-6: 실전 패턴
- [ ] API 모듈화 (axios 인스턴스, interceptor)
- [ ] 로딩 상태 관리 (로딩 스피너)
- [ ] 에러 핸들링 (try-catch, 에러 메시지 표시)
- [ ] 폼 유효성 검사 (직접 구현)

**📝 미니과제**: API 호출 시 로딩/에러 상태 처리 추가

### Day 7: 중간 복습 & 리팩토링
- [ ] 1~3주차 핵심 개념 복습
- [ ] 코드 리팩토링 및 구조 정리
- [ ] 부족한 부분 보충 학습

### ✅ 3주차 완료 체크
- [ ] Vuex의 state → mutation → action 흐름을 설명할 수 있다
- [ ] axios로 REST API를 호출할 수 있다
- [ ] Spring Boot 백엔드와 Vue 프론트엔드를 연동할 수 있다
- [ ] CORS 문제를 해결할 수 있다

---

## 📅 4주차: 심화 (인증과 실전 프로젝트)

> 💡 Spring 비유: Navigation Guard = Spring Security Filter, JWT = 동일 개념

### Day 1-2: 인증/인가 (JWT)
- [ ] JWT 토큰 개념 복습 (Spring Security 연동)
- [ ] 로그인 화면 구현
- [ ] 토큰 저장 (localStorage vs Vuex)
- [ ] axios interceptor로 토큰 자동 첨부
- [ ] 토큰 만료 처리

**📝 미니과제**: 로그인/로그아웃 기능 구현

### Day 3-4: 네비게이션 가드와 권한 제어
- [ ] `beforeEach` 전역 가드
- [ ] 라우트별 가드 (`beforeEnter`)
- [ ] 인증 상태에 따른 페이지 접근 제어
- [ ] 404 페이지 처리

**📝 미니과제**: 비로그인 시 로그인 페이지로 리다이렉트

### Day 5: 환경변수와 빌드
- [ ] `.env` 파일과 환경변수 (`VUE_APP_*`)
- [ ] 개발/운영 환경 분리
- [ ] `npm run build` 빌드 산출물 이해
- [ ] Spring Boot에 정적 리소스로 배포하는 방법

**📝 미니과제**: 환경별 API URL 분리 설정

### Day 6-7: 미니 풀스택 프로젝트
- [ ] 게시판 또는 관리자 대시보드 중 택 1
- [ ] 요구사항 정의 및 화면 설계
- [ ] Spring Boot 백엔드 API 구현
- [ ] Vue 프론트엔드 구현
- [ ] JWT 인증 적용
- [ ] 빌드 및 통합 테스트

### ✅ 4주차 완료 체크
- [ ] JWT 기반 로그인/인증 흐름을 구현할 수 있다
- [ ] 네비게이션 가드로 페이지 접근을 제어할 수 있다
- [ ] Vue 프로젝트를 빌드하고 배포할 수 있다
- [ ] Spring + Vue 풀스택 애플리케이션을 독립적으로 구축할 수 있다

---

## 🎯 학습 원칙

| 원칙 | 설명 |
|------|------|
| **매일 코딩** | 이론만 읽지 말고 반드시 코드를 작성한다 |
| **점진적 확장** | Todo 앱 하나를 4주간 점진적으로 발전시킨다 |
| **Spring 비유** | 새로운 개념은 항상 Spring/백엔드와 대응시켜 이해한다 |
| **기록** | 새로 배운 것, 헷갈리는 것을 메모한다 |
| **완성** | 4주차 미니 프로젝트를 반드시 완성한다 |

## 📁 프로젝트 폴더 구조 (예상)

```
Learning-vue/
├── week1-basics/          # CDN 기반 기초 실습
│   ├── 01-instance/
│   ├── 02-directives/
│   ├── 03-events/
│   └── 04-computed-watch/
├── week2-components/      # Vue CLI 프로젝트
│   └── todo-app/
├── week3-api/             # API 연동
│   ├── frontend/
│   └── backend/           # Spring Boot
├── week4-project/         # 최종 프로젝트
│   ├── frontend/
│   └── backend/
└── .claude/
    └── docs/              # 학습 문서
```

---

> 📌 **진행 상태**: 학습 시작 전 (2026-02-10 생성)