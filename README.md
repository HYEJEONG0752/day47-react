## **생명주기란 무엇인가요?**

- 컴포넌트가 생성되고 화면에 렌더링되며 업데이트되고 소멸하는 과정을 설명하는 것.
- 각 단계마다 특정 메서드가 호출되어 개발자가 원하는 동작을 구현할 수 있도록 함.

## **컴포넌트의 마운팅 단계에서 호출되는 생명주기 메서드는 무엇인가요?**

- `constructor()`, `static getDerivedStateFromProps()`, `render()`, `componentDidMount()`메서드가 호출되고, 이 단계는 컴포넌트가 DOM에 추가될 때 수행됨.

## **클래스 컴포넌트와 함수형 컴포넌트의 주요 차이점은 무엇인가요?**

- 클래스 컴포넌트: 상태 관리 및 생명주기 메서드를 사용하며, `class`키워드로 정의됨
- 함수형 컴포넌트: 상태 관리 및 생명주기 메서드를 사용할 수 없었으나, `Hook`을 통해 가능하게 되었으며, 더 간결하고 코드 작성이 쉬움

## **`componentDidMount()` 메서드의 주요 역할은 무엇인가요?**

- `componentDidMount()`메서드는 컴포넌트가 처음 마운트된 후 한번만 호출됨.
주로 API요청, 이벤트 리스너 설정, 비동기 작업 등을 수행하는 데 사용됨.

# **`useEffect` Hook은 어떤 생명주기 단계에 해당하나요?**

- `useEffect` Hook은 클래스 컴포넌트의 `componentDidMount()`, `componentDidUpdate`, `componentWillUnmount`메서드의 역할을 모두 수행할 수 있음.
특정 조건에 따라 적절한 시점에 효과를 적용할 수 있음.

## **클래스 컴포넌트에서 상태를 초기화하는 메서드는 무엇인가요?**

- 상태는 `constructor`메서드 안에서 `this.state`로 초기화 됨.
(예: `this.state = { count: 0 };`)

## **함수형 컴포넌트에서 상태 관리를 위해 사용하는 Hook은 무엇인가요?**

- 함수형 컴포넌트에서 상태 관리를 위해 사용하는 Hook은 `useState`임.
(예: `const [count, setCount] = useState(0);`)

## **`componentWillUnmount()` 메서드는 언제 호출되나요?**

- `componentWillUnmount()`메서드는 컴포넌트가 DOM에서 제거되기 직전에 호출.
주로 이벤트 리스너 해제나 클린업 작업에 사용

## **`shouldComponentUpdate()` 메서드는 어떤 역할을 하나요?**

- `shouldComponentUpdate()`메서드는 컴포넌트가 업데이트될지 여부를 결정.
기본적으로 `true`를 반환하며, 성능 최적화를 위해 조건에 따라 `false`를 반환할 수 있음.

## **에러 경계를 설정하기 위해 사용하는 컴포넌트는 무엇인가요?**

- 에러 경계를 설정하기 위해 클래스 컴포넌트에서 `componentDidCatch()`와 `getDerivedStateFromError()`메서드를 사용하여 에러 경계를 설정. 주로 UI를 보호하기 위해 사용됨.

## **`getSnapshotBeforeUpdate()` 메서드는 어떤 상황에서 사용되나요?**

- `getSnapshotBeforeUpdate()`메서드는 DOM이 업데이트되기 직전에 호출되며, 이전 상태를 기반으로 특정 정보를 캡처할 때 사용. 반환된 값은 `componentDidUpdate()`에서 접근할 수 있음.

## **`useState` Hook의 기본 사용법을 설명해주세요.**

- `useState`는 함수형 컴포넌트에서 상태 관리를 위해 사용되는 Hook으로 상태 변수와 해당 상태를 업데이트하는 함수를 반환.
```javascript
const [const, setCount] = useState(0);
```
여기서 `count`는 상태 변수이고, `setCount`는 상태를 업데이트하는 함수

## **클래스 컴포넌트에서 `render()` 메서드의 역할은 무엇인가요?**

- `render()`메서드는 JSX를 반환하며, 컴포넌트가 화면에 렌더리욀 UI를 정의함.
상태나 props의 변경에 따라 다시 호출됨.

## **`componentDidCatch()` 메서드는 어떤 목적으로 사용되나요?**

- `componentDidCatch()`메서드는 자식 컴포넌트 트리에서 발생한 자바스크립트 에러를 잡아내고, 로깅하거나 대체 UI를 렌더링하는데 사용

## **함수형 컴포넌트에서 생명주기 메서드를 대체하는 Hook은 무엇인가요?**

- `useEffect`를 통해 컴포넌트의 마운트, 업데이트, 언마운트 시점에 코드를 실행할 수 있다.