## 리터럴과 변수, 상수, 테이터 타입
데이터 타입을 다루기 전에 먼저 변수와 상수 리터럴에 대해 알아봅시다. 데이터를 보관하는 메커니즘입니다.

### 변수와 상수
ES6에서는 Block-lever scope를 갖는 변수 let과 상수 const를 지원한다.

#### 변수
변수란 이름을 붙인 값입니다. 변수이 암시하듯 값은 언제든 바뀔 수 있습니다.
변수의 기본 형식입니다.
```
    var currentTemc = 22;
    let currentTemc = 22;
```
변수 currentTemc 생성(선언)하고 초깃값을 할당하는 두가지 일을 합니다. currentTemc 초기값은 언제든 바뀔 수 있습니다.
```
    currentTemc = 21;
```
변수를 선언할 때 꼭 초깃값을 지정해야하는 건 아닙니다. 초깃값을 설정하지않으면 암시적으로 undefined가 할당 됩니다.
```
    var currentTemc;

    console.log(currentTemc == undefined);
```
let 문 하나에서 변수 여러 개를 선언할 수 있습니다.
```
    let target,room1;
```

#### 상수
변수와 마찬가지고 값을 할당받을 수 있지만 한번 할당한 값은 변경할 수 없습니다.
```
    const ROOM = 22;

    ROOM = 21;

    Uncaught TypeError: Assignment to constant variable.
```
절대적인 규칙은 아니지만 상수 이름에는 보통 대문자와 밑줄만 사용합니다. 이런 규칙을 따르면 코드에서 상수를 찾기도 쉽고 상수의 값을 바꾸려하지도 않습니다.

### 식별자 이름
변수와 상수, 함수 이름을 식별자라 부릅니다. 식별자에는 규칙이 있습니다.
* 식별자는 반드시 글자나 달러 기로($), 밑줄로 시작해야합니다.
* 식별자에서 글자와 숫자, 달러 기호, 밑줄만 쓸 수 있습니다.
* 식별자는 최소 하나의 문자로 구성되어야합니다.
* 유니코드 문자도 쓸 수 있습니다.
* 예약어는 식별자로 쓸 수 없습니다.

<small>**예약어**</small>
<small>예약어는 아직 특별한 쓰임새는 없지만 미래에 키워드로 쓸 가능성이 있어서 예약해 둔 것입니다.</small>
```
- abstract
- boolean
- byte
- char
- class
- const
.
.
```

#### 식별자 선업법
* 카멜케이스
     * CurrentTempc, anIdentifierName와 같이 문자와 문자 사이를 대문자를 써 경계를 표시합니다.
* 스네이크 케이스
    * current_temp_c, an_indentiFier_name와 같이 문자와 문자사이를 언더스코어로 연결해 표시합니다.

<small>식별자는 대문자로 시작해서는 안됩니다. 대문자로 시작할 경우 클래스입니다.</small>


### 리터럴
