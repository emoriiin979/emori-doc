# TypeScriptチートシート

## 型一覧

| 型 | 説明 | 例 | 備考 |
|--|--|--|--|
|`any`|何でも可|-||
|`void`||-||
|`null`||null||
|`undefined`||undefined||
|`never`||-||
|`boolean`|真偽値|true, false||
|`number`|数値|123, 12.3||
|`string`|文字列|"abcd"||
|`T[]`, `Array<T>`|配列|[1, 2]|`number[]` のように指定する。|
|`[T1, T2]`|複数の型|[123, "abcd"]|`[number, string]` のように指定する。|

## 型判定

### typeof

```
const a = "aaaa"
console.log(typeof a === "string")  // true
console.log(typeof a === "number")  // false
```

### "property" in object

```
const a = {p: "v"}
console.log("p" in a)  // true
console.log("q" in a)  // false
```

### instanceof

```
const a = [1, 2]
console.log(a instanceof Array)  // true
```

### type-guard functions

```
const a = [1, 2]
console.log(Array.isArray(a))  // true
```

```
const a = "aaaa"
const aLength = (typeof a === "string" && a.length)
