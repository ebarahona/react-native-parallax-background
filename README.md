# react-native-parallax-background

## Installation

```
npm install --save react-native-parallax-background
```

## Demo

![Demo](./demo.gif)

## `ParallaxBackground` Properties
#
| Prop | Description |
|---|---|
|**`uri`**|string of image url |
|**`maxHeight`**|height of the image background. |

```js
import {ParallaxBackground} from 'react-native-parallax-background';

export default class App extends React.Component {
  render() {
    return (
      <View style={styles.container}>
        <ParallaxBackground
          maxHeight={300}
          uri={'http://cdn.eventfinda.co.nz/uploads/events/transformed/1050208-474117-7.png?v=2'}
          >
          <View>
            <Text> content </Text>  
          </View>  
        </ParallaxBackground>
      </View>
    );
  }
}
```

## `HorizontalWrapper` Properties
*Note: `ParallaxBackground` elements must be direct descendants of `HorizontalWrapper`*

| Prop | Description | Defaul|
|---|---|---|
|**`offset`**|index of the children ParallaxBackground component should be showed.|0|

```js
import {HorizontalWrapper, ParallaxBackground} from 'react-native-parallax-background';

export default class App extends React.Component {
  render() {
    return (
      <View style={styles.container}>
        <HorizontalWrapper
        offset={1}>
          <ParallaxBackground
            maxHeight={300}
            uri={'http://cdn.eventfinda.co.nz/uploads/events/transformed/1050208-474117-7.png?v=2'}>
            <View><Text> Content 1</Text> </View>  
          </ParallaxBackground>
          <ParallaxBackground
            maxHeight={300}
            uri={'http://cdn.eventfinda.co.nz/uploads/events/transformed/1040425-469847-7.jpg'}>
            <View><Text> Content 2</Text> </View>  
          </ParallaxBackground>
          <ParallaxBackground
            maxHeight={300}
            uri={'http://cdn.eventfinda.co.nz/uploads/events/transformed/975524-440514-7.jpg'}>
            <View><Text> Content 3</Text> </View>  
          </ParallaxBackground>
        </HorizontalWrapper>
      </View>
    );
  }
}
```

## License

[MIT License](http://opensource.org/licenses/mit-license.html).