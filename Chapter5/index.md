# chapter 5. 표현식과 연산자
## 표현식
* 값으로 평가될 수 있는 문
* 무언가를 요청 하는 문
* 결과를 명시적으로 반환 하는 것


```
    let x;      //선언문
    x = 3*5;    //표현식
```
```
    let x,y;         
    y = x = 3*5;    // 곱셈 표현식
                    // 첫번째 할당 x = 15, y = undefined
    y = x = 15;     // 두번째 할당 y = 15
    y = 15;         // x=15, y=15
                    // 이값은 사용하지도 않았고 어딘가에 할당하지도 않으니 그냥 버려집니다.
```
자바스크립트 표현식은 <strong>연산자 우선순위</strong>로 평가
표현식은 대부분 연산자 표현식입니다.
즉, 곱셈 표현식은 곱셈 연산자와 피연산자 두개로 이어집니다. 피연산자는서로 곱하는 두 숫자이며 피연산자 자체도 표현식입니다.

### 연산자
연산자는 하나이상의 피연산자가 있어야 결과로 나타낼 수 있다.

### 산술연산자


```  
    $pop.css({
        left: function() {return "50%" },
        top: function() { return ( ! isFlow ) && "50%" },
        marginTop: function() { return ( ! isFlow ) && -( $pop.outerHeight() / 2 ) },
        marginLeft: function() {return -( $pop.outerWidth() / 2 ) },
        height: function() { return ( isFlow ) && "100%" }
    });
```

``` 
    let a = true;
    let b = true;
    let c = 3;

    (function(){
        return console.log( a && b && c);
    })()
```