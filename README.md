---
description: Function
---

# curry

> (\* -> a) -> (\* -> a)

제공된 함수에 해당하는 커리(혹은 커링)를 반환합니다. 커리 함수는 2가지 특이한 기능을 갖습니다. 첫째, 인수를 한번에 하나만 제공할 필요가 없습니다. 만일 `f` 가 삼항 함수라면 `g`는 `R.curry(f)` 일때 아래는 모 같습니다.

```
g(1)(2)(3)
g(1)(2, 3)
g(1, 2)(3)
g(1, 2, 3)
```

둘째, 특별 Placeholder 값인 `R._` 를 사용하여 간격을 지정할 수 있어 위치와 관계없이 인수 형태 부분적으로 사용할 수 있습니다. `g` 가 위와 같고 \_를 `R._` 라고 할 때 아래는 모두 동일합니다.

```
g(1, 2, 3)
g(_, 2, 3)(1)
g(_, _, 3)(1)(2)
g(_, _, 3)(1, 2)
g(_, 2)(1)(3)
g(_, 2)(1, 3)
g(_, 2)(_, 3)(1)
```

```
const addFourNumbers = (a, b, c, d) => a + b + c + d;

const curriedAddFourNumbers = R.curry(addFourNumbers);
const f = curriedAddFourNumbers(1, 2);
const g = f(3);
g(4); //=> 10
```
