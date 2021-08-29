---
title: "CSS `accent-color`"
date: 2021-08-30 09:00:00 +0900
categories: css
---

코드 한 줄로 기본 제공되는 HTML 양식 입력에 브랜드 색상을 가져온다.

오늘날의 HTML 양식 요소는 [사용자 지정이 어렵다](https://codepen.io/GeoffreyCrofte/pen/BiHzp). 마치 몇 가지 또는 사용자 지정 스타일을 선택할 수 없거나, 입력 스타일을 재설정하여 처음부터 다시 구축하는 것 같은 느낌이 든다. 처음부터 다시 쌓는 것은 예상했던 것보다 훨씬 더 많은 작업이 된다. 요소 상태에 대한 잊혀진 스타일([indeterminate](https://developer.mozilla.org/en-US/docs/Web/CSS/:indeterminate), 지켜보고 있다)과 기본 제공 접근성 기능의 손실로 이어질 수도 있다. 브라우저에서 제공하는 기능을 완전히 재생성하는 것은 수행하려는 작업보다 더 많은 작업이 될 수 있다.

```
accent-color: hotpink;
```

[CSS UI 규격](https://www.w3.org/TR/css-ui-4/#widget-accent)의 CSS `accent-color`는 CSS 줄로 요소들에 색조를 더하여 브랜드를 요소 안으로 끌어들이는 방법을 제공함으로써 사용자 지정 노력을 덜어준다.

![확인란, 라디오 버튼, 범위 슬라이더 및 진행 요소가 모두 핫핑크색으로 칠해진 액센트 컬러 데모의 밝은 테마 스크린샷](https://web-dev.imgix.net/image/vS06HQ1YTsbMKSFTIPl2iogUQP73/CfSS3F1XUsfCHIB86xeE.png?auto=format&w=1600)

[데모](https://codepen.io/web-dot-dev/pen/PomBZdy)

`accent-color` 속성은 color-scheme과 함께 동작하여, 저작자에게 밝은 요소와 어두운 요소 모두에 색조를 더한다. 다음 예에서 사용자는 어두운 테마를 활성화하고 페이지에는 `color-scheme: light dark`를 사용하며 어두운 테마 핫핑크 색조 컨트롤에도 동일한 `accent-color: hotpink`를 사용한다.

![체크 버튼, 라디오 버튼, 범위 슬라이더 및 progress 요소가 모두 핫핑크색으로 칠해진 액센트 컬러 데모의 어두운 테마 스크린샷](https://web-dev.imgix.net/image/vS06HQ1YTsbMKSFTIPl2iogUQP73/3gxeeZoSLY34tsMxkyt9.png?auto=format&w=1600)

[데모](https://codepen.io/web-dot-dev/pen/PomBZdy)

### 브라우저 지원

이 글 2021/8/11 현재 크롬 93+ 및 Firefox 92+는 `accent-color`를 지원한다.

## 지원되는 요소

현재, 네 가지 요소([checkbox](https://web.dev/accent-color/#checkbox), [radio](https://web.dev/accent-color/#radio), [range](https://web.dev/accent-color/#range) 및 [progress](https://web.dev/accent-color/#progress))만 `accent-color` 속성을 통해 색조가 적용된다. [https://accent-color.glitch.me](https://accent-color.glitch.me) 에서 각각 밝은 색상과 어두운 색상으로 미리 볼 수 있다.

경고: 다음 데모의 요소가 모두 같은 색이면 브라우저에서 아직 액센트 색상을 지원하지 않는 것이다.

### Checkbox

<div style="height: 500px; width: 100%"><iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading=lazy src="https://codepen.io/web-dot-dev/embed/dyWjGqZ?height=500&theme-id=light&default-tab=result&editable=true" style="height: 100%; width: 100%; border: 0;" title="Pen dyWjGqZ by web-dot-dev on Codepen"></iframe></div>

### Radio

<div style="height: 500px; width: 100%"><iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading=lazy src="https://codepen.io/web-dot-dev/embed/WNjKrgB?height=500&theme-id=light&default-tab=result&editable=true" style="height: 100%; width: 100%; border: 0;" title="Pen WNjKrgB by web-dot-dev on Codepen"></iframe></div>

### Range

<div style="height: 500px; width: 100%"><iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading=lazy src="https://codepen.io/web-dot-dev/embed/yLbqeRy?height=500&theme-id=light&default-tab=result&editable=true" style="height: 100%; width: 100%; border: 0;" title="Pen yLbqeRy by web-dot-dev on Codepen"></iframe></div>


### Progress

<div style="height: 500px; width: 100%"><iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading=lazy src="https://codepen.io/web-dot-dev/embed/rNmrxqL?height=500&theme-id=light&default-tab=result&editable=true" style="height: 100%; width: 100%; border: 0;" title="Pen rNmrxqL by web-dot-dev on Codepen"></iframe></div>

## 대비 보장

액세스할 수 없는 요소가 존재하지 않도록 하려면 `accent-color`를 지원하는 브라우저에서 사용자 정의 악센트와 함께 사용할 [적합한 대비 색상](https://webaim.org/articles/contrast/)을 결정해야 한다. 다음은 Chrome 94(왼쪽)와 Firefox 92 Nightly(오른쪽)의 알고리즘 차이점을 보여주는 스크린샷이다.

![파이어폭스와 크롬을 나란히 찍은 스크린샷으로, 다양한 색상과 어둠으로 전체 스펙트럼의 확인란을 렌더링](https://web-dev.imgix.net/image/vS06HQ1YTsbMKSFTIPl2iogUQP73/DJhB56n10Eh8O29RsRdE.png?auto=format&w=1600)

여기서 가장 중요한 것은 브라우저를 신뢰하는 것이다. 브랜드 색상을 제공하고 이것이 현명한 결정을 내릴 것이라고 믿자.

⭐️ 브라우저는 어두운 테마에서 색상을 변경하지 않습니다.

## 추가: 더 많은 색조

이 4가지 폼 요소보다 더 많은 색조 적용을 하는 방법이 궁금한가? 다음은 색조 조정되는 최소 샌드박스이다.

 * 포커스 링
 * 텍스트 선택 강조 표시
 * 표식기 나열
 * 화살표 표시기 (웹킷에만 해당)
 * 스크롤 막대 엄지손가락 (Firefox 전용)

```
html {
  --brand: hotpink;
  scrollbar-color: hotpink Canvas;
}

:root { accent-color: var(--brand); }
:focus-visible { outline-color: var(--brand); }
::selection { background-color: var(--brand); }
::marker { color: var(--brand); }

:is(
  ::-webkit-calendar-picker-indicator,
  ::-webkit-clear-button,
  ::-webkit-inner-spin-button,
  ::-webkit-outer-spin-button
) {
  color: var(--brand);
}
```

<div style="height: 500px; width: 100%"><iframe allow="camera; clipboard-read; clipboard-write; encrypted-media; geolocation; microphone; midi;" loading="lazy" src="https://codepen.io/web-dot-dev/embed/RwVBreJ?height=500&amp;theme-id=light&amp;default-tab=result&amp;editable=true" style="height: 100%; width: 100%; border: 0;" title="Pen RwVBreJ by web-dot-dev on Codepen"></iframe></div>

### 잠재적 미래

규격은 이 문서에 표시된 네 가지 요소로 `accent-color`를 적용하는 것을 제한하지 않으며 나중에 더 많은 지원을 추가할 수 있다. `<select>`에서 선택한 `<option>`과 같은 요소를 `accent-color`로 강조 표시할 수 있다.

웹에 다른 어떤 색조를 적용하고 싶은가? 당신의 선택자를 @argylink로 트윗을 보내주면 이 글에 추가될 수 있다!

---

원문: [CSS `accent-color`](https://web.dev/accent-color/)
