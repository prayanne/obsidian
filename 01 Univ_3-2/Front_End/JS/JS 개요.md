
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
		- <button type="button" onclick="func()"></button>
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
```
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
```
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