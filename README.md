# README.md

## [데모 페이지](https://youryu0212.github.io/clone-kakaopage/)

- 기능 : 월,화,수,목,금,토,일 탭 전환
- 슬라이딩 배너 구현 ( 3초에 한번씩 or 클릭시 전환 )

## STEP4 변경사항 :

- 파일 네이밍컨밴션 변경 : handler -> weeklyWebtoonHandler
- 변수명 네이밍컨벤션 변경 : main -> webtoon-weekly, cardInfo -> weeklyWebtoonImageCard 등
- 폴더구조 변경 : js파일 별도 폴더로 이동
- express 서버 구현

## SETP3 이후 피드백 반영 :

- [x] 4가아니고 다른 갯수도 동작하게 한다면?? 어렵겠군요.. :
  - 매직 넘버 (4) => imageCardInfo.length 로 변경
- [x] 메서드가 좀 복잡해보이죠? 아주 긴 건 아닌데. 하위함수로 더 분리할 수 있을까? 한번 고민은 해보세요. : image-box-handler.js의 nextImage 함수
- [x] 하위함수로 분리하고 나서 위 함수랑 중복을 해결할 수 있는 부분도 생길지 모르겠네요. : image-box-handler.js의 prevImage 함수
  - 두 메소드에서 setInterval 타이머 초기화 로직 중복을 하위함수로 분리
- [x] 이런걸 써 됩니다. target.parentNode 그런데 DOM구조가 바뀌면 이 코드가 동작하지 않을수도 있어요
  - 다음, 이전 두 버튼의 이벤트를 분리하여 parentNode 사용을 제거 가능, 이벤트 버블링 구현 연습을 위해 구현은 x
- [x] 계산에 의해서 이런값을 설정하는 것 좋고요. 100이라는 숫자는 여전히 매직넘버긴하고요. 이름 달아주셔요.
  - 매직넘버 제거 : const TRANSLATE_RANGE = 100; const SLIDER_INTERVAL = 2000;

## 학습진행상황

- CSS 경험이 없다보니 새로운 탭 UI를 만드는데 너무 많은 시간이 소요될 것 같아 처음 구현했던 요일연재 탭에서 자바스크립트 연습을 우선했습니다. DOM 조작은 처음이라 구현에 급급하지 않고 학습과의 밸런스를 맞추기 위한 선택이었지만 CSS를 많이 연습하지 못한 것이 아쉽습니다. 오늘과 주말을 이용해 CSS를 연습할 계획입니다.
- 네이밍 컨벤션이 형편없다는 것을 인지했습니다. 알고리즘풀이로 개발을 시작해서인지 아직도 변수명을 짓는게 생소하고 힘들기만합니다. 지금부터라도 계속 수정해봐야겠는데 저 스스로 읽기에도 코드가 난잡해지고있어서 읽고싶은 마음이 떨어지는게 사실이네요. 앞으로는 처음 코드를 짤 때 부터 변수명에 조금이라도 더 많은 시간을 투입해야겠습니다.
- 홈, 요일연재 탭을 구현하지 않고 요일연재 내부의 요일 탭 이벤트만 구현하다보니 querySelector과 innerHTML 두 메소드만으로 충분했습니다. createElement, appendChild , insertBefore 등 다양한 메소드를 활용해보라는 요구사항이 있었음에도 스스로 경험의 폭을 줄여버린 느낌이네요. 오늘부터 여러 탭을 만들어보면서 여러 메소드를 경험해보겠습니다.

## 질문사항

-

## 카카오페이지 클론 - HTML,CSS,Javascript

- [x] 카카오페이지 헤더 구현
- [x] 네비게이션 바 레이아웃 구현
- [x] 이미지 박스 ( 설명 멘트 및 광고 이미지 포함 ) 레이아웃 구현
- [x] 이미지 카드 ( 웹툰별 리스트에 사용하기 위함 ) 레이아웃 구현
- [x] 네비게이션 레이아웃 활용 : 탭 UI
- [x] 네비게이션 레이아웃 활용 : 요일 탭 UI
- [x] 네비게이션 레이아웃 활용 : 웹툰 선택기준 UI
- [x] 웹툰 리스트 레이아웃 구현
- [x] 이미지 카드 레이아웃 활용 : 웹툰 정보 출력 이미지 카드 구현
- [x] footer 구현

## DOM API를 활용한 카카오페이지 동적 기능 개선

- 학습목표 :
- [x] 요일 연재 탭 각 요일별 데이터 구축
- [x] 요일 하이라이트 표시 이동
- [x] 이미지 박스 교체 함수
- [x] 이미지 카드 교체 함수
- [x] 선택된 요일 글자 진하게 표시 (selected-text) position 이동 함수
- [x] 이벤트 핸들링 함수
- [x] 이벤트 버블링 활용

## 슬라이드 구현

- [x] 자동 슬라이딩
- [x] 무한 슬라이딩
- [x] 버튼 이벤트 (이벤트 버블링 활용)
- [x] 셋타임아웃, 셋인터벌 활용

## express를 이용한 서버 구현

- [x] npm 학습
- [x] express 설치
      <img width="1215" alt="image" src="https://user-images.githubusercontent.com/87521172/155580109-38a6461d-17f7-46cb-b4df-bf56ac4a7b21.png">

## 이전 step 피드백

- [x] 클래스명 축약 : main-content**content**nav**circile -> main-content**nave_circle
- [x] 파일 네이밍 변경 : 파일 이름 연결에 언더바(\_) 사용 -> 대쉬 (-)로 변경
- [x] children[1].children 대신 셀렉터로 표현가능 (imageBoxContainer.querySelector(".image-box\_\_page-info") 등 활용)
- [x] el,boxInfo 등 변수명 불분명 -> 헝가리안 표기법 확인할 것 ( 헝가리안 표기법은 프로젝트 규모가 큰 현재에는 잘 사용하지 않는 방법이라고 하여 변수명을 좀 더 의미있게 변경 )
- [x] 변수명이 의도를 담을 수 있게 구체적으로 작성 ( handler -> weeklyWebtoonHandler 처럼 변수에 의미를 부여)
