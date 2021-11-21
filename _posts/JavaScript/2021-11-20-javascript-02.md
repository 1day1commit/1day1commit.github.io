---
layout: post
title: 'JavaScript String'

categories:
  - JavaScript

tags:
  - [JavaScript]

toc: true

permalink: /:title/

date: 2021-11-21T12:30:32+0900
last_modified_at: 2021-11-21T12:30:32+0900
---

<br>
<br>

# String

## 대소문자 바꾸기

`toUpperCase` 는 문자열을 모두 대문자로 바꿔주는 메서드 입니다.

`toLowerCase` 는 문자열을 모두 소문자로 바꿔주는 메서드 입니다.

두 메서드 모두 String 에서 제공하는 메서드입니다. 또한 원래의 배열에 영향을 주지 않습니다.

<br>

## 문자 길이

배열의 길이를 알고싶을 때 `length` 라는 속성을 사용합니다.

문자열도 `length` 라는 속성으로 길이를 알 수 있습니다.

회원가입을 할 때 이름이 10자가 넘어가는지, 핸드폰 번호가 10자리 또는 11자리가 아닌지 체크할 때 등등 자주 사용하는 속성입니다.

## 문자열 찾기

`indexOf` 메서드는 문자열에 특정 문자열이 들어있는지 확인하고, 만약 있다면 몇 번째 순서에 해당 문자열이 있는지 알려줍니다.

해당 문자열이 없다면 -1 을 반환합니다.

예를들어 댓글에 욕설이 포함되면 달지 못하도록 차단할 때 사용할 수 있습니다.

```javascript
let info = '안녕하시요 나는 정태영';
let firstChar = info.indexof('안녕하시요');

if (firstChar !== -1) {
  info =
    info.slice(0, firstChar) +
    '안녕하세요' +
    info.slice(firstChar + 5, info.length);
}

console.log(info);
```

위 코드는 '안녕하시요' 라는 오타를 '안녕하세요' 라고 바꿔주는 코드입니다.
