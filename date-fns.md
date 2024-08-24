# date-fns

`date-fns`는 JavaScript에서 날짜와 시간을 다루기 위한 유틸리티 라이브러리다. 이 라이브러리는 다양한 날짜와 시간 관련 함수들을 제공하여, 날짜 형식 변환, 날짜 계산, 날짜 비교 등을 쉽게 수행할 수 있게 해준다. `date-fns`는 함수형 프로그래밍 스타일을 따르며, 각 함수는 불변성을 유지한다.

## 주요 기능

- **날짜 생성 및 변환**: 문자열을 `Date` 객체로 변환하거나, `Date` 객체를 특정 형식의 문자열로 변환할 수 있다.
- **날짜 계산**: 날짜를 더하거나 빼는 등의 연산을 수행할 수 있다.
- **날짜 비교**: 두 날짜를 비교하여 차이를 계산하거나, 특정 날짜가 다른 날짜보다 이전인지 이후인지 확인할 수 있다.
- **날짜 형식화**: `Date` 객체를 다양한 형식의 문자열로 변환할 수 있다.

## 설치

`date-fns`를 설치하려면 npm 또는 yarn을 사용할 수 있다.

```sh
npm install date-fns
# 또는
yarn add date-fns
```

**사용 예시**

다음은 date-fns의 주요 기능을 사용하는 예시이다.

**날짜 생성 및 변환**

```javascript
import { parseISO, format } from "date-fns";

const isoString = "2023-10-05T14:48:00.000Z";
const date = parseISO(isoString);
console.log(date); // 출력: 2023-10-05T14:48:00.000Z

const formattedDate = format(date, "yyyy-MM-dd");
console.log(formattedDate); // 출력: 2023-10-05
```

**날짜 계산**

```javascript
import { addDays, subMonths } from "date-fns";

const today = new Date();
const nextWeek = addDays(today, 7);
console.log(nextWeek); // 출력: 오늘 날짜로부터 7일 후의 날짜

const lastMonth = subMonths(today, 1);
console.log(lastMonth); // 출력: 오늘 날짜로부터 1개월 전의 날짜
```

**날짜 비교**

```javascript
import { isBefore, isAfter } from "date-fns";

const date1 = new Date(2023, 9, 5);
const date2 = new Date(2023, 9, 10);

console.log(isBefore(date1, date2)); // 출력: true
console.log(isAfter(date1, date2)); // 출력: false
```

**날짜 형식화**

```javascript
import { format } from "date-fns";

const date = new Date(2023, 9, 5);
const formattedDate = format(date, "yyyy-MM-dd");
console.log(formattedDate); // 출력: 2023-10-05
```
