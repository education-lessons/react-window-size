
# Why the fork?
Using react-window-size directly with Gatsby will result into build errors becuase when building gatsby, window is not available in global space. This fork gracefully handles that.

# React Window Size

A higher-order React component that passes the browser window's dimensions as props to the wrapped component.

Example:

```javascript
import React, { Component } from 'react';
import windowSize from 'react-window-size';

class ScreenSize extends Component {

  render() {
    return (
      <p>
        Screen width is: {this.props.windowWidth}
        <br />
        Screen height is: {this.props.windowHeight}
      </p>
    );
  }

}

export default windowSize(ScreenSize);
```
