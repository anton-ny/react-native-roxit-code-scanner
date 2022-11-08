# react-native-roxit-code-scanner

Broadcast code scanner receiver

## Installation

```sh
npm install react-native-roxit-code-scanner
```

## Usage

```js
import * as ScodeScanner from 'react-native-roxit-code-scanner';
import {DeviceEventEmitter} from "react-native";

// ...

const scode_callback = useCallback(scode => {
	console.log('scode', scode);
}, []);

useEffect(
  () => {
    setTimeout(() => {
      DeviceEventEmitter.addListener('scode', scode_callback);
      return () => DeviceEventEmitter.removeAllListeners('scode');
    }, 100);
  }
);
```

