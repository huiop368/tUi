---
order: 0
title: 基本
---

滑动开关

```jsx
import Switch from 'lib/switch'
import 'lib/switch/style'

class SwitchExample extends React.Component {
  constructor (props){
    super(props)
    this.state = {
        checked : false    
    }

    this.onChange = this.onChange.bind(this)
  }

  onChange(checked) {
      this.setState({checked : !this.state.checked})
  }

  render() {
    return (
        <div>
            <Switch checked={this.state.checked} onChange={this.onChange} />
        </div>  
    )
  }
}

ReactDOM.render(<SwitchExample />, mountNode);
```
