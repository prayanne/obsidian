```table-of-contents
```
# 정의
- 입력을 받아서 특정한 작업을 수행하여, 결과를 반환하는 명령들의 집합

# 종류
1. 자바스크립트 내장 함수
	1. setTimeout(function, millisecond)
	2. eval(string)
2. 사용자 정의 함수

## 사용자 정의 함수 선언의 특징
- 동일 여부 검사 x
	- 매개 변수
	- 인수 타입
- 개수 확인 x
	- 매개 변수
	- 인수의 개수
	- 다른 경우
		- undefined - 적게 들어옴
		- 무시 - 많게 들어옴

<hr>

# 함수 구문

## 함수 선언식
1. function 을 선언
2. 함수명 기재
3. 호이스팅 됨

## 함수 표현식
1. 변수를 선언
2. 함수 대입
3. 호이스팅 되지 않음

## 호이스팅
- 프로그램에서 변수나 함수를 호출하는 코드가 함수 선언보다 위에 있음에도 불구하고 마치 선언된 코드가 위에 있는 것처럼 동작하는 자바스크립트 기능
- 자바 스크립트는 코드를 실행하기 전에 준비 단계에서 함수를 미리 찾아 생성

<hr>

# 자바 스크립트 내장 함수
- eval
	- 문자열 입력을 계산 || 실행
		- 결과 반환
		- `eval("1+2+3"); // 6 반환`
- paseInt()
- parseFloat()
- setTimeout()



# 함수 선언식
```js
function name(a){}
	let b = a + 10;
	return b;
}
```

# 함수 표현식
```js
var func = function [name] (a) {
	let b = a + 10;
	return b;
};
```

# 익명 함수
- 함수 이름 없이 만들어 한 번만 사용
```js
let greeting = function( name ){
	console.log(“안녕하세요 ” + name);
};

greeting(“홍길동”);
```

# 화살표 함수
- 자바 언어의 람다식(lamda expression)과 유사하며 ES6에 추가
- `let func = (매개 변수) => 반환값;`
``` js
const funcAdd = ( a, b ) => {
	return a + b;
};
console.log(funcAdd(3, 5));
```
- 매개변수가 한 개인 경우 소괄호 생략 가능
``` js
const funcAdd = a => {
	return a + 100;
};
console.log(funcAdd(3));
```
- 처리를 한 행으로 반환하는 경우 return 생략 가능
 ``` js
 // 생략
 const funcAdd = ( a, b ) => a + b;
 
 // return
 const funcAdd = ( a, b ) => return a + b;
  ```

# CallBack function
- 다른 함수의 매개변수로 전달할 수 있는 함수
- 매개변수로 함수를 일단 받음
	- 때가 되면 나중에 호출
- Event Dribble을 할 때
	- GUI가 특징

- 상황에 따라 필요한 다른 함수를 실행하고 싶을 때 활용
``` js callback_function.js
function mainFunc(callback) {
	console.log( “main Function”);
	callback();
}

function subFunc( ) {
	console.log( “sub Function”);
}

mainFunc(subFunc);

```
- 이벤트 처리에도 활용
``` js
  document.queryselector("#callback-btn")
  .addEventListener("click", function() {
	console.log(“Clicked the button!");
});
  ```

<hr>

# 스코프
- 변수와 함수가 접근 가능한 범위
	- 영역의 개념
## 종류
- 전역 / 글로벌 스코프(Global Scope)
	- 전역 변수로서 어디서든 접근 가능
	- 함수 영역 외부의 전역에 변수나 함수를 선언, 자바스크립트는 시작점(Entry Point) 없음
- 지역/함수 스코프(Local Scope or Function Scope)
	- 해당 함수내에서만 접근 가능
- 블록 레벨 스코프(Block Level Scope)
	- let과 const로 선언된 변수 해당
	- 해당 변수가 선언된 블록(중괄호{})에서만 접근 가능
-  스코프 체인(Scope Chain)
	- 중첩 함수의 경우 내부함수는 외부함수의 변수에 접근 가능

<hr>

# 자바스크립트 객체

## Feature
- 자바스크립트 객체는 속성 (property)과 메소드 (method)를 가짐
- 객체의 속성 값으로 또 다른 객체 포함 가능
	- 계층적 구조
- 자바스크립트 내장 객체와 사용자가 정의한 객체 사용

## 내장 객체
- 자바스크립트에서 기본적으로 제공되는 객체
	- Array, Date, Math, String
- 웹 브라우저가 제공하는 window와 navigator (다음 장에서 설명)
- Date 객체
	- 사용자의 컴퓨터에서 제공되는 날짜와 시간을 알아내거나 설정
- Math
	- 수학 계산을 위해 기본적으로 제공되는 객체
		- 별도의 선언이나 생성없이 바로 사용 가능
		- 상수 값은 Math 객체의 속성으로 제공
		- 주요 수학 함수는 Math 객체의 메소드로 제공

|     |     |
| --- | --- |
|     |     |
