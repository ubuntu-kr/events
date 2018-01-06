# events
우분투한국커뮤니티 행사 모음

우분투한국커뮤니티 행사 모음 웹사이트 입니다. 행사 정보만 담겨 있으며, 신청 기능과 결제 기능은 포함되어 있지 않습니다.

## 이벤트 정보 추가하기

`_posts` 폴더에 아래와 같은 형식의 이름을 가진 파일을 생성합니다.  
년-월-일-행사-이름.md 형식이며, 년-월-일 부분은 파일 생성한 날의 날짜로 합니다.
```
  YYYY-MM-DD-name-of-the-event.md
````

파일을 열고, 가장 위에 행사 기본정보를 담은 YAML Front Matter 를 넣어줍니다.  
YAML Front Matter 의 시작과 끝은 `---` 로 구분합니다.
```
---
layout: event
title:  "행사 제목"
desc: "행사에 대한 간단한 설명(한문장)"
date: YYYY-MM-DD HH:MM:SS +HH:MM
start_time: YYYY-MM-DD HH:MM:SS +HH:MM
end_time: YYYY-MM-DD HH:MM:SS +HH:MM
submit_start: YYYY-MM-DD HH:MM:SS +HH:MM
submit_end: YYYY-MM-DD HH:MM:SS +HH:MM
location: "행사 장소 위치"
location_query: "Google Map 상에서 해당 위치에 대한 문자열"
price: "0 KRW"
ticket_link: "참가 등록 링크"
image: "행사 페이지의 배경 이미지 URL"
---
```

- layout: 페이지 레이아웃. event 로 유지합니다.
- title: 행사 제목을 입력합니다.
- desc: 행사에 대한 간단한 설명을 한문장으로 씁니다.
- date: 본 파일을 생성한 시각을 대략적으로 입력합니다.
- start_time: 행사 시작 시각을 입력합니다.
- end_time: 행사 종료 시각을 입력합니다.
- submit_start: 행사 참가 등록 시작 시각을 입력합니다.
- submit_end: 행사 등록 마감 시각을 입력합니다.
- location: 행사 장소 위치를 입력합니다.
- location_query: Google Map 상에서 해당 위치에 대한 문자열을 입력합니다.
  - www.google.com/maps/place/(이 자리에 위치한 내용)/...
- price: 참가 비용을 입력합니다. 뒤에 환율 단위도 붙입니다.(예 : 5000 KRW)
- ticket_link: 참가 등록 링크를 입력합니다.
- image: 행사 페이지의 배경으로 나타날 이미지의 URL 을 입력합니다.

### 행사 기본 정보 입력시 참고.
- 모든 시각 정보는 아래와 같은 형식으로 작성하며, 시간대 까지 포함합니다.
  - 예: 2018년 01월 08일 오후 2시, 시간대 : 서울(GMT+09:00)
    - 2018-01-01 14:00:00 +09:00
- 사전 참가 등록 없이 참석하는 행사의 경우, submit_start 와 submit_end 를 지웁니다. 그러면 실제 페이지에서는 등록이 필요 없다고 나타납니다.
- 참가 등록을 받으나, 아직 등록 양식 등이 준비되지 않아 ticket_link 를 입력하지 못한다면, 우선 ticket_link 를 주석 처리 하고. submit_start 와 submit_end 부분만 먼저 입력해 둡니다. 그러면 실제 페이지에서는 준비중 이라고 나타납니다.

이제 행사 상세 정보를 입력합니다. YAML Front Matter 가 끝난 라인 다음 줄에서 부터 작성합니다. 마크다운 문법에 떄라서 작성 하시면 됩니다.

### 연사 프로필 요소
이 사이트에 내장된 연사 프로필 요소를 사용하려면 아래와 같은 방식으로 작성합니다.

```
{% include profile.html
  profile="연사 프로필 이미지 URL"
  heading="발표 제목" bold="연사 이름과 소속 정보"
  desc="발표에 대한 설명" %}
```

아래는 예제 입니다.

```
{% include profile.html
  profile="https://avatars2.githubusercontent.com/u/553900?v=4&s=400"
  heading="Ubuntu 17.10 의 새로운 변화" bold="한상곤 - 우분투한국커뮤니티 Contents Creator, Microsoft MVP(Visual Studio and Development Technologies)"
  desc="우분투 17.10의 대표적인 변화에 대해서 조금 자세히 소개하고 설명합니다. 이번 17.10에서 변화된 내용을 통해서 우리가 함께 주목해야 할 점과 새로운 변화가 가져올 의미를 함께 나눠 볼 수 있도록 준비하였습니다. 새롭게 출시될 LTS(18.04)와 새로운 변화를 기대하는 모든 분들과 함께 하길 기원합니다." %}
```

작성을 완료 하였다면, 해당 파일을 커밋 하여 푸시 합니다. 몇분 기다리면 실제 웹사이트에서 확인이 가능합니다.
