```table-of-contents
```
# 발단
- liveScript
	- 넷스케이프사
	- 브랜든 아이크
- 썬 마이크로 시스템스(오라클)가 JavaScript로 변경

# JS 특징 나열
## JavaScript
- 동적으로 HTML콘텐츠를 운영
	- 실시간
	- 상호작용
	- 동적으로 변경
- 객체 기반의 스크립트 언어
	- 웹 브라우저에서 해석되는 인터프리터 언어
- Node.js와 같은 프레인워크
	- 서버 프로그래밍에도 사용 가능

## 특징
- 동적
	- 동적 타이핑
		- 변수를 할당할 때 타입이 결정
		- 선언할 때 x
		- TypeScript - ES6의 확장으로 정적 타이핑 지원
- 타입을 명시할 필요가 없음
	- 비교할 때,
		- 타입 비교x | ==
		- 타입 비교o | ===
- 인터프리터 언어
	- 브라우저가 소스코드를 해석해서 실행
- 표현
	- 객체 지향 프로그래밍
		- 선언과 생성 동시 처리
		- Prototype 기반
			- 객체가 공유하는 메소드 정의
	- 함수형 프로그래밍
		- 함수 자체가 객체
		- 화살표 함수를 통해 람다식 지원
		- High-Order Function 지원
			- 함수를 인수, 인자로 전달 가능 || 변수로 취급 가능
- HTML의
	- 내용
	- 속성
	- 스타일
	- 변경 가능
- 이벤트
	- 처리 가능
	- 상호 작용 가능
- 서버와 실시간 통신이 가능

## JS의 용도
- HTML 컨텐츠 동적으로
	- 생성
	- 삭제
	- 변경
- 이벤트 반응 동작 구현
- HTML, CSS 요소 변경
- 입력값 계산 || 검증
- 대화형 컨텐츠 구현
	- 게임
	- 애니메이션
- 웹 서버 통신 구현


## JS의 확장
- BackEnd FrameWorks
	- Node.js
	- Next.js
- FrontEnd FrameWorks
	- React.js
	- Vue.js
	- Angular.js
- jQuery
	- 자바스크립트 라이브러리
		- 클라이언트 스크립트를 단순화 할 수 있도록 설계
	- 프론트엔드 프레임워크의 등장
		- 가상 돔 활용 -> 성능 향상
		- 필요성 저하
- JSON - JavaScript Object Notation
	- 속성 - 값 형태로 개발형 표준 포맷
		- 데이터 오브젝트를 전달하는 것이 목표
	- 브라우저 - 서버의 통신 (AJAX)
		- XML을 대체하는 주요 데이터 포맷

<hr>
# JS의 기본 문법

## JS가 지원하는 프로그램 구성요소
1. 요소
	1. 변수
	2. 함수
	3. 객체
	4. 클래스
2. 문법
	1. 반복문
	2. 조건문
3. 자료구조
	1. 배열
	2. 리스트
	3. 맵
4. 비동기 처리 지원
5. HTTP 처리
	1. 요청
	2. 응답
6. HTML 문서에 접근할 수 있는
	1. 내장 객체
	2. 함수
7. DOM을 다룰 수 있음
	1. 6번의 요소들로 DOM에 접근 할 수 있음
8. JSON 구문
	1. 객체를 정의함

# 작성 방법

- HTML에 포함
	- JS는 웹 브라우저에서 독립적으로 실행될 수 없음
- HTML에 포함 시키는 방식
	- 인라인 JS
		- Attribute에서 지정
		- `<button type="button" onclick="func()"></button>`
	- 웹 문서 내장
		- Tag - Script
		- 위치
			- head
				- 함수의 정의
				- 실행 -> body 컨텐츠
			- body
				- body 컨텐츠 -> 실행 보장
	- 외부 파일 참조
		- 
		  

<hr>
# 변수
1. 사전에 정의 없이 사용할 수 있다
	1. 단, 전역변수로 사용하려면 미리 선언하여야 함
2. 변수 선언에는 자료형을 지정하지 않음
3. 변수는 문자로만 선언하여야 함 && 숫자로 시작할 수 없다
	1. $
	2. _
	3. 대소문자
	4. 사용 가능
## var
1. 기본적으로 제공하던 변수 선언자
2. 특징
	1. 재 할당 가능
	2. 재 선언 가능
## let
1. ES6 에서 추가된 선언자
2. 특징
	1. 재 할당 가능
	2. 재 선언 불가
## const
1. ES6 에서 추가된 선언자
2. 특징
	1. 재 할당 불가
	2. 재 선언 불가


<hr>
# 자료형

## 기본형 - Primitive Type
1. 숫자
	1. Infinity
	2. NaN
		1. Not a Number
2. 문자열
	1. "" 
		1. Double quote
	2. '' 
		1. Single pQuote
	3. ``- Back Quote
		1. 템플릿 문자열 표현
			1. ES6 추가
3. 불리안
	1. True
	2. False
4. null
	1. Null Type
5. undefined type
	1. 할당되지 않은 상태

## 형 변환
### 암시적 형 변환
	1. 자바 스크립트 엔진이 자동으로 수행
```js
let number = 20;
let string = '24';
let resultA = number + string;
let bool = true;
let resultB = number + bool;
console.log(resultA);
console.log(resultB);
type_casting_imp.js
// ‘20’ + ‘24” = 2024 문자열
// 20 + 1 = 21 숫자
```
### 명시적 형 변환
	1. 개발자가 직접 형 변환
```html
<!DOCTYPE html>
<html>
<body>
<script>
var valueA = 20;
// 숫자형을 문자열로 변환
valueA = String(valueA);
document.write(valueA + ‘ ‘ + typeof valueA + "<br><br>");
var valueB = true;
// 불리언을 문자열으로 변환
valueB = String(valueB);
document.write(valueB + ‘ ‘ + typeof valueB + "<br><br>");
var valueC = ‘24’;
// 문자열을 숫자형으로 변환
valueC = Number(valueC);
document.write(valueC + ‘ ‘ + typeof valueC + "<br><br>");
</script>
</body>
</html>
```


# 참조형
## 객체 리터럴
- 객체 직접 생성
	- 객체 하나 생성
## Object
- Object 객체를 이용하여, 사용자 객체 생성
	- 객체 하나 생성
## new
- 생성자 함수를 사용
	- 객체 정의
	- new 를 통해, 객체를 생성
	- 다수 생성 가능


## Class
- class 키워드를 이용
	- 객체를 정의
	- 객체 생성
	- 다수 생성 가능


<hr>
# 연산자
## 비교 연산자
- ==
	- !=
- ===
	- !==

<hr>

# 출력 함수

## prompt
- Value를 입력 받는다
## confirm
- True
- False
## alert
- 사용자에게 message 를 전달함

## write
- HTML 파일에 쓰기
	- document.write();
	- 이전의 HTML은 삭제
```
<!DOCTYPE html>
<html>
<body>
	<h1 id="test">Table Example.</h1>
	<script>
		function func() {
			var title1 = "멀티미디어 배움터2.0";
			var title2 = "모바일 멀티미디어";
			var title3 = "자바입문: 이론과 실습";
			
			document.write("<table border='1'>");
			document.write("<caption> 베스트셀러 </caption>");
			document.write("<tr>");
			document.write("<th> 순위 </th>");
			document.write("<th> 제목 </th>");
			document.write("</tr>");
			document.write("<tr> <td> 1 </td> <td> " + title1 + " </td> </tr>");
			document.write("<tr> <td> 2 </td> <td> " + title2 + " </td> </tr>");
			document.write("<tr> <td> 3 </td> <td> " + title3 + " </td> </tr>");
			document.write("</table>");
			}
	</script>
	<button type="button" onclick="func()">클릭하세요!</button>
</body>
</html>
```

## console.log
- JS code를 디버깅 할 때 많이 사용하는 함수
- 크롬 브라우저에서 디버깅
- 개발자 모드에서 console 진입



<hr>

# 객체

## 특징
- 자바스크립트 객체는 속성 (property)과 메소드 (method)를 가짐
- 객체의 속성 값으로 또 다른 객체 포함 가능
	- 계층적 구조
- 자바스크립트 내장 객체와 사용자가 정의한 객체 사용

## 내장 객체
- 자바스크립트에서 기본적으로 제공되는 객체
	- Array
	- Date
	- Math
	- String
- 웹 브라우저가 제공하는 window와 navigator (다음 장에서 설명)

## Array 객체

### 배열의 생성
- new 연산자 이용
- 배열 리터럴을 이용

### 배열 요소의 접근

- 배열이름[인덱스]와 같이 각괄호 ([ ])를 이용해 접근

1. 
```js
var book_arr = new Array(“자바스크립트", “E516", 2, 34);
// 배열의 내용
// book_arr[0]: " 자바스크립트 "
// book_arr[1]: “E516“
// book_arr[2]: 2
// book_arr[3]: 34
var book_arr2 = ["자바스크립트", “E516", ", 2, 34];
var arr100 = new Array(100); // 요소 갯수가 100인 배열 생성
```

2. 
```js
<html><body>
<script type = "text/javascript" >

var arr = new Array("one", 2, "3", 4, "five");
// arr 내용 = ["one", 2, "3", 4, "five"]

arr[6] = 6;
arr[7] = "seven";
arr[9] = "3+6";
// arr 내용: ["one", 2, "3", 4, "five", undefined, 6, "seven", undefined, "3+6"]

document.write("length of array: " + arr.length + "<br/>");

document.write("arr = [");
for(i=0;i<arr.length;i++) document.write(" " + arr[i] + " ");
document.write("] <br/> ");

arr.length = 3;
document.write("length of array: " + arr.length + "<br/>");

document.write("arr = [");
for(i=0;i<arr.length;i++) document.write(" " + arr[i] + " ");
document.write("] <br/> ");

document.write("arr[" + 100 + "]: " + arr[100] + "<br/>");
document.write("length of array: " + arr.length + "<br/>");

arr[100] = 100;
document.write("arr[" + 100 + "]: " + arr[100] + "<br/>");
document.write("length of array: " + arr.length + "<br/>");

</script>
</body></html>
```

### 배열 객체의 메소드
- reverse()
	- 배열 내 요소들의 순서를 반대로 바꾸는 기능
- sort()
	- 배열 내 요소들의 순서를 오름차순으로 정렬
	- 숫자가 문자보다 앞에 정렬됨
- join()
	- 배열 내 요소를 모두 합쳐서 하나의 문자열로 만들어 줌 
	- 이 때 요소 사이에 끼워 넣을 문자열 지정 가능
- concat()
	- 배열의 뒤에 요소를 붙혀서 (concatenation) 배열의 내용
추가
- slice()
	- 배열의 요소들 중 일부만을 배열로 만들어서 리턴.
	- 사용 형식은 array.slice(첫 요소 index, 마지막 요소 index+1)

## 사용자 정의 객체

### 객체 생성 및 특징

- 사용자 정의 객체 생성
	- 객체 리터럴로 직접 생성
	- Object 객체를 이용하여 사용자 객체 생성
	- 생성자 함수를 이용하여 객체 정의하고 new를 통해 객체 생성
	- class 키워드를 이용하여 클래스 정의하고 객체 생성
- 객체 생성 후 속성 및 메소드를 언제라도 추가 가능
- 점(dot, ".") 연산자를 붙혀서 속성과 메소드 접근
- 다양한 변수 형을 속성으로 사용 가능
	- ex) 문자열과 숫자형을 동시에 사용 가능
- 객체의 계층적 구조
	- 객체의 속성 값으로 또 다른 객체 사용 가능

### 객체의 접근 방식
1. 점(dot, ".") 연산자를 이용
2. 배열 표시 방식("[ ]")

- 속성을 삭제하기 위해서는 delete라는 명령어 이용
```js
// 객체의 속성 접근 방법
var property1 = book.title;
var property2 = book.info.price;

// 혹은
var property3 = book["title"];
var property2 = book.info["price"];

// 객체의 속성 삭제 방법
delete book.title;
delete book.info.price;
  ```

### 객체의 접근
- 객체에 포함된 속성의 개수나 이름을 모르더라도 객체 내의 모든 속성을 접근할 수 있는 방법
- 객체 접근 방식은 점(".")에 의한 접근은 불가능하며 배열 방식("[ ]") 사용
- foreach 반복문은 배열 객체에만 사용 (ES6부터는 Map, Set 지원)

#### 개선 반복문
##### for in
- 속성의 이름을 모르기 때문에 점(".") 접근 방식은 사용 불가
``` js
var obj = { a: '가', b: '나', c: '다' };

for (var key in obj) {
	console.log (key, obj[key]); // a 가, b 나, c 다
}
```
##### for of
- Symbol.iterator 속성을 가지고 있는 컬렉션 전용 반복문 for of 문과 비교
```js
var iterable = [10, 20, 30];

for (var value of iterable) {
	console.log(value); // 10, 20, 30
}
```