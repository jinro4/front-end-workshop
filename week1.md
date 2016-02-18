# Front-end Workshop

---

# 이 세미나를 들으면 뭐가 좋을까요

- 이 세미나를 "잘" 듣는다면 세미나가 끝날 무렵 여러분은 좋은 웹 사이트 설계하고 디자인 할 수 있을겝니다.
- 포토샵과 그림판을 벗어난 실제 웹 사이트의 동작을 알 수 있게 됩니다.
- 2차 전직을 할 수 있게 됩니다. (디자이너 / 기획자 -> 퍼블리셔)
- 3차 전직도 열심히 하면 할 수 있습니다. (퍼블리셔 -> 개발자)

---

# 그래서 우리는 뭘 배우나요?

- 처음으로 웹의 구조와 간략한 역사 탐험을 시작합니다.
- HTML, CSS에 대한 기초적인 지식과 레이아웃을 공부합니다.
- 배운 HTML, CSS로 간단한 사이트를 만들어 볼 겁니다.
- HTML5, CSS3에 대한 심화 지식을 공부합니다.
- 각종 빌드 도구, 에디터, SASS에 대한 지식을 공부합니다.
- 마지막으로 실제 서비스를 만들어 볼 겁니다.

---

# 세미나 일정

- 매주 목요일 오후 5시 ~ 8시(최대)
- 저녁 제공(맛있는걸로 골라봅시다.)
- 연휴 때는 다른 날로 정함

---

# Front-end Workshop
## ~ Week 1 ~

---

# 웹의 역사

![](http://mmg.nextleapmediagro.netdna-cdn.com/wp-content/uploads/2014/02/historyoftheinternet-timeline.png)

- 처음은 군사 목적으로 시작됨요
- 그러다 1989년 CERN에서 일하던 팀 버너스리 라는 아저씨가 문서를 한 군데에서 관리하기 위해 '인터넷'이라는 개념을 정의했어요.
- 프로토콜은 우리가 자주 보고 있는 HTTP를 사용하고 있는데 이건 나중에 설명할게요.
- 처음에는 미국, 유럽 외 몇몇 국가만 사용할 수 있게 하다가 규제가 풀리고 빠른 속도로 발전 되었어요.

---

# 과거의 웹

![](http://qk9ekibrxo-flywheel.netdna-ssl.com/wp-content/uploads/2015/10/websites-and-web-services-of-the-past-where-are-they-now.jpg)

- 보는 것과 같이 이전에는 주로 텍스트 위주였어요.
- 이유로는 전송 속도가 14.4kbps, 빨라야 56kbps 였기 때문에 매우 느렸기 때문이죠.(전화비 때문에 엄마한테 등짝맞음)
- 그래서 이에 익숙해진 양반들 때문에 아직도 텍스트 위주 레이아웃 구성을 해놓은 곳이 많답니다.

---

# 현재의 웹

![](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcSjnh0mnZgHASF_RpiE_Rcryt7JIuUjded9fNFi8hbt8ZBcqlQU)

- 전송 속도가 엄청나게 빨라졌기 때문에 이미지, 동영상을 아낌없이 때려붓고 있습니다.
- 또한 마크업 내에서 스타일링 하던 것에서 벗어나 외적인 것은 주로 CSS로 하게 되었죠.
- 과거 페이지를 한 장의 문서로 생각하던 관점과 달리 [웹 사이트 = 애플리케이션] 으로 보고 있습니다.
- 이전에는 상상도 할 수 없었던 브라우저 내에서 게임을 한다거나 렌더링을 하는 일도 벌어지고 있죠.

---

# 웹 표준

- 어느날 염병할 MS가 웹 브라우저의 독자 표준을 주장하면서 IE를 똥 같이 만들어버렸어요.
- 그러면서 다른 브라우저에서 지원하지 않는 API들을 풀면서 웹 표준 전쟁이 시작되었죠.(대표적으로 ActiveX)
- 게다가 이놈들은 Windows를 판매하기 위해 IE 버전이 자동으로 업그레이드 되지 않아요.
- 이런 문제 때문에 W3C에서는 웹 표준 권고안을 제안하게 되고 현대의 브라우저들은 모두 이를 따릅니다.

---

# 웹 표준(이어서)

- 하지만 MS가 그동안 싸놓은 똥 때문에 개발 시 크로스 브라우징을 고려하지 않을 수 없게 되었어요.
- 해외에는 IE 점유율이 많이 떨어지고 크롬이나 사파리 점유율이 증가하고 있지만,
- 국내는 답이 없습니다.(그래도 많이 좋아지고 있어요)
- 따라서 우리는 최소 IE8을 지원하는걸 목표로 하고 있습니다.

---

# 웹 접근성

- 웹 접근성은 웹 표준의 일부로써 "장애 여부와 상관없이 누구나 원활하게 페이지를 사용할 수 있어야 한다." 라는 목적을 가집니다.
- 예를 들어 시각 장애인은 화면을 볼 수 없으니 스크린 리더기를 지원할 수 있도록 마크업을 설계 해야할 테고,
- 마우스를 사용하지 못하는 몸이 불편한 사람을 위해 키보드 만으로도 네비게이션 할 수 있도록 지원해야 합니다.
- 이 내용들은 추후 발전되어 국내에 "장애인 차별 금지 법"에 포함되게 됩니다.(안지키면 벌금이에요)

---

# 그래서 현재는

![](http://file.thisisgame.com/upload/tboard/user/2013/12/14/20131214014047_5048.jpg)

- 과거 이 모든 것을 모호하게 개발자가 혼자 처리하던 것이 현재는 하나의 직종으로 분리 되었습니다.
- 그게 바로 퍼블리셔라는 직종인데 아직 국내에서는 대기업을 제외하고는 희귀한 직종이죠.
- 현실적으로 스타트업이나 소기업에서는 이들을 채용하기 어렵기에 개발자나 디자이너가 역할을 분담해서 작업합니다.
- 간혹 퍼블리셔로 시작해서 디자이너나 개발자로 2차 전직하기도 한답니다.(물론 역으로도)

---

# 쉬는 시간

---

# HTML 소개

- 이제부터는 HTML에 대해 알아 보겠습니다.
- HTML은 하이퍼-텍스트-마크업-랭귀지의 약자로 페이지 내의 구조를 잡고 뼈대가 되는 역할을 합니다.
- 난이도는 하급이지만, 구조를 제대로 작업하지 않으면 추후 CSS를 입히거나 인터렉션을 만들 때 필히 개고생을 할겁니다.
- 기초적인 내용부터 함께 살펴보죠.

---

# HTML 기초

- HTML은 태그라고 불리는 태그의(?) 집합입니다. 아래와 같이 생겼어요.

```html
<html>
<body>
    <h1>전 헤더입니다.</h1>
    <a href="https://livere.com">라이브리 닷컴으로 이동</a>
    <img src="http://mud-kage.kakao.co.kr/14/dn/btqcHfRTtg3/ulq0kjkjFgA14bIplkYaIK/o.jpg">
</body>
</html>
```
- 항상 모든 태그는 열리면 닫혀야 합니다.(XHTML 기준) 다만 현재 HTML5에서는 몇몇 태그는 이를 예외로 하고 있습니다.
- 태그들은 대부분 독자적인 속성을 가지고 있습니다. `<a href=..>`

---

# HTML 기초(이어서)

- HTML은 항상 `<html>` 태그로 시작합니다.
- 헤더의 정보를 담는 `<head>` 태그도 있는데 이는 나중에 설명할게요.
- 실제 HTML 마크업을 담기위해 `<body>` 태그를 사용합니다.

```html
<html>
    <head></head>
    <body></body>
</html>
```

- 위 3개 태그는 반드시 들어간다고 생각하시면 됩니다.

---

# 기초 구문 소개(1)

- 이제 우리는 개인 프로필을 만들어 볼겁니다. 이를 만들기 위해 필요한 요소를 살펴보죠.
- 처음은 `<h1>` 태그 입니다. 이 친구는 페이지의 제목에 주로 사용됩니다.

```html
<html>
<body>
    <h1>Tamm Kwun - Profile</h1>
</body>
</html>
```

- `h` 태그는 `<h1>`부터 `<h4>`까지 있습니다. 각자 크기 뿐만 아니라 대제목 제목 소제목 등 쓰임새가 있어요.

---

# 기초 구문 소개(2)

- 이번에는 각자의 프로필 사진을 추가해봅시다.
- 이미지를 넣는 태그는 `<img>` 태그 입니다. 내부 속성인 `src`를 통해 이미지 경로를 지정할 수 있습니다.

```html
<!-- html, body 생략 -->
<img src="http://mud-kage.kakao.co.kr/14/dn/btqcHfRTtg3/ulq0kjkjFgA14bIplkYaIK/o.jpg">
```

- 이미지는 로컬 컴퓨터 혹은 접근 가능한 URL에 존재해야 합니다.

---

# 기초 구문 소개(3)

- 마지막으로 여러분의 소개와 블로그 URL을 넣어봅시다.
- 줄 바꿈은 `<br>` 태그를 사용하세요!
- URL의 경우 `<a>` 태그의 `href` 속성에 넣을 경우 외부로 이동할 수 있는 하이퍼 링크가 됩니다.

```html
<!-- html, body 생략 -->
- 이름: Tamm Kwun<br>
- 연락처: 010-6565-4768<br>
- 소개: 잘 부탁드립니다. 앞으로도 많은 잉여질을 할 수 있도록 도와주세요.<br>
<a href="https://medium.com/@jinro4">- 블로그로 이동</a>
```

---

# 기초 구문 소개(4)

- 여기까지 잘 따라왔다면 아래와 같은 소스코드가 나올겁니다.
- 여러분이 원하는 정보를 조금 더 넣어보세요!

```html
<html>
<body>
    <h1>Tamm Kwun - Profile</h1>
    <img src="http://mud-kage.kakao.co.kr/14/dn/btqcHfRTtg3/ulq0kjkjFgA14bIplkYaIK/o.jpg">
    - 이름: Tamm Kwun<br>
    - 연락처: 010-6565-4768<br>
    - 소개: 잘 부탁드립니다. 앞으로도 많은 잉여질을 할 수 있도록 도와주세요.<br>
    - 블로그로 이동: <a href="https://medium.com/@jinro4">https://medium.com/@jinro4</a>
</body>
</html>
```
---

# 실습 과제

- 오늘 여러분이 공부한 내용을 잘 곰씹어보세요.
- 프로필 이미지의 사이즈를 조절하기 위해서 어떤 속성을 사용해야 하는지 알아보고 적용해보세요.
- 줄 간격이 너무 다닥다닥 붙어있으니 조금 여유있게 만들어보세요.
- `<a>` 태그를 클릭 했을 때 새 창이 열리도록 만들어보세요.
- 서로 알려주지 마세요 :)