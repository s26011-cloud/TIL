# JavaScript 기초 강의

## 메소드

<aside>

 alert()

- 경고창에 () 문구를 출력하라는 메소드이다.

 prompt

- 문자열을 입력할 수 있는 다이얼로그 박스를 열어주는 메소드이다.

 comfirm

- alert랑 비슷한다 최소 버튼과 확인 버튼이 있다.
</aside>

## console

 console.log()

- 콘솔 화면에 기록을 남기는 명령어이다.

 console.clear()

- 콘솔 창을 깨끗하게 만드는 명령어이다.

## 변수

<aside>

let 변수이름(); //변수 선언

변수이름 = 데이터; //변수 초기화

</aside>

<aside>

let 변수이름 = 데이터1; //변수 선언과 초기화를 동시

변수이름 = 데이터2; //새로운 데이터 대입

변수이름 = 데이터3 //새로운 데이터 또 대입

변수가 기억하고 있는 데이터를 바꿀 수 있다.

</aside>

## 상수

<aside>

### 상수 만드는 방법

const 상수이름 = 데이터;

상수는 값 변경이 안된다.

상수를 만들 때는 선언과 초기화를 동시에 해야한다.

</aside>

## 문자열 표현법

<aside>

### 따옴표를 이용한 문자열

const str1 = ‘작은 따옴표’

const str2 = “큰 따옴표”
<hr>

### 백틱을 이용한 템플릿 리터럴

const str3 = ``이게 백틱입니다` `

백틱을 문자열 내부에 데이터를 삽입할 수 있다.

${변수명} 이렇게 삽입함

</aside>

## document

<aside>

- document.querySelectory
    
    선택자를 인자로 전달받아, 전달받은 선택자와 일치하는 문서 내 첫번째 요소(Element)를 반환한다. 일치하는 요소가 없으면 null 데이터를 반환한다.
    
    인자로 전달되는 선택자는 문자열 타입의 유효한 css 선택자를 의미한다.
    
- document.getElementById
    id를 인자로 전달받아, 전달받은 선택자와 일치하는 문서 내 요소(Element)를 반환한다. 일치하는 요소가 없으면 null 데이터를 반환한다.

    인자로 전달되는 선택자는 문자열 타입의 'id'를 의미한다.

- textContent
    textContent 속성은 해당 노드가 포함하고 있는 텍스트 콘텐츠를 표현하는 속성이다.

    textContent를 통해 요소가 포함한 텍스트를 읽거나 변경할 수 있다.
</aside>

## 함수

### 함수 선언식
`` function 함수명() {함수의 기능을 표현한 구문}``

### 함수 표현식
`` const 함수명 = function(){함수의 기능을 표현한 구문}``

#### 마지막에 함수명()을 호출 해야한다.
<hr>

### 함수 선언식과 함수 표현식의 차이점
- 함수 선언식은 함수 호출문이 선언식보다 위에 있어도 된다.
- 함수 표현식은 함수 호출문이 위에 있으면 안된다.
<hr>

### 주의할 점.
#### 함수 내부에서 선언된 변수는 함수 밖에서 사용할 수 없다. (지역 변수)
#### 함수는 반환 값이 없거나 오직 하나이다.
#### return 아래에 코드를 써도 반환되지 않는다.
#### return은 함수를 강제로 종료시키는 역할도 한다

## 함수 return의 활용

 ```function greturn(){
    console.log("반환한다, 무언가를!!")
    return 10;
}

const result = greturn() <--(10)
console.log(result)
```
함수가 자기 기능을 수행한 자기의 호출문 자리에 리턴값을 두고 간다.

## 이벤트

### 구문 기본 형태
```button.onclick = handleClick```:
    타겟.on이벤트명 = 이벤트핸들러함수

## addEventListener

### 구문 기본 형태

```
target.addEventListener('click',function(){})
```
## createElement, appenddChild

### createElement란
- 지정된 이름의 HTML 요소를 만들어 반환해주는 역할을 한다.

### createElement 구문 형태

```
document.createElement('div')
```
HTML 요소가 만들어지고 반환 되었다고 해서 바로 웹 브라우저 화면에 추가되진 않는다.

웹 브라우저 화면에 추가하려면 dom에 직접 추가해야 한다.

## dom에 추가하는 과정

### appenChild

### 구문 형태

```
target.appenChild(자식을 추가할 요소)
```
### 예제

```
const p = document.createElement("p")
document.body.appendChild(p)
```

## 입력 요소 값 읽기

### 요소의 텍스트에 접근하고 싶다
- textContent or innerText

### 사용자가 요소에 입력한 값에 접근하고 싶다
- value

from에 포함된 입력 요소의 naem을 통해 각 입력 요소에 접근할 수 있다.

## 삼항 연산
- 세 개의 항을 이용해 결과를 반환하는 연산이다

- 보통 if문의 단축 형태로 사용되기 때문에, 삼항 조건 연산식이라고도 부른다.

### 기본 구문

```
3 > 2 ? "참" : "거짓"
```

## 타이머를 만들자

### setTimeout
- 정해진 시간이 지나고 나면 주어진 함수를 실행 해주는 타이머 메소드이다.

#### 사용방법

```
setTimeout(실행할 함수, ms 단위의 시간)
```

### setInterval
- 일정한 시간 간격에 따라 함수를 반복 실행할 수 있도록 해주는 타이머 메소드이다.

#### 사용방법

```
setInterval(반복 실행할 함수,ms 단위의 시간)
```

### clearInterval
- setInterval 메소드가 호출되어 반복 실행할 함수 타이머를 등록하면 0이 아닌숫자를 반환하는데 숫자는 타이머의 ID를 의미하며, 이를 claerInterval 메소드에 전달하면 타이머 반복 실행이 취소된다.

## classList

### Element.classList
- 웹 요소(Element)로부터 클래스 콜렉션을 반환하는 읽기 전용 속성이다.

## localStorage
- 현재 도메인의 로컬 저장소에 접근할 수 있게 해준다.