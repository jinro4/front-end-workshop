# Front-end Workshop
## ~ Week 4 ~

---

# 4주차가 밝았습니다.

- 지난 주에는 이제 태그 중 쓸만한 애들은 거의 다 배웠습니다.
- 물론 지금까지 배운 태그 말고도 여러 친구들이 있지만 그건 추후 HTML5 차례에 같이 다뤄보도록 하죠!
- 이번 주부터는 예고대로 `CSS`라는 놈에 대해 공부해보겠습니다.
- 예비군 가기 싫다..

---

# CSS - Cascading StyleSheet

- `HTML`이 인체를 구성하는 뼈대라면 `CSS`는 살과 옷같은 존재입니다.
- 무언가를 스타일링하거나 레이아웃을 변경하는 등의 역할을 하지요.
- 매번 버전이 올라가고 있고 현재는 `CSS3`가 권고 상태입니다.
- 이 친구는 조금 어렵지만 잘 따라온다면 큰 무리는 없을겁니다.

---

# CSS의 간략한 역사

- `CSS`는 1996년에 공식적으로 도입되었습니다.
- 이전까지는 무조건 `HTML`만을 이용해 스타일링을 했었는데 이건 말그대로 지옥이었어요.
- 여러분에게 몇번 실습 과제로 냈던 `<font>` 태그나 `<center>` 태그등을 통해서 일일이 하나하나 스타일링 했습니다.
- 하지만 `CSS`를 사용한다면 보다 편하고 아름답게 스타일링 할 수 있습니다.

---

# CSS 기초

- `CSS`는 `<head>` 태그 안에 `<style>` 태그 사이에 넣습니다.
- 물론 외부 파일로 불러오거나 태그 안에 인라인으로도 넣을 수 있습니다.
- 기본 문법은 다음과 같습니다.

![inline](http://www.w3schools.com/css/selector.gif)

---

# 이제 글자 색을 바꿔봅시다.

- 우선 태그의 색상을 바꿔볼까요
- 태그 색상을 바꾸는 `CSS`는 `color` 입니다.

```CSS
p {
    color: blue;
}
```
```HTML
<p>저는 파란색 입니다.</p>
```

---

# 텍스트 관련된걸 조금 더 볼까요

- 글자 크기를 늘리기 위해서는 `font-size`를 사용합니다.
- 동시에 글자도 굵게 만들어보죠.

```CSS
p {
    color: blue;
    font-size: 14px;
    font-weight: bold;
}
```

---

# 이제 `id`와 `class`를 공부해봅시다.

- `id`는 앞에서 한번 다룬적이 있지만 `class`는 생소할겁니다.
- 이 둘은 각 엘리먼트를 식별하고 종류를 결정하는 역할을 합니다.
- `id`는 반드시 동일 페이지에 하나만 존재할 수 있습니다.
- `class`는 "종류"를 구분한다고 생각하시면 됩니다.

```HTML
<button id="submit-btn" class="my-btn">승인</button>
<button id="cancel-btn" class="my-btn color-gray">취소</button>
```

---

# 얘들을 쓰면 뭐가 좋을까요

- 각 엘리먼트들의 역할을 명확하게 구분할 수 있습니다.
- 누군가 당신의 소스코드를 봤을 때 쉽게 이해할 수 있도록 도움을 줍니다.
- 따라서 이름을 잘 정해야 합니다.(사실 이게 제일 어려움)

```HTML
<div id="wrapper">
    <p class="pppp">잘못된 예</p>
    <p class="color-red font-size-14">좋은 예</p>
</div>
```

---

# `id`, `class` 셀렉터

- 지금까지 한 내용은 태그에 직접 `CSS`를 먹이는 방법이었어요.
- 하지만 이제 `id`와 `class`를 배웠으니 각각에 `CSS`를 적용해봅시다.
- `id`는 해당 `id` 앞에 `#`를 붙이면 됩니다.
- `class`는 `.`을 붙이면 되영

```CSS
#submit-btn { color: red }
.my-btn { color: blue; }
```

---

# 이제 사이즈를 조절해봅시다

- 대부분의 엘리먼트는 사이즈를 조절할 수 있습니다.
- `width`, `height`을 통해서 `div`와 여러 엘리먼트를 조절해봅시다.

```HTML
<div id="wrapper">
    <input type="text" class="my-text">
    <button type="button" class="my-btn">버튼이에요</button>
</div>
```

```CSS
#wrapper { width: 200px; }
.my-text { width: 100px; height: 30px; }
.my-btn { width: 50px; }
```

---

# 그럼 실습을 해봅시다.

- 이전에 만들었던 프로필 기억하시나요?
- 그 프로필을 조금 더 예쁘게 만들어보세요.
- 위에서 배운 내용을 토대로 색상과 크기를 변경하시면 됩니다.
- 마지막 실습에도 사용될꺼니 꼭 저장해주세요.

---

# 이제 배경에 대해 공부해봐요

- 이번에는 배경의 색을 바꾸거나 이미지를 넣어볼게요.
- 배경이니까 `background`라고 쓰시면 됩니다.

```CSS
.box1 {
    background-color: red;
}

.box2 {
    background-image: url(이미지 URL);
}
```

---

# 배경 이미지에 관련해서 더 알아봅시다

- 만약 이미지를 바둑판식 배열 형태로 하기 싫다면 다음 내용을 적용하세요.

```CSS
.box1 { background-repeat: no-repeat; }
```

- 이미지의 위치를 정할 수도 있어요(박스 내의)

```CSS
.box1 { background-position: right top; }
```

- 또한 이미지를 스크롤과 무관하게 고정할 수도 있어요.

```CSS
.box1 { background-attachment: fixed; }
```

---

# 사실 이걸 한 줄에 다 쓸수도 있답니다.

```CSS
.box1 {
    background: blue url(이미지 URL) no-repeat right top;
}
```

- 이런걸 `속기 속성`이라고 합니다.
- `background` 말고도 `margin`, `padding`, `border` 등 여러가지 속기 속성이 존재합니다.
- 하지만 오히려 가독성이 떨어지니 쓰지말자고 하는 사람들도 있어요.(개취)

---

# 이제 간격을 조절해봅시다.

- 간격을 조절하는 `CSS`는 크게 3가지 입니다.
- 바로 앞서 언급했던 `margin`, `padding`, `border` 랍니다.
- 이를 이해하기 위해서 다음 사진을 잘 봐주세요.

![inline](http://www.havequery.com/resources/images/boxmodel1.png)

---

# CSS Box Model

- 이런 애들을 CSS Box Model이라 합니다.(뭔가 거창해보이네요)
- Box Model의 개념을 잘 이해해야만이 나중에 미세한 `CSS` 스타일링을 잘할 수 있습니다.

```CSS
.box {
    width: 200px;
    height: 50px;
    margin: 25px;
    padding: 20px;
    border: 10px;
}
```

---

# 얘네들도 각 포지션 별로 지정할 수 있어요.

- 각각 `top`, `left`, `right`, `bottom`이 존재합니다.

```CSS
.box {
    margin-top: 20px;
    padding-left: 10px;
    border-bottom: 5px;
}
```

---

# 또한 속기 속성을 다음과 같이 쓸 수도 있습니다.

```CSS
.box {
    margin: 20px 10px 5px 5px;
    padding: 20px 10px 5px 5px;
    border: 5px solid red;
}
```

- `margin`, `padding` 뒤에 붙는 애들은 시계 방향으로 돌아갑니다.
- `border`는 다른 애들과 조금 다른데 굵기 뒤에 윤곽선 모양, 색상 순으로 들어갑니다.

---

# 이제 마지막 실습을 해봅시다.

- 위에서 배운 내용으로 프로필을 수정해볼거에요.
- `<br>` 태그를 사용하지 마세요.
- 프로필은 3단 레이아웃으로 구성되어야 합니다.(header, main, footer)
- 모든 엘리먼트는 `id` 혹은 `class`를 가져야 합니다.
- 오늘 배운 내용을 전부 사용해보세요 :)

---

# 다음화 예고

- 다음 주에는 `CSS`를 조금 더 깊게 살펴볼거에요.
- 특히 레이아웃에 대해 공부할텐데, 어려우니 복습을 잘 하셔야 합니다:

```CSS
// 이런걸 배울거랍니다.
#container {
    display: block;
    overflow: hidden;
    position: fixed;
    left: 0px;
    top: 0px;
    z-index: 100;
}
```
