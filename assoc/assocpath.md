---
description: Object
---

# assocPath

> \[Idx] → a → {a} → {a}
>
> Idx = String | Int | Symbol

Object를 얕은 복사로 만들고 주어진 경로를 만드는 데 필요한 노드를 설정하거나 재정의하고 해당 경로의 끝 부분에 특정 값을 배치합니다. 이렇게 하면 Prototype 속성도 새 개체에 복사되어 합쳐집니. 원시값이 아닌 모든 속성은 참조로 복사됩니다.

```
R.assocPath(['a', 'b', 'c'], 42, {a: {b: {c: 0}}}); //=> {a: {b: {c: 42}}}

// Any missing or non-object keys in path will be overridden
R.assocPath(['a', 'b', 'c'], 42, {a: 5}); //=> {a: {b: {c: 42}}}
```
