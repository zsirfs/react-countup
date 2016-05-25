# React CountUp

A React component wrapper around [CountUp.js](https://inorganik.github.io/countUp.js/).
This component counts up a number in an animated way.


## Installation
Make sure you have a compatible version of `React 0.14.x` and `15.x.x` installed in your project.
```bash
npm install react-countup --save-dev
```

## Usage
#### Basic
```js
import React from 'react';
import { render } from 'react-dom';
import CountUp from 'react-countup';

render(
  <CountUp start={0} end={160526} />,
  document.getElementById('root')
);
```
#### Advanced
```js
import React from 'react';
import { render } from 'react-dom';
import CountUp from 'react-countup';

const onComplete = () => {
  // Do something on completion
};

render(
  <CountUp
    start={160527.0127}
    end={-875}
    duration={2.75}
    useEasing={true}
    separator=" "
    decimal=","
    prefix="EUR "
    suffix=" left"
    callback={onComplete}
  />,
  document.getElementById('root')
);
```

### Attributes

##### `start` *{number}*
The start number from which the should start from

##### `end` *{number}*
Target number to count up

##### `duration` *{number}*
Duration of count up animation

##### `useEasing` *{boolean}*
use "easeOutExpo" if `true`

##### `useGrouping` *{boolean}*
group thousands by separator character

##### `separator` *{string}*
Specifies character of thousands separator

##### `decimal` *{string}*
Specifies decimal character

##### `prefix` *{string}*
Static text before the animating value

##### `suffix` *{string}*
Static text after the animating value

##### `callback` *{function}*
Callback function to be triggered after completed count up
 animation

## License
MIT