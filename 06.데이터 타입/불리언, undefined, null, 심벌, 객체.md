## 불리언 타입
&emsp; -> 논리적 참, 거짓을 나타내는 true와 false 뿐이다.
```js
var t = true;
console.log(t); // true

var f = false;
console.log(f); // false
```

<br />

## undefined 타입
&emsp; -> undefined 뿐이다.   
> **자바스크립트 엔진이 변수를 초기화하는 데 사용하는 데 사용한다.**   
=> 변수에 참조했을때 undefined면 값이 할당된 적이 없는 초기화 되지 않은 변수라는 것을 알 수 있다.   

*undefined는 개발자가 의도적으로 변수에 할당하면 undefined의 본래 취지와 벗어날 수 있으니 사용하지말자..*

<br />

## null 타입
&emsp; -> null 뿐이다.   
> **변수에 값이 없다는 것을 의도적으로 명시할 때 사용한다.**
=> 변수에 null을 할당하는 것은 변수가 이전에 참조하던 값을 더 이상 참조하지 않겠다는 의미이다.

```js
var name = 'siyeon';

name = null; // 이전 참조를 제거한다.
```
함수가 유효한 값을 반환할 수 있는 경우 명시적으로 null을 반환하기도 한다.
```html
<!DOCTYPE html>
<html>
  <body>
    <script>
      var element = document.querySelector('.name');
      console.log(element); // html에 element가 없기 때문에 null이 출력된다.
    </script>
  </body>
</html>
```
<Br />

## 심벌 타입
&emsp; -> Symbol 함수를 호출해 생성한다.
> 다른 값과 중복이 되지 않는 유일무이한 값이다.   
 => 주로 이름이 충돌할 위험이 없는 객체의 유일한 프로퍼티 키를 만들기 위해 사용된다.

```js
// 심벌 값 생성
var key = Symbol('key');
console.log(typeof key); // symbol

// 객체 생성
var obj = {};

obj[key] = 'value';
console.log(obj[key]); // value
```
33장으로 가면 더 자세히 정리할 것이다.

<br />


## 객체 타입
자바스크립트의 데이터 타입은 크게 원시 타입과 객체 타입으로 분류한다.   
> 자바스크립트를 이루고 있는 거의 모든 것이 객체이다. (지금까지 본 6가지 데이터 타입 외의 값은 모두 객체 타입이다.)