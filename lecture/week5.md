# Front-end Workshop
## ~ Week 5 ~

---

# 5주차가 밝았습니다.

- 지난 주에는 `CSS`의 기초적인 부분에 대해 살펴봤습니다.
- `HTML`보다는 조금 더 어렵다는걸 느끼셨죠?
- 익숙해지기 위해서는 지속적인 연습이 필수입니다.
- 이번 주에는 `CSS` 레이아웃에 대해 공부해보겠습니다.
- 그 전에 각자 해온 숙제를 `Slack` 채널에 올려주세요 :)

---

# 레이아웃의 기초 - display

- `CSS`에는 `display`라고 불리는 속성이 있습니다.
- 이 친구는 해당 엘리먼트가 어떻게 보여질지 혹은 정렬할지를 결정합니다.
- 이전에 `HTML`을 공부할 때 배운 BLE와 ILE에 대한 개념이 필요하죠.
- `BLE`의 기본 `display` 속성은 `block` 입니다.
- `ILE`는 당연히 `inline`이겠죠?

---

# 레이아웃의 기초 - display

- `display` 속성은 엄청나게 많지만 자주 사용하는 것들만 살펴볼게요.
- 첫 번째 속성 값은 `block` 입니다.

```HTML
<span>저는 인라인이에요</span>
<span>저도 인라인이죠</span>
<span class="block-span">하지만 저는 블록입니다.</span>
```

```CSS
.block-span {
    display: block;
}
```

---

# 레이아웃의 기초 - display

- 다음 알아볼 속성은 `inline` 입니다.

```HTML
<div>저는 블록입니다.</div>
<div>저도 블록이에영</div>
<div class="inline-div">하지만 저는 인라인 입니다.</div>
<span>저는 당연히 인라인이겠죠?</span>
```

```CSS
.inline-div {
    display: inline;
}
```

---

# 레이아웃의 기초 - display

- 마지막은 `inline-block`으로 얘는 `inline`이지만 `block` 입니다.
- 예를 들어 `inline` 속성은 `width`, `height`, `margin` 값을 지정할 수 없습니다만 `inline-block`을 사용하면 값을 조절할 수 있습니다.
- 따라서 매우 유용하게 사용할 수 있습니다.


---

# 레이아웃의 기초 - display

```HTML
<div>내가 바로 inline-block이다!</div>
<div>내가 바로 inline-block이다!</div>
<div>내가 바로 inline-block이다!</div>
```

```CSS
div {
    border: 1px solid black;
    display: inline-block;
    width: 50px;
    height: 50px;
    margin: 10px;
}
```

---

# 레이아웃의 기초 - position

- 이번에 알아볼 `CSS` 속성은 `position` 입니다.
- 얘는 엘리먼트의 위치와 상태를 정의합니다.
- 사용 방법은 다음과 같습니다.

```CSS
.just-normal {
    position: static;
}

.im-fixed {
    position: fixed;
}
```

---

# 레이아웃의 기초 - position

- 첫 번째 볼 친구는 `fixed` 입니다. `fixed`로 지정된 엘리먼트는 "화면의" 해당 위치에 딱 붙어서 움직이지 않습니다.
- 위치는 `top`, `bottom`, `left`, `right`로 조절할 수 있습니다.

```CSS
div {
    position: fixed;
    width: 50px;
    height: 50px;
    border: 1px solid black;
    top: 0px;
    left: 50px;
}
```

---

# 레이아웃의 기초 - position

- 두 번째는 `absolute` 입니다.
- `absolute`는 어떻게 보면 `fixed`와 비슷하지만 `fixed`는 화면을 상대적으로 판단하지만 `absolute`는 항상 그 위치에 존재합니다.
- 다음 실습을 통해 이 2개 속성의 차이를 확인해봅시다!

---

# 레이아웃의 기초 - position

```CSS
.fixed {
    position: fixed;
    bottom: 0px;
    right: 0px;
}

.absolute {
    position: absolute;
    bottom: 50px;
    right: 0px;
}
```

---

# 레이아웃의 기초 - position

- 이번에 알아볼 속성은 `relative` 입니다. 기본적으로 아무일도 하지 않는 것 처럼 보이지만 하위 엘리먼트에 `position` 속성을 적용할 경우 정렬 대상이 상위 엘리먼트로 변경됩니다.

```CSS
.relative {
    position: relative;
}

.child-div {
    position: absolute;
}
```

- 실습으로 확인해봅시다.

---

# 레이아웃의 기초 - position

- 마지막 속성은 `static` 입니다. 하는일은 그냥 엘리먼트의 `position`을 초기 상태로 돌리는데 사용할 수 있어요.

```CSS
div {
    position: relative;
}

.just-static {
    position: static;
}
```

---

# 실습 과제

- 여러분은 이제 명함을 만들겁니다.
- 지금까지 배운 내용을 통해 시지온 명함을 만들어주세요.
- 앞/뒷면 모두 존재해야 합니다.
- 이미지는 적당한 것을 사용하셔도 됩니다.

![right](http://cfile2.uf.tistory.com/image/150DDC464FFA4C5A25D357)
