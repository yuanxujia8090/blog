# JS 书写技巧整理

### 去重技巧
    

```javascript
// 简单值类型
const array = [1, 1, 2, 3, 5, 5, 1]

const uniqueArray = [...new Set(array)];
```

### 短路求值
    
```javascript
//  && 返回第一个，当所有值为true时，返回最后一个
let one = 1, two = 2, three = 3;
console.log(one && two && three); // Result: 3
console.log(0 && null); // Result: 0

// || 可以返回第一个，当所有值都是flase时，返回最后一个
let one = 1, two = 2, three = 3;
console.log(one || two || three); // Result: 1
console.log(0 || null); // Result: null
```

### 幂运算

```
console.log(2**3); // 8
// 以下表达式是等效的:
Math.pow(2, n);
2 << (n - 1);
2**n;
例如： 2<<3  等同于  2**4 = 16
```

 ### 类方案上下文绑定
    

```javascript
class App {
  // 该方法中this指向App实例
  helloWorld = () => {
    // do something 
  }
}
```

### 数组截取

1.  直接使用arr.length = n
    
2.  arr.slice(0,n) // 速度更快