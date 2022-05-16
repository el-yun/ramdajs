---
description: Object
---

# assoc

> Idx -> a -> {k: v} -> {k: v}
>
> Idx = String | Int

Object를 얕은 복사로 만들고 주어진 값으로 지정된 속성을 설정하거나 재정의 합니다. 이렇게 하면 Prototype 속성도 새 개체에 복사되어 합쳐집니. 원시값이 아닌 모든 속성은 참조로 복사됩니다.

```
R.assoc('c', 3, {a: 1, b: 2}); //=> {a: 1, b: 2, c: 3}
```
