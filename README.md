# project_time_namhui
1만 시간의 법칙 웹 페이지
1. 프로젝트 개요

본 프로젝트는 **「1만 시간의 법칙」**을 주제로 한 단일 페이지 웹 애플리케이션입니다.
사용자가 목표 분야와 하루 훈련 시간을 입력하면, 해당 목표를 달성하기 위해 필요한 총 훈련 일수를 직관적으로 안내하는 UI를 제공합니다.

HTML5 시맨틱 구조 기반

CSS Flexbox 중심의 반응형 레이아웃

모바일 우선(Mobile First) 설계

2. 프로젝트 목적

시맨틱 HTML을 활용한 구조적 문서 작성 능력 강화

Flexbox와 미디어 쿼리를 이용한 반응형 레이아웃 구현

접근성을 고려한 UI 구성 (visually-hidden 활용)

디자인 시안 기반 퍼블리싱 역량 검증

3. 기술 스택
구분	내용
Markup	HTML5
Styling	CSS3
Layout	Flexbox
Responsive	Media Query (min-width: 993px)
Font	GmarketSans, NotoSansKR, OTEnjoystories
4. 폴더 구조
project
 ┣  images
 ┣  index.html
 ┣  style.css
 ┣  reset.css
 ┣  font.css

5. 페이지 구조 설명 (HTML)
5.1 Header

서비스 타이틀 이미지와 인용 문구 배치

배경 이미지(clock.png)를 활용한 시각적 강조

실제 제목은 h1.visually-hidden 처리하여 접근성 유지

<header>
  <h1 class="visually-hidden">1만 시간의 법칙</h1>
  <img class="title" ... />
  <blockquote class="quote">...</blockquote>
</header>

5.2 Main
1) 소개 영역 (.intro)

dfn 태그를 사용하여 “1만 시간의 법칙”의 정의 명확화

배경 quotes 이미지 활용

2) 계산기 영역 (.calculator)

목표 분야 입력(input text)

하루 훈련 시간 입력(input number)

<form> + <fieldset> 구조로 의미적 그룹화

3) 결과 버튼 영역 (.submit)

핵심 CTA(Call To Action) 버튼

버튼 옆 클릭 유도용 이미지 배치

4) 결과 출력 영역 (.result)

<output> 태그를 사용하여 계산 결과 표현

강조된 숫자 표현을 위한 Bold 폰트 적용

5) 액션 영역 (.action)

추가 행동 유도 버튼 배치

확장 기능(모달, 공유 기능) 영역으로 설계

5.3 Footer

로고 및 저작권 문구

작은 폰트와 중앙 정렬로 시각적 부담 최소화

6. 스타일링 전략 (CSS)
6.1 공통 스타일

body를 Flex 컨테이너로 설정하여 전체 중앙 정렬

브랜드 컬러(#5B2386, #FCEE21) 중심의 컬러 시스템 유지

버튼은 공통 button 스타일로 일관성 확보

6.2 접근성 고려
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
}

스크린 리더를 고려한 숨김 텍스트 처리

시각적 요소와 문서 구조 분리

6.3 레이아웃 구성

대부분의 영역을 flex-direction: column으로 구성

입력 영역은 가독성을 위해 가로 배치(row) 적용

요소 간 gap 속성 활용으로 여백 관리


6.4 반응형 디자인

기준 해상도: min-width: 993px

데스크톱 환경에서:

폰트 크기 확대

입력창 및 버튼 너비 확장

결과 숫자 강조 (output: 72px)

@media screen and (min-width: 993px) {
  main {
    width: 780px;
    font-size: 14px;
  }
}

7. 구현 시 고려 사항 및 개선 포인트

width: 500px 등 고정 폭 요소 → 반응형 단위로 개선 가능

8. 결론

본 프로젝트는 HTML/CSS 퍼블리싱의 기본 구조와 반응형 레이아웃 구현 능력을 목표로 제작되었습니다.
시맨틱 구조, 접근성, 디자인 일관성을 이해하고 작성하려는 노력을 하였습니다.