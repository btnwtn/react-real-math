# react-real-math
Do math with a DSL as easy as React.js!

## Install

```
$ yarn add react-real-math
```

## Example

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

For some uses (big production apps), you'll want to use numbers greater
than nine, `react-real-math` provides a useful helper to cover this case.

```javascript
import { Zero, Two, Four, Concat, Add } from './react-real-math';

const forty = (
  <Concat>
    <Four />
    <Zero />
  </Concat>
)

console.log("The answer to everything:", computeValue(
  <Add>
    {forty}
    <Two />
  </Add>
))
```
