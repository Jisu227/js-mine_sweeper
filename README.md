# *지뢰 찾기 게임*



#### 🎯 *실행 화면*


![Sep-27-2021 23-49-22](https://user-images.githubusercontent.com/86669143/134932254-f3ceaf90-07a0-452f-b2a3-fe1dab4d196f.gif)



---
#### 🧩 *배운 내용 정리하기*
    
    1. contextmenu 이벤트
    => 지금까지 마우스 클릭 이벤트는 모두 좌클릭이었다. 마우스 우클릭 이벤트는 따로 있다.
       좌클릭 이벤트는 click이고, 우클릭 이벤트는 contextmenu 이다. contextmenu 이벤트는
       기본적으로 브라우저 메뉴를 띄우므로 이를 막으려면 event.preventDefault 메서드를 호출해야 한다.
    
    2. 옵셔널 체이닝
    => ?.는 옵셔널 체이닝(optional chaining)이라는 문법이다. 앞에 있는 것이 참(truthy)인 값이면
       뒤 코드를 실행하고, 거짓(falsy)인 값이면 코드를 모두 undefined로 만들어 버린다.
    ex) const obj = undefined;
        const arr = undefined;
        const func = undefined;
        obj?.b; // undefined
        arr?.[0]; // undefined
        func?.(); // undefined
    - 객체나 배열뿐만 아니라 함수에도 옵셔널 체이닝을 적용할 수 있다. 속성에 접근하거나 호출하려는 것이
      거짓인 값인지 아닌지 의심될 때 옵셔널 체이닝을 적용하자.
    
    3. 재귀 함수
    => 어떤 함수의 내부에서 자기 자신을 다시 호출하는 함수를 재귀 함수(recursive function)라고 한다.
    ex) let i = 0;
        function recurse() {
          i++;
          recurse();
        }
    - 재귀 함수를 사용할 때 호출 스택의 최대 크기를 초과하는 경우가 빈번하게 발생한다.
      이때 Maximum call stack size exceeded 오류가 발생하는데, setTimeout과 같은 비동기 함수를 
      사용해 해결 할 수 있다.
      재귀 함수를 사용할 때는 연산량이 많으면 브라우저가 느려지는 현상이 발생하므로 연산량을 최소화 할 수 있게
      코드를 작성하자.