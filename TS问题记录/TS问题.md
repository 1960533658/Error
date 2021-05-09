# TS问题

## 如何理解类型兼容中的四种协变
> 协变： 在一个方向上可以赋值
> 逆变： 之子按相反的方向上可以赋值
ps： 方向不是固定的，当你认为谁给谁赋值是正向，那么它就是正向的，相反的方向则为逆向
> 双向协变正向和逆向都可以
> 不变：两个方向都不可以
## 函数重载的打印结果只有3

## 索引类型访问操作符
> 第一行代码泛型使用的格式该怎么理解
```ts
let getValue = <T, K extends keyof T>(obj: T, keys: K[]): T[K][] => {
  let arr = [] as (T[K][])
  keys.forEach(key => {
    arr.push(pbj[key])
  })
  return arr
}

let obj3 = {
  name: "zs"
  age: 12,
  marrired: true
}
getValue(obj3,["name","age","marrired"])
```

## 声明文件不成功