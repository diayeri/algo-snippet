# 배열

## 순서 거꾸로 뒤집기

### for 반복문

```js
const arr = ["Apple", "Banana", "Orange"];

// 배열 거꾸로
const reverse = [];
for (let i = arr.length - 1; i >= 0; i--) {
  reverse.push(arr[i]);
}

// 결과 출력
console.log("arr : " + arr);
console.log("reverse : " + reverse);
```

### reverse() 메서드

```js
const arr = ["Apple", "Banana", "Orange"];

// 배열 거꾸로
const reverse = arr.reverse();

// 결과 출력
console.log("arr : " + arr);
console.log("reverse : " + reverse);
```

### reverse() + 전개구문 => 원본배열 유지

```js
const arr = ["Apple", "Banana", "Orange"];

// 배열 거꾸로
const reverse = [...arr].reverse();

// 결과 출력
console.log("arr : " + arr);
console.log("reverse : " + reverse);
```
