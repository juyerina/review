# JavaScript 

### Index

### 1. 데이터 타입

자바스크립트의 데이터 타입은 다음과 같음.

**원시형 타입**

- 숫자 number
- 문자 string

```
// 문자열은 배열처럼 인덱스를 통해 접근이 가능함 = 유사배열
var str = '안녕하세요';
console.log(str[1]); 
// => '녕'
```

- 불린 boolean

> null, undefined, 숫자 0, 빈 문자열 ""은 모두 false 값을 가진다.

- null
- undefined

> 선언된 변수에 값이 없거나 존재하지 않는 객체의 프로퍼티는 모두 undefined로 반환된다.

**자료형 타입**

- 객체 object
- 배열 array
- 함수 function



### 2. 변수

변수는 `var` 키워드를 이용해 선언한다. 

```js
var aaa;
aaa = 10;

console.log(aaa);
// => 10
```
`var`는 전역변수로 선언된다. 이를 보완하기 위해 ES6에서는 `let`과 `const`가 도입됨.


### 3. 제어문

조건에 따른 조건실행문 `if` 와 `switch`, 반복실행문 `for`와`while` 이 있음.<br>
제어문에서는 별도의 scope를 가지지 못하기 때문에 안에서 선언된 변수는 전역 변수가 된다.<br>


#### 1) 조건문

조건이 참이면 실행하고 거짓이면 동작하지 않음.

**- if문**

```js
var a = 20;

if(a<=20){
	console.log("참참참!");
} else {
	console.log("땡땡땡!");	
}

// => "참참참!"


// 조건을 삼항식으로 간소화 시킬 수도 있다.

var b = 10;
b>20 ? console.log("참참참!") : console.log("땡땡땡!");

// => "땡땡땡!"
```

**- switch문**

실행 조건이 여러 개일 경우

```js
var aa = 10;
switch(aa){
	case 10: 
		console.log("aa = 10");
		break;
	case 20:
		console.log("aa = 20");
	case 30:
		console.log("aa = 30");
		break;
		// break를 만나면 switch 문에서 탈출함.
	default:
		console.log("aa = none");
		// 위에 있는 case와 일치하지 않을 경우
}
```

#### 2) 반복문

**- for문**

조건이 거짓이 될 때까지 반복 실행. 횟수가 정해져 있음.

```js
for(초깃값;조건식;증감식){
	실행문;
}

// ex
for (var i=0; i<=2; i++){
	console.log(i);
}

// console 창
// 0
// 1
// 2
```

*for문의 실행흐름*

변수확인 -> 조건확인 -> 실행구문 -> 증감연산

다중으로도 사용이 가능하다.

```js
for(초깃값;조건식;증감식){
	실행문;
	for(초깃값;조건식;증감식){
		실행문;
	}
}
```



