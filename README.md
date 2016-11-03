# react-real-math
Do math with a DSL as easy as React.js!

```javascript
import { computeValue, Add, Multiply, Subtract, One, Two, Four, Five } from 'react-real-math'

console.log("The answer to everything:", computeValue(
  <Add>
    <Two/>
    <Multiply by={<Four/>}>
      <Subtract by={<One/>}>
        <Add>
          <Five/>
          <Four/>
          <One/>
          <One/>
        </Add>
      </Subtract>
    </Multiply>
  </Add>
))
```
