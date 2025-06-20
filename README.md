# TIL
# Component 컴포넌트
- UI를 구성하는 독립적인 단위
- 마크업을 반환하는 자바스크립트 함수
- 다른 컴포넌트 안에 중첩 가능능

### 장점  
- 독립적 : 자신만의 state를 가질 수 있어 독립적으로 동작
- 재사용성 : 한 번 만들어 두면 여러 곳에 재사용 가능
- 조합 가능 : 여러 개를 조합해 화면 구성성
- 유지보수 쉬움 : 코드가 작고 역할이 명확해서 관리가 쉬움

### props와 state
- props : 컴포넌트에 외부에서 전달되는 데이터
- state : 컴포넌트 자체 내부에서 관리하는 데이터

## 반환문
- 반환문은 아래 컴포넌트에서처럼 한 줄에 모두 작성 가능
>`return <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />;`
- 마크업이 모두 return 키워드와 같은 라인에 있지 않은 경우 다음과 같이 괄호로 묶어야 함
>`return (`   
  `<div>`  
    `<img src="https://i.imgur.com/MK3eW3As.jpg"` `alt="Katherine Johnson" />`
  `</div>`   
`);`

## 컴포넌트 중첩 및 구성 
- 같은 파일에 여러 컴포넌트 포함 가능
- 이 파일이 복잡해지면 언제든지 별도의 파일로 이동 가능
>`export default function Gallery() {`  
>--`return (`  
>----`<section>`  
>------`<h1>Amazing scientists</h1>`  
>------`<Profile />`  
>------`<Profile />`  
>------`<Profile />`  
>----`</section>`  
>--`);`  
>`}`
- Profile 컴포넌트는 Gallery안에서 렌더링되기 때문에 Gallery는 각 Profile을 자식으로 렌더링하는 부모 컴포넌트
- 컴포넌트는 다른 컴포넌트를 렌더링할 수 있지만, 그 정의를 중첩해서는 X
- 자식 컴포넌트에 부모 컴포넌트의 일부 데이터가 필요한 경우, 정의를 중첩하는 대신 props로 전달
