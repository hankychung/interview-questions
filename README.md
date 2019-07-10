# interview-questions

#### 修改以下 print 函数，使之输出 0 到 99，或者 99 到 0

要求：

1、只能修改 setTimeout 到 Math.floor(Math.random() * 1000 的代码

2、不能修改 Math.floor(Math.random() * 1000

3、不能使用全局变量

```
function print(n){
  setTimeout(() => {
    console.log(n);
  }, Math.floor(Math.random() * 1000));
}
for(var i = 0; i < 100; i++){
  print(i);
}
```

解答：

1、使用已有的全局变量i
```
function print(n){
  setTimeout(() => {
    console.log(i--);
  }, Math.floor(Math.random() * 1000));
}
for(var i = 0; i < 100; i++){
  print(i);
}
```

2、立即执行函数
```
function print(n){
  setTimeout((() => {
    console.log(n);
  })(), Math.floor(Math.random() * 1000));
}
for(var i = 0; i < 100; i++){
  print(i);
}
```
