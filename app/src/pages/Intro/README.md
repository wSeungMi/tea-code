# 사용자 가이드 intro.js-react

## 주제

intro.js와 같은 기능을 제공하는 라이브러리는 사용자에게 웹사이트나 애플리케이션의 특정 기능을 소개하는 인터랙티브 가이드를 만들 수 있게 해주는 도구입니다. 이러한 유형의 라이브러리나 기능을 일반적으로 "사용자 가이드 라이브러리", "투어(Tour) 라이브러리", 또는 **"워크스루(Walkthrough) 라이브러리"**라고 부릅니다.

### 사용자 가이드 라이브러리의 주요 용도

- **사용자 온보딩**: 새로운 사용자가 애플리케이션을 처음 사용할 때 기능을 소개합니다.
- **기능 강조**: 업데이트된 기능이나 중요한 기능을 사용자에게 직접 보여줍니다.
- **사용자 경험 향상**: 사용자가 애플리케이션을 더 쉽고 효과적으로 사용할 수 있도록 돕습니다.

## 목표

intro.js-react를 사용하여 React에서 사용자 가이드 기능을 구현할 수 있습니다.

## 내용

intro.js-react의 Step과 Hint 컴포넌트를 사용하여 사용자 가이드 기능을 구현합니다.

- Step: 페이지에 접근 시 바로 단계별로 보여주는 가이드
- Hint: 아이콘 클릭시 나타나는 설명 (like tooltip)

## 역할

- 네비게이터: 민경
- 드라이버: 승미

## 기능 구현 명세

### 조건

- 화면에 접속 시 blur 효과에 대한 설명이 툴팁으로 보여집니다.

### 프로세스

1. import

   1.1. Intro.js-react에서 Steps와 Hints를 import합니다.

   1.2. Intro.js의 CSS 파일을 import합니다.

2. Step과 Hint의 활성화 여부를 관리하는 상태를 정의합니다. (stepsEnabled, hintsEnabled)

3. 사용자 가이드 투어를 위한 Step들을 정의합니다.

   3.1. 연결할 요소를 선택합니다. (element)

   3.2. 해당 요소에 대한 설명을 작성합니다. (title, intro)

4. 힌트를 정의합니다.

   4.1. 연결할 요소를 선택합니다. (element)

   4.2. 해당 요소에 대한 설명을 작성합니다. (hint)

5. Step과 Hint 컴포넌트를 작성합니다.

   5.1. Step 컴포넌트에 속성 추가

   - enabled : 스텝들이 보이는지 여부를 정의, 기본값은 false
   - initialStep: 투어를 시작할 때의 스텝 인덱스
   - steps: 모든 스텝 정보
   - onExit: 스텝들이 비활성화될 때 호출되는 콜백

     5.2. Hint 컴포넌트에 속성 추가

   - enabled: 보이는지 여부, 기본값 false
   - hints: 모든 hint 정보

6. localstorage에 방문 여부 확인하는 코드를 작성하고 state에 적용합니다.