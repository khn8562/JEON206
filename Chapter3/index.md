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
리터럴이라는 단어는 값을 프로그램 안에서 직접 지정한다는 의미
즉 값을 만드는 방법입니다.
```
    Object();
    {};

    Array();
    [];
```


### 원시타입과 객체
자바스크립트의 값은 원기값 또는 객체입니다.
원시값은 불변이며 원시 타입에는 여섯가지가 있습니다.
* 숫자
* 문자열
* 불리언(true, false)
* null
* underfined
* 심볼

여섯 가지 원시 타입 외 객체가 있습니다. 여러가지 형태와 값을 가질 수 있습니다.

* Number
* String
* Boolean
* Array
* Date
* RegExp
* Map와 WeakMap
* Set와 WeakSet

이들은 대응하는 원시 값에 기능을 제공하는 역활을 합니다.

### 숫자
자바스크립트는 10진수, 2진수, 8진수, 16진수의 네 가지 숫자형 리터럴을 인식합니다.
기본적으로 10진수를 표현합니다.
```
    let const = 10;
    let blue = 0x000ff == 255; (16진수);
    let green = 0o0022 == 18; (8진수);
    let inf = Infinity // 무한대를 나타내는 숫자값입니다.
    let nan = NaN; // 숫자가 아님
```
또한 숫자를 대응하는 Number객체에는 중요한 숫자형 값에 해당하는 프로퍼티가 있습니다.
* Number.EPSILON (1에 더 했을 때 1과 구분되는 결과를 만들수 있는 가장 작은 값)
* MAX_SAFE_INTEGER (표현할 수 있는 가장 큰 정수)
* MAX_VALUE (표현할 수 있는 가장 큰 숫자)
* MIN_SAFE_INTEGER (표현할 수 있는 가장 작은 정수)
* MIN_VALUE (표현할 수 있는 가장 작은 숫자)
* NEGATIVE_INFINITY (-Infinity)
* NAN (NAN)
* POSITIVE_INFINITY (Infinity)

위 프로퍼티에 대해서는 16장에서 설명합니다.

### 문자열
자바스크립트에서 문자열은 유니코드텍스트입니다. 유니코드는 텍스트 데이터에 관한 표준이며 사람이 사용하는 언어 대부분의 글자와 심볼에 해당하는 코드 포인트를 포함하고있습니다.
문자열 리터럴에슨 작은따운표, 큰따운표, 백틱을 사용합니다. 백틱은 es6에 도입한 것이며 템플릿 문자열에 사용합니다.


#### 이스케이프
텍스트 데이터를 사용할 때는 항상 텍스트 데이터와 프로그램 자체를 구별할 방법이 필요합니다.
```
    'He looked up and said "don't do that!"to Max';

    "He looked up and said \"don't do that!\"to Max";

    "In JavaScript, use \\as an escape character in strings";
```
<small>큰 따옴표를 쓸지, 작은따옴표 쓸지는 스스로 정하면 됩니다. 하지만 보통은 큰따옴표를 사용합니다. don't 등의 아포스트로피를 사용 할때 큰 따옴표를 쓰는편이 맞습니다.</small>

#### 템플릿 문자열
값을 문자열 안에 써야 하는일이 많습니다. 이때 문자열 병합을 통해 변수나 상수를 문자열 안에 쓸 수 있습니다.
```
    let nameTemp = JEONGHO;
    "The Current Temperature is "+nameTemp+""
    `User ${nameTemp} is not authorized to do ${action}.`;
```

#### 줄바꿈
```
    const enter = "line\n" + \"line2\n" + "line3"

    "line
    line2
    line3"
```

#### 숫자와 문자열
자바스크립트는 필요하다면 숫자가 들어 있는 문자열을 자동으로 숫자로 부꿉니다. 이런 상황이 어떻게 일어나는지는 5장에서 설명합니다.
```
    3 + '30': // 330 3이 문자열로 바뀝니다.
    3 * '30' // 90 30이 숫자로 바뀝니다.
```

### 불리언
불리언은 true와 false 두가지 값밖에 데이터 타입입니다.자바스크립트에서도 비슷한 방식을 사용합니다. 모든 값이 참과 거짓으로 나눌 수 있읍니다.

```
    true,false

    0 == false;
    "진실" == true;
    !!"진실" == true;
```

### 심볼
심볼은 유일한 토큰을 나타내기 위함 es6에서 도입한 새 데이터 타입입니다. 심볼은 항상 유일하며 절대적입니다.
```
    const RED = Symbol("The color of a sunset!");
    const ORANGE = Symbol("The color of a sunset!");

    RED === ORANGE //false; 심볼은 모두 서로 다릅니다.
```

### null과 undefined
null과 umdefined는 모두 존재않는 것을 나타냅니다. null은 프로그래머에게 허용된 데이터 타입이며 undefined는 자바스크립트 자체에서 사용합니다.
```
    let currentTemp; //  암시적으로 undefined입니다.
    const targetTemp = null; // 아직 모르는 값입니다.
```

### 객체
객체의 본질은 컨테이너입니다.
```
    const obj = {};
    const obj = Object();

    obj.color = "yellow";
```
프로퍼티에 접근하는 방식은 접근연산자(.)와 유효한 식별자가 아닌 이름은 쓴다면 계산된 멤버 접근 연산자([])를 써야 합니다.

### Nubmer, String, Boolean 객체 
자바스크립트는 일시적으로 Nubmer, String, Boolean 객체를 만듭니다. 이 객체에는 toUpperCase,concat,parseInt ... 함수가 들어있습니다.  이 함수를 호출하는 즉시 임시 객체를 파괴합니다. 
```
    const s = "hello";
    s.toUpperCase()
    
    s.rating = 3 ;
    console.log(s);
    s.rating; // undefined
```
이런 동작은 전혀 드러나지 않고 사실 필요없지만 사바스크립트가 이면에서 무슨 일을 하는지 알아두면 도움이 될 수 있습니다.

### 배열
자바스크립트 배열은 특수한 객체입니다. 배열 콘텐츠에는 순서가 있으며 키는 순차적인 숫자입니다.

* 배열 크기는 고정되지 않습니다. 언제든 요소를 추가하거나 제거할 수 있습니다.
* 요소의 데이터 타입을 가리지 않습니다. 즉, 문자열만 쓸 수 있는 배열이라던가 숫자만 쓸 수 있는 배열 같은게념이 아예 없습니다.
* 배열 요소는 0으로 시작합니다.

<small>배열은 분수, 음수 등을 키로 쓸수 있습니다. 하지만 이런 행동은 설꼐 목적에 어긋 날 뿐아니라 혼란스러운 동작과 찾기 어려운 버그를 초래할 수 있습니다.</small>

### 객체와 배열 마지막의 쉼표

```
    const arr = {
        "one",
        "two",
        "three",
    }
    
    const 0 = {
        one: 1,
        two: 2,
        three: 3,
    }
```
마지막 쉼표를 trailing comma, dangling comma, terminal comma 등 부릅니다.
자바스크립트 객체 표기법(JSON)에는 마지막 쉼표를 허용하지 않지만 자바스크립트 객체,배열에 마지막 쉼표는 선택입니다. 

### 날짜 
자바스크립트의 날짜와 시간은 내장된 Date 객체에서 담당합니다. 자바스크립트의 Date는 자바에서 가져온 객체입니다. Date 객체는 사용하기 어려운 편이고 서버시간과 미세하게 다를 수 있습니다.
 
 ```
    const now = new Date();
    
 ```
 Date() 생성자를 통해 만들 수 있습니다.
 
### 정규표현식
 (regex or regexp로도 쓰는) 정규표현식은 자바스크립트의 부속언어에 가깝습니다. 정규표현식은 필요한 복잡한 검색과 교체작업을 비교적 단순하게 만듭니다. 자바스크립트의 정규표현식은 RegExp 객체를 사용합니다. 슬래시 한쌍 (/ ... /)사이에 심볼을 넣는 리터럴 문법도 있습니다.
 
 ```    
    const regexp_type1 = /ab+c/g;
    const regexp_type2 = new RegExp("ab+c","g");
 ```
 
### 데이터 타입 변환(문자 -> 숫자 , 숫자 -> 문자)
#### 문자 -> 숫자
``` 
    const numStr = "33.3";
    const num = Number(numStr);
    
    typeof num == number;
``` 
숫자로 바꿀 수 없는 문자열에는 NaN이 반환됩니다. 위 방법은 Number 객체 생성자를 사용하는 방법입니다.

두번째 방법은 내장 함수인 parseInt 나 parseFloat 함수를 사용하는 방법입니다.

``` 
    const a = parseInt("16 volts", 10); volts는 무시됩니다. 
    const b = parseInt("16 volts 1000", 10); volts는 무시됩니다. 
``` 
parseInt,parseFloat 함수는 기본 값이 10이지만 항상 기수를 명시하길 권합니다. 숫자 + 문자 조합에서 숫자를 변환하지만 숫자 + 문자 + 숫자로 변환을 하면 뒤에 숫자는 무시합니다.

#### 숫자 -> 문자
``` 
    const n = 33.5;
    const s = n.toString();
``` 
<small>숫자가 아닌 객체를 변환 할 경우 쓸모 없는 문자열 "[object Object]"를 반환합니다.</small>

### 불리언으로 변환
자바스크립트는 부정연산자(!)를 써서 모든 값을 불리언으로 바꿀수 있습니다.
``` 
    const n = 0; //거짓 같은 값
    const b1 = !!n; // false
    const b2 = Boolean(n); // false
``` 
 또한 조건연산자를 통해 문자열 또는 숫자로 변환도 가능합니다.
```
 const c = true ? 1 : 0;
 const b = true ? "통과" : "";
```

### 요약
* 자바스크립트에는 문자열, 숫자, 불리언, null, undefined, 심볼의 여섯가지 원시타입과 객체 타입이 있습니다.
* 자바스크립트의 모든 숫자는 배정도 부동소수점 숫자(더블)입니다.
* 배열은 특수한 객체이며, 객체와 마찬가지로 매우 강력하고 유연한 데이터 타입입니다.
* 날짜, 맵, 셋, 정규식 등 자주 사용할 다른 데이터 타입들은 특수한 객체 타입입니다.