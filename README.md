# javascript_css_html
기초적인 이론 지식
# HTML
#### head tag
> 메타데이터를 포함하기 위한 요소, title, style, link ,script 에 대한 데이터

#### meta tag
> descripiton, keywords, author, 기타 메타 데이터 정의 브라우저, 검색엔진 등에 의해 사용 

#### form tag
> 사용자가 입력한 데이터를 수집하기 위해 사용, input, textarea, button, select, ... 등의 입력 양식 태그를 포함 할 수 있음
> action = URL, method = get,post 를 가지고 있음
> 

# CSS
#### 후손 셀렉터
>셀렉터A 셀렉터B 자식 뿐만아니라 아래 모두에게 적용
#### 자식 셀렉터
> 셀렉터 > 셀렉터B 자식만 
#### 인접 동위 셀렉터
> 셀렉터A + 셀렉터B 바로 옆에있는 형제만
#### 일반 동위 셀렉터
> 셀렉터A ~ 셀렉터B
#### 가상 클래스 셀렉터
> link(셀렉터가 방문하지 않은 링크), :visited(셀렉터가 방문한 링크), :hover, :active(클릭된 상태), :focus(셀렉터에 포커스가 들어와있을 때) 와 같이 특정 상태에 따라 스타일 지정
#### UI 요소 상태 셀렉터
> :checked, :enabled, :disabled
#### 구조 가상 클래스 셀렉터
> :first-child , :last-child, :nth-child(n), :nth-last-child(n), :first-of-type, :last-of-type, :nth-of-type(n), :nth-las-of-type(n)
#### 부정 셀렉터
> :not
#### 정합성 체크 셀렉터
> :valid, :invlid(input, form에 대한 정합성 검증이 실패하거나 성공한 요소)
#### 가상 요소 셀렉터
> ::first-letter(콘텐츠의 첫글자), ::first-line(콘텐츠의 첫줄), ::after, ::before, ::selection(드래그한 콘텐츠)

#### em 단위
> 배수 단위로 상대 단위임, 요소에 지정된 사이즈에 상대적인 사이즈를 설정 1em은 요소에 지정된 사이즈 1배 2em dms 2배
>중첩된 자식 요소에 em을 지정하면 모든 자식 요소의 사이즈에 영향을 미치기 때문에 주의
#### rem 단위
> em의 기준은 상속의 영향으로 바뀔 수 있음 하지만 rem은 html 사이즈를 기준으로 삼음 (root)(em)
#### viewport 단위
> vmin : viewport 너비 높이 중 작은쪽의 1/100
> vmax : viewport 너비 높이 중 작은쪽의 1/100
#### box-sizing
> content-box : content 영역의 width, height
> border-box : padding, border 가 포함된 값
#### background-attachment 프로퍼티
> 일반적으로 화면을 스크롤하면 배경이미지도 함께 스크롤 되는데 고정되어있게 할려면 fixed 키워드를 넣으면 됨
#### @keyframes
> CSS 애니메이션과 트랜지션 방식의 주된 차이는 @keyframes rule에 있음 애니메이션의 흐름중에서 여러 시점에서 css 프로퍼티 값을 지정할 수 있음
#### SASS mixin
> extend와 차이는 매개 변수를 사용 할 수 있다. style markup 반환
#### SASS function
> mixin 과 다르게 @return directive를 통하여 값을 반환








# Javascript
#### javascript의 특징?
>   1. 웹 브라우저에서 동작하는 유일한 프로그래밍 언어
  2. 인터프리터 언어(컴파일 작업을 수행 x)
  3. 프로토타입 기반 객체지향 언어

#### ECMAScript와 Javascript의 관계?
>   *ECMAscript : 자바스크립트 표준 명세인 ECMA-262
  1. Javascript 는 기본 뼈대를 이루는 ECMAScript와 브라우저가 별도 지원하는 클라이언트 사이드 Web API 를 포함한것 ex)DOM, Fetch
  
#### Javascript 데이터 타입 종류 ES6기준
> 원시타입(변경 불가능한 값, 값에 의한 전달) : boolean, null, undefined, number, string, symbol
객체 타입 : object

#### symbol 타입이란? (ES6에 추가된 새로운 데이터 타입)
> 이름의 충돌 위험이 없는 유일한 객체의 프로퍼티 키를 만들기 위함
> 
```
var key = Symbol('key');
console.log(typeof key); // symbol
>
var obj = {};
obj[key] = 'value';
console.log(obj[key]); // value
```

#### 동적 타이핑 ?
> 변수에 할당된 값에 따라 자동으로 변수의 타입이 할당되는 것

#### 호이스팅 ?
>  자바스크립트의 모든 선언문은 프로그램의 맨 위로 올라가 먼저 선언이 되게 된다.

#### 변수 선언 단계
>  선언단계 : 변수 객체에 변수 등록. 이 변수 객체는 스코프가 참조하는 대상이 된다.
초기화 단계 : 변수 객체에 등록된 변수를 메모리에 할당한다. 이단계에서 변수 undefined 로 초기화
할당 단계 : undefined로 초기화 된 변수에 실제값 할당

#### var와 let의 차이점과 var의 문제점
> let : 블록 레벨 스코프
> var : 함수 레벨 스코프
var 의 문제점
	1. 전역 변수의 남발됨
    2. 의도치 않은 변수의 전역화가 됨
    3. 중복 선언이 허용됨
var : 변수 생성 단계중 선언단계 + 초기화 단계 같이 실행 된다 undifind 로
let : 변수 생성 단계중 선언단계 -> TDZ -> 초기화로 각각의 단계로 이루어 진다.

#### 함수가 프로퍼티를 가질 수 있는 이유
> 함수는 객체이기 떄문에 프로퍼티를 가질 수 있습니다
```
> function square(number) {
  return number * number;
}
> square.x = 10;
square.y = 20;
> console.log(square.x, square.y);
```

#### 함수 객체 프로퍼티중 arguments 프로퍼티에 대해 설명
> 함수 호출시 전달 된 **인수의 정보를 담고있는 순회 가능한 유사 배열 객체**
> 가변 인자 함수를 구현할 때 유용하게 사용 할 수 있음

#### 함수 객체 프로퍼티중 length에 대해 설명
> 함수 정의시 작성된 매개변수 갯수

#### 즉시실행 함수 사용법
> 소괄호로 함수를 감싼다. 최초 한번만 호출되면 다시 호출할 수 없다.

#### 자바스크립트는 프로토타입 기반 객체지향 프로그래밍인데 프로토타입?
> 객체 지향 상속 개념과 같이 부모 객체의 프로퍼티 또는 메소드를 상속 받아 사용할 수 있게 하는 것

#### 렉시컬 스코프?
> 함수를 어디서 호출하는지가 아니라 어디에 선언하였는지에 따라 스코프 결정에 영향을 줌

#### 함수의 호출방법 4가지
> ```
// 1. 함수 호출
foo(); // window
// window.foo();
> 
// 2. 메소드 호출
var obj = { foo: foo };
obj.foo(); // obj
> 
// 3. 생성자 함수 호출
var instance = new foo(); // instance
>
// 4. apply/call/bind 호출
var bar = { name: 'bar' };
foo.call(bar);   // bar
foo.apply(bar);  // bar
foo.bind(bar)(); // bar

#### 자바스크립트의 this 에 대해서
> 함수 호출방식에 의해 this에 바인딩할 객체가 동적으로 결정됨 -> 함수를 호출할 때 함수가 어떻게 호출되었는지에 따라 this에 바인딩할 객체가 결정
> 함수 호출 방식과 this
	1. 함수 호출 -> this === window, global
    2. 메소드 호출 -> this === 해당 메소드를 소유한 객체, 해당 메소드 호출 객체
    3. 생성자 함수 호출 -> this === 새ㅇ성자 함수 내에서 사용되는 객체를 가르킨다 
    4. apply/call/bind 호출 this === 첫번째 생성자 함수

#### Socpe-Safe Constructor Patten
> 생성자 함수를 new 없이 호출한 경우, 함수 Person 내부의 this는 전역객체를 가리키므로 name은 전역변수(window)에 바인딩된다. 또한 new와 함께 생성자 함수를 호출하는 경우에 암묵적으로 반환하던 this도 반환하지 않으며, 반환문이 없으므로 undefined를 반환하게 된다.
>
>일반함수와 생성자 함수에 특별한 형식적 차이는 없기 때문에 일반적으로 생성자 함수명은 첫문자를 대문자로 기술하여 혼란을 방지하려는 노력을 한다. 그러나 이러한 규칙을 사용한다 하더라도 실수는 발생할 수 있다.
>
>// Scope-Safe Constructor Pattern
function A(arg) {
  // 생성자 함수가 new 연산자와 함께 호출되면 함수의 선두에서 빈객체를 생성하고 this에 바인딩한다.
>  /*
  this가 호출된 함수(arguments.callee, 본 예제의 경우 A)의 인스턴스가 아니면 new 연산자를 사용하지 않은 것이므로 이 경우 new와 함께 생성자 함수를 호출하여 인스턴스를 반환한다.
  arguments.callee는 호출된 함수의 이름을 나타낸다. 이 예제의 경우 A로 표기하여도 문제없이 동작하지만 특정함수의 이름과 의존성을 없애기 위해서 arguments.callee를 사용하는 것이 좋다.
  */
  if (!(this instanceof arguments.callee)) {
    return new arguments.callee(arg);
  }
>
 > // 프로퍼티 생성과 값의 할당
  this.value = arg ? arg : 0;
}
>
>var a = new A(100);
var b = A(10);
>
> console.log(a.value);
console.log(b.value);

#### 실행 컨텍스트가 무엇인지
> 실행 가능한 코드가 실생되기 위해 필요한 환경, 실행 가능한 코드를 형상화, 구분하는 추상적 개념
> 물리적으로는 객체의 형태를 가지며 (Variable object, Scope chain, thisValue) 3프로퍼티 소유

#### 실행 컨텍스트 Variable Object
> VO가 갖는 정보 -> 변수, 메게 변수와 인수 정보, 함수 선언(함수 표현식은 제외)

#### 클로저의 개념(클로저에 대해 설명하세요)
> 클로저는 함수와 그 함수가 선언됐을 떄의 렉시컬 환경과의 조합
> 렉시컬 스코핑 : 스코프는 함수를 호츨할 떄가 아니라 함수를 어디에 선언하였는지에 따라 결정 되는것
>자신을 포함하고 있는 외부함수보다 내부함수가 더 오래 유지되는 경우 외부 함수 밖에서 내부 함수가 호출되더라도 외부함수의 지역 변수에 접근할 수 있는 것
```
>ex)
function outerFunc() {
  var x = 10;
  var innerFunc = function () { console.log(x); };
  return innerFunc;
}
>
/**
 *  함수 outerFunc를 호출하면 내부 함수 innerFunc가 반환된다.
 *  그리고 함수 outerFunc의 실행 컨텍스트는 소멸한다.
 */
var inner = outerFunc();
inner(); // 10
```
> 자신이 생성될 때의 환경을 기억하는 함수..

#### 클로저 사용 이유
> 1. 상태 유지
```
var toggle = (function() {
  var isShow = false;
  return () => {
     //isShow 처리
     isShow = !isShow
 }
})();
```  
> 2. 전역 변수 사용 억제
```
var increase = (function () {
      // 카운트 상태를 유지하기 위한 자유 변수
      var counter = 0;
      // 클로저를 반환
      return function () {
        return ++counter;
      };
    }());
```
> 3. 정보 은닉
```
function Counter() {
  // 카운트를 유지하기 위한 자유 변수
  var counter = 0;
  // 클로저
  this.increase = function () {
    return ++counter;
  };
  // 클로저
  this.decrease = function () {
    return --counter;
  };
}
```

#### 함수형 프로그래밍
> 거의 모든 것을 순수 함수로 나우누어 문제를 해결하는 기법, 대입문을 사용하지 않는 프로그래밍

#### javascript event flow(버블링과 캡처링이 뭔가요)
>버블링 : 자식요소에서 발생한 이벤트가 부모 요소로 전파되는 것
>캡처링 : 자식 요소에서 발생한 이벤트가 부모 요소부터 시작하여 이벤트를 발생시킨 자식요소까지 도달하는 것
버블링과 캡처링은 하나만 발생하는 것이 아니라 캡처링 부터 시작하여 버블링으로 종료

#### RESET API 두가지 규칙
> 1. URI는 정보의 자원을 표현해야 함니다
	ex) 
    bad
    GET /getTodos/1
    GET /todos/show/1
    good
    GET /todos/1
 2. 자원에 대한 행위는 HTTP Method로 표현한다
 	ex) bad : GET /todos/delete/1
    	good : DELETE /todos/1
 
 #### HTTP Method
 > 1. GET : 모든/ 특정 리소스들을 조회
 2. POST : 리소스를 생성
 3. PUT : 리소스의 전체를 교체
 4. PATCH : 리소스의 일부를 수정
 5. DELETE : 모든 / 특정 리소스를 삭제

 #### REST API 구성
 > Resource : 자원 - HTTP URI
 Verb : 자원에 대한 행위 - HTTP Method
 Representations : 자원에 대한 행위의 내용 - HTTP Message Pay Load
 
 #### SPA 란?
 > Single Page Application
 기본적으로 단일 페이지로 구성되며 기존의 서버 사이드 렌더링과 비교할 때 배포가 간단하며 네이티브 앱과 유사한 사용자 경험을 제공 가능
 >
 >SPA는 기본적으로 웹 애플리케이션에 필요한 모든 정적 리소스들을 한번 다운로드 하고 페이지 갱신에 필요한 데이터만을 전달 받아 페이지를 갱신하여 전체적인 트래픽을 감소하고 새로고침이 발생하지 않는다. 또한 사용자 경험(UX) 향상에 큰 영향을 준다
   
#### 일시적 사작지대 TDZ 란
> 스코프의 시작 지점부터 초기화 시작 지점까지의 구간을 TDZ 라고 한다

#### 이벤트 버빌링과 캡처링
> 버블링 : 한요소에 이벤트가 발생하면 이 요소에 할당된 핸들러가 동작하고 이어서 부모 요서의 핸들러 동작 거의 모든 이벤트는 버블링됨 focus와 같은 예외도 있긴함
> 캡쳐링 : 캡처링은 한요소에 이벤트가 가기까지 이벤트가 하위 요소로 전파되는 단계


# React

### React 공식으로 제공하는 hook의 종류와 사용법들
(기본적인 훅은 생략함 내기준 이미 아는 훅)
#### useContext
> ```
> const value = useContext(MyContext); //context 객체(React.createContext에서 반환된 값)을 받아 그 context의 현재 값을 반환합니다.
#### useReducer
> ``` 
> const [state, dispatch] = useReducer(reducer, initialArg, init) ///useState의 대체 함수 (state, action) => newState의 형태로 reducer를 받고 dispatch 메서드와 짝의 형태로 현재 state를 반환합니다. 세번자 인자는 초기 state를 지연해서 생성하기 위함
> 
>ex)
> 
>function init(initialCount) {
>  return {count: initialCount};
>}
>function reducer(state, action) {
>  switch (action.type) {
>    case 'increment':
>      return {count: state.count + 1};
>    case 'decrement':
>      return {count: state.count - 1};
>    case 'reset':
>      return init(action.payload);
>    default:
>      throw new Error();
>  }
>}
>
>function Counter({initialCount}) {
>  const [state, dispatch] = useReducer(reducer, initialCount, init);
>  return (
>    <>
>      Count: {state.count}
>      <button
>        onClick={() => dispatch({type: 'reset', payload: initialCount})}>
>        Reset
>      </button>
>      <button onClick={() => dispatch({type: 'decrement'})}>-</button>
>      <button onClick={() => dispatch({type: 'increment'})}>+</button>
>    </>
>  );
>}

#### useCallback
> ``` 
> const memoizedCallback = useCallback(
>  () => {
>    doSomething(a, b);
>  },
>  [a, b],
>);
> //메모이제이션된 콜백을 반환한다. 불필요한 렌더링을 방지하기 위해 (예로 shouldComponentUpdate를 사용하여) 참조의 동일성에 의존적인 최적화된 자식 컴포넌트에 콜백을 전달할 때 유용합니다.

#### useMemo
> ```
> const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
> 메모이제이션된 값을 반환한다.

#### useRef
> ```
> const refContainer = useRef(initialValue); 
>// 컴포넌트의 전 생애주기를 통해 유지될 수 있도록 한다. 컴포넌트가 리렌더링 되도 값을 유지해야 할 것들을 넣으면 됨 interVal 사용하는 것처럼 DOM 에 접근하는 방법도 있어요
>//부모가 자식에게 메서드를 넘겨하하는 상황이 발생할 떄 

#### useImperativeHandle
> ```
>const FormControl = React.forwardRef((props, ref) => {
> const inputRef = useRef(null);
> useImperativeHandle(ref, () => ({getValue(){
>  return inputRef.current.value
> }) }, [inputRef]); // deps도 추가가능하다.
> return (
>  <div className="form-control">
>    <input type="text" ref={inputRef} />
>  </div>
> );
>})
>const App = () => {
> const inputRef = React.useRef();
> return (
>  <div className="App">
>    <FormControl ref={inputRef} />
>    <button
>     onClick={() => {
>      console.log(inputRef.current.getValue());
>     }}>
>     focus
>    </button>  
>  </div>
> );
>}
>//위의 예시에서 <FormControl ref={inputRef} />를 렌더링한 부모 컴포넌트는 inputRef.current.getValue()를 호출할 수 있습니다.
>//자식 컴포넌트의 ref를 부모에서 사용해야 하는 경우나, 메소드 전달 할때 유용하게 쓸 수 도 있을듯..

#### useLayoutEffect
>이 함수의 시그니처는 useEffect와 동일하긴 한데, 모든 DOM 변경 후에 동기적으로 발생합니다. 이것은 DOM에서 레이아웃을 읽고 동기적으로 리렌더링하는 경우에 사용하세요. useLayoutEffect의 내부에 예정된 갱신은 브라우저가 화면을 그리기 이전 시점에 동기적으로 수행될 것입니다.

화면 갱신 차단의 방지가 가능할 때 표준 useEffect를 먼저 사용하세요.

# 기타
#### webpack?
> 여러개 파일을 하나의 파일로 합쳐주는 모듈 번들러

#### 바벨?
> ECMAScript 로 짜여진 코드를 현재 및 과거의 브라우저 환경에서 호환되는 버전으로 변환하는데 주로 사용

#### npm?
> npm 은 자바스크립트 프로그래밍 언어를 위한 패키지 관리자이다.

#### CORS
>추가 HTTP 헤더를 사용하여, 한 출처에서 실행준인 웹 애플리케이션이 다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여하도록 브라우저에게 알려주는 체제
>CORS는 동일한 도메인이 아닌 다른 도메인에 리소스를 요청할 시에 서로 다른 origin에 대하여 HTTP 요청이 가능하게 해주는 표준입니다.
> 로컬환경에서 테스트를 할 때 CORS를 해결한 적이 있다.
> 일단 package.js 에서 "proxy" : "프록시 주소"로 설정해 준 후 요청을 로컬로 보내게 되면 프록시로 요청을 하게 된다. 그후 node로 만든 프록시서버에서 패킷의 해더를 조작하여 해결한 경험이 있다.

#### 브라우저 저장소
>키 - 벨류 스토리지의 형태
> 로컬 스토리지와 세션 스토리지의 차이점은 영구성에 있음. 로컬 스토리지는 사용자가 지우지 않는 이상 계속 남아있음, 세션은 닫으면 없어짐
> 쿠키는 만료 기한이 있는 키 - 값 저장소
> localStorage.setItem, getItem, removeItem, clear 와 같이 사용할 수있음
> 세션 스토리지는 window.sessionStorage에 위치
> 세션 스토리지에 access token 과 refresh 토큰을 넣고 사용해 보았음