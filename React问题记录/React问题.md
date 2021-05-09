# React问题

## 关于在方法中修改了state中的值，可以在页面中显示更新后的数据，但是无法直接打印的问题
> 直接在setState({数据更新}, 回调函数)，因为设置方法是异步的

```js
import React from "react";
class ContUpdate extends React.Components {
  state: {
    count: 0
  }

  handleAdd() {
    this.setState({
      count: this.state.count +1
      // 使用回调函数
    }, () => console.log(this.state.count)}) // 1
    console.log(this.state.count)// 0
  }
  render() {
    return (
      <div>
        <p>数据：{this.state.count}</p>
        <button onClick={this.handleAnd}>按钮</button>
      </div>
    )
  }
}
```
