# :diamond_shape_with_a_dot_inside: Alpine.js

## :curly_loop: 경량 자바스크립트 프레임워크 Alpine

### 단순성이 핵심

- cdn 불러오기

```html
<script src="//unpkg.com/alpinejs" defer></script>
```

- x-attribute를 html 요소에 인라인으로 작성하는 방식  
  x- attribute는 html 요소에 배치하고 요소를 확장하는 역할을 한다
- 요소를 알파인js의 구성 요소로 선언하면 x데이터를 사용하여 구성 요소에 일부 상태를 제공할 수 있음 cf) 리액트 (state)

```html
<div x-data="{ open: false }">
  <button @click="open = true">Expand</button>

  <span x-show="open"> Content... </span>
</div>
```

여기서 x-data는 {open: false} 객체와 같음을 의미
open은 false 로 지정되었고 해당 컴포넌트 안에서 유효하다

알파인 cdn 으로 불러오고 콘솔에 alpine 입력하면 버전 정보 나옴

x-model : 데이터 바인딩

클릭 이벤트
x-on:click ="js"

modifier
submit 이벤트에 대해 prevent default 하기

- x-on:submit.prevent

- x-for : Repeat a block of HTML based on a data set

```html
<button x-on:click="todos = todos.filter((currTodo) => currTodo !== todo)">
  x
</button>
```

```html
<button @click="todos = todos.filter((currTodo) => currTodo !== todo)">
  x
</button>
```

x-on:click을 @click으로 대체가능

- 폼 제출 후 input 비우기
- 포인터 변경 -> class 추가

포인터로 바꾸기

빈 todo 추가 막기

x-show :뷰에서 요소를 조건부로 표시하거나 숨길 수 있게 함

x-bind:class="{'completed' : todo.completed }"
에서 x-bind 생략 가능
