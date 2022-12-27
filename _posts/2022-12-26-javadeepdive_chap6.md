---
layout: post
title: Javascript deepdive 스터디 Chapter 6.
---

모던 자바스크립트 Deep Dive
자바스크립트의 기본 개념과 동작 원리

스터디를 시작합니다.
제가 맞은 부분인 6장부터 시작하고 다른 장도 차근차근 TIL형식으로 이어나갈 예정입니다.

6장 데이터 타입

1. 숫자타입
2. 문자열타입
3. 템플릿 리터럴
4. 불리언 타입
5. undefined 타입
6. null 타입
7. 심벌타입
8. 객체타입
9. 데이터 타입의 필요성
10. 동적 타이핑

숫자 number 타입 - 숫자, 정수와 실수 구분 없이 하나의 숫자 타입만 존재
JS에서 숫자타입을 취급하는 특성
ECMAScript 사양에 따르면 숫자 타입의 값은 배정밀도 64비트 부동소수점 형식을 따른다. 
즉, 모든 수를 실수로 처리하며, 정수만 표현하기 위한 데이터 타입인 integer type이 별도로 존재하지 않는다.

// 아래는  모두 숫자 타입이다.
var integer = 10; 11 정수
var double = 10.12; // 실수
var negative = -20; // 음의 정수

정수, 실수, 2진수, 8진수, 16진수 리터럴은 모두 메모리에 배정밀도 64비트 부동소수점 형식의 2진수로 저
장된다. 자바스크립트는 2진수, 8진수, 16진수를 표현하기 위한 데이터 타입을 제공하지 않기 때문에 이들
값을 참조하면 모두 10진수로 해석된다.
숫자 타입은 추가적으로 세 가지 특별한 값도 표현할 수 있다.
/ 숫자 타입의 세 가지 특별한 값
console.log(10 / 0); Infinity: 양의 무한대
console.log(10 / -0);  -Infinity: 음의 무한대
console.log(1 * 'String'); // NaN NaN: 산술 연산 불가(not-a-number)

문자열string 타입 - 문자열, 숫자로 표현되어 있어도 타입 변환으로 문자로 취급될 수 있음
문자열 데이터는 텍스트 데이터를 나타내는데 사용, 문자열은 0개 이상의 16비트 유니코드 문자의 집합으로 전세계 대부분의 문자를 표현 가능.
다른 타입의 값과 달리 문자열을 따옴표로 감싸는 이유는 키워드나 식별자 같은 토큰과 구분하기 위해서다.
작은 따옴표(’), 큰따옴표(“), 백택(`)을 사용해서 구분.

탬플릿 리터럴
ES6부터 템플릿 리터럴'emplate iteral이라고 하는 새로운 문자열 표기법이 도입되었다. 템플랏 리터럴은 멀터라
인 문자열multi-line string, 표현식 삽입 expression interpolation, 태그드 템플릿lagged template 등 편리한 문자열 처리 기틀 제공한다. 템플릿 리터럴은 런타임에 일반 문자열로 변환되어 처리된다. 백틱으로 구분해서 사용.

`console.log(1 + 2 = ${1 + 2}`); // 1 + 2 = 3 과 같이 표현식을 삽입하려면 ${ } 으로 표현식을 감싼다. 
이때 표현식의 평가 결과가 문자열이 아니더라도 문자열로 타입이 강제로 변환되어 삽입된다.
멀티라인 문자열 - 백슬래시('\')를 사용해 줄바꿈등 공백을 표현할때 사용.

불리언 boolean 타입 - 논리적 참(true)과 거짓(false) 두 가지로 값을 나타낸다
undefined 타입 - var 키워드로 선언된 변수에 암묵적으로 할당되는 값 / 문제가 있기 때문에 비추천 ( 추가 확인 필요)
null 타입 - 값이 없다는 것을 의도적으로 명시할 때 사용하는 값.
심벌symbol 타입 - ES6에서 추가된 7번째 타입 ( 추후 다른 장에서 설명 예정 )
객체 타입 - 객체, 함수, 배열 등 ( 11장에서 설명예정)


데이터 타입의 필요성
타입 분류에 따른 메모리 공간확보와 정보값을 읽을 메모리 공간 크기 결정을 위해(그림설명으로 이해가 불가하여 다른 예시 찾아볼 예정)
타입에 따른 2진수 해석 방식을 결정하기 위해

동적타이핑의 이해
JAVA나 C언어의 경우 정적 타이핑으로 변수 선언시 타입도 함께 결정되지만 JS는 다양한 타입을 선언하고 타입을 동적으로 변경할수 있다. 그러나 이로인해 문제가 발생할 수 있고 프로그램의 안정성이 떨어진다.
( 추가적인 이해 후에 내용 더할 예정)


전체적으로 기본적인 내용이라서 외워야하는 부분이고, 이해하지 못하더라 계속해서 반복 학습을 해야할 듯합니다.

2022.12.26