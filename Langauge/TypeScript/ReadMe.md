## 타입스크립트를 공부하기 위한 폴더입니다.

### Why TS?

#### JS의 유연한 타입은 때때로 문제가 된다. 
```
if ("" == 0) {
  // 참입니다! 근데 왜죠??
}
if (1 < x < 3) {
  // *어떤* x 값이던 참입니다!
}
```
JS 는 존재하지 않는 프로퍼티의 접근을 허용한다.
```
const obj = { width: 10, height: 15 };
// 왜 이게 NaN이죠? 철자가 어렵네요!
const area = obj.width * obj.heigth;
```

#### 정적 타입 검사
* 몇몇 언어는 버그가 많은 프로그램을 아예 실행시키지도 않음. 
* 프로그램을 실행시키지 않으면서 코드의 오류를 검출 : __정적 검사__

TS는 정적 타입 검사자 이기 때문에 프로그램을 실행시키기 전에 값의 종류를 기반으로 프로그램의 오류를 찾음.

#### 런타임 특성 (Runtime Behavior)
TypeScript는 JavaScript의 런타임 특성을 가진 프로그래밍 언어입니다. 예를 들어, JavaScript에서 0으로 나누는 행동은 런타임 예외로 처리하지 않고 Infinity값을 반환합니다. 논리적으로, TypeScript는 JavaScript 코드의 런타임 특성을 절대 변화시키지 않습니다.

즉 TypeScript가 코드에 타입 오류가 있음을 검출해도, JavaScript 코드를 TypeScript로 이동시키는 것은 같은 방식으로 실행시킬 것을 보장합니다

JavaScript와 동일한 런타임 동작을 유지하는 것은 프로그램 작동을 중단시킬 수 있는 미묘한 차이를 걱정하지 않고 두 언어 간에 쉽게 전환할 수 있도록 하기 위한 TypeScript의 기본적인 약속입니다.


#### 삭제된 타입 (Erased Types)
개략적으로, TypeScript의 컴파일러가 코드 검사를 마치면 타입을 삭제해서 결과적으로 "컴파일된" 코드를 만듭니다. 즉 코드가 한 번 컴파일되면, 결과로 나온 일반 JS 코드에는 타입 정보가 없습니다.

타입 정보가 없는 것은 TypeScript가 추론한 타입에 따라 프로그램의 특성을 변화시키지 않는다는 의미입니다. 결론적으로 컴파일 도중에는 타입 오류가 표출될 수 있지만, 타입 시스템 자체는 프로그램이 실행될 때 작동하는 방식과 관련이 없습니다.

마지막으로, TypeScript는 추가 런타임 라이브러리를 제공하지 않습니다. TypeScript는 프로그램은 JavaScript 프로그램과 같은 표준 라이브러리 (또는 외부 라이브러리)를 사용하므로, TypeScript 관련 프레임워크를 추가로 공부할 필요가 없습니다.