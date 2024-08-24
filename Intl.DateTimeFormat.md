# Intl.DateTimeFormat

Intl.DateTimeFormat은 JavaScript의 국제화 API(Internationalization API)에서 제공하는 클래스이다. 이 클래스는 날짜와 시간을 특정 형식으로 로컬라이즈(현지화)하여 출력할 수 있도록 도와준다. 다양한 옵션을 설정하여 날짜와 시간을 형식화할 수 있다.

## 기본 사용법

```javascript
const formatter = new Intl.DateTimeFormat("locale", options);
const formattedDate = formatter.format(date);
```

- locale: 출력할 언어와 지역을 지정한다.
- options: 날짜와 시간을 어떻게 형식화할지를 설정하는 객체이다.

options 객체에는 다음과 같은 속성을 설정할 수 있다.

- <span style="color: red;">&#9679;</span> **year**: 연도의 표시 방법을 지정한다.

  - `"numeric"`: 숫자 형식 (예: 2024)
  - `"2-digit"`: 두 자리 연도 형식 (예: 24)

- <span style="color: green;">&#9679;</span> **month**: 월의 표시 방법을 지정한다.

  - `"numeric"`: 숫자 형식 (예: 8)
  - `"2-digit"`: 두 자리 숫자 형식 (예: 08)
  - `"long"`: 전체 이름 (예: August)
  - `"short"`: 약어 (예: Aug)
  - `"narrow"`: 가장 짧은 형식 (예: A)

- <span style="color: blue;">&#9679;</span> **day**: 날짜의 표시 방법을 지정한다.

  - `"numeric"`: 숫자 형식 (예: 7)
  - `"2-digit"`: 두 자리 숫자 형식 (예: 07)

- <span style="color: orange;">&#9679;</span> **hour**, **minute**, **second**: 시간의 시각 표시 방법을 지정한다.

  - `"numeric"`: 숫자 형식 (예: 1, 2, 3, ...)
  - `"2-digit"`: 두 자리 숫자 형식 (예: 01, 02, 03, ...)

- <span style="color: purple;">&#9679;</span> **weekday**: 요일의 표시 방법을 지정한다.
  - `"narrow"`: 짧은 형식 (예: M, T, W, ...)
  - `"short"`: 약어 (예: Mon, Tue, Wed, ...)
  - `"long"`: 전체 이름 (예: Monday, Tuesday, Wednesday, ...)
