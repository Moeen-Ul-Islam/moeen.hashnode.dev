# Styling Components With StyleSheet-React Native

## How does styling work in React Native?

Styling in React Native is done using JavaScript. Since React components have support for the `style` prop, you can also create an object of style values and pass them on to the component as *props*. The style names work exactly the same way as in CSS, except that they’re written in camel-case (e.g., `backgroundColor`).

```javascript
import React from "react";
import {
    View,
    Text,
    StyleSheet,
    useColorScheme
} from 'react-native'

function AppPro():JSX.Element{
    const isDarkMode = useColorScheme() === 'dark'
    return(
        <View style={{flex: 1, backgroundColor: "#ffffff" }}>
            View
            <Text style={{fontSize: 26, color: "#000"}}>
                Hello World!
            </Text>
        </View>
    )
}
```

Styling a *React Native* application highly depends upon the complexity of your application. As it grows more complex, it is recommended that you use `StyleSheet.create` to define multiple styles for your application. e.g.,

```javascript
import React from "react";
import {
    View,
    Text,
    StyleSheet,
    useColorScheme
} from 'react-native'

function AppPro():JSX.Element{
    const isDarkMode = useColorScheme() === 'dark'
    return(
        <View style={styles.container}>
            <Text style={isDarkMode ? styles.whiteText: styles.darkText}>
                Hello World!
            </Text>
        </View>
    )
}
//styles
const styles = StyleSheet.create({
    container: {
        flex: 1,
        alignItems: 'center'
    },
    whiteText: {
        color: '#FFFFFF'
    },
    darkText: {
        color: '#000000'
    }
})
```

> The more complex your application, the more you should break down your styles into smaller pieces of reusable codes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675630470667/bd61fd53-36e1-4123-a4c0-0a6b905e05b9.jpeg align="center")

## Some methods provided by `StyleSheet`

### `create` :

Creates a new style object from a set of styles.

```javascript
static create(styles: Object): Object;
```

### `flatten`:

Flattens an array of style objects into a single style object.

```javascript
import React from 'react';
import {StyleSheet, Text, View} from 'react-native';

const App = () => (
  <View style={page.container}>
    <Text style={flattenStyle}>React Native</Text>
    <Text>Flatten Style</Text>
    <Text style={page.code}>{JSON.stringify(flattenStyle, null, 2)}</Text>
  </View>
);

const page = StyleSheet.create({
  container: {
    flex: 1,
    padding: 24,
    alignItems: 'center',
  },
  text: {
    color: '#000',
    fontSize: 14,
    fontWeight: 'bold',
  },
  code: {
    marginTop: 12,
    padding: 12,
    borderRadius: 8,
    color: '#666',
    backgroundColor: '#eaeaea',
  },
});

const typography = StyleSheet.create({
  header: {
    color: '#61dafb',
    fontSize: 30,
    marginBottom: 36,
  },
});

const flattenStyle = StyleSheet.flatten([page.text, typography.header]);

export default App;
```

*OUTPUT:*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675631610814/9af59c55-65ce-42f7-a7cd-810be78b085a.png align="center")

### `hairlineWidth`:

Returns the hairline width of the device, which can be used to create thin lines or borders.

```javascript
import React from 'react';
import {StyleSheet, Text, View} from 'react-native';

const App = () => (
  <View style={styles.container}>
    <Text style={styles.row}>React</Text>
    <Text style={styles.row}>Native</Text>
  </View>
);

const styles = StyleSheet.create({
  container: {
    flex: 1,
    padding: 24,
  },
  row: {
    padding: 4,
    borderBottomColor: 'red',
    borderBottomWidth: StyleSheet.hairlineWidth,
  },
});

export default App;
```

*OUTPUT:*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675631564763/d91600d1-6b5e-455d-a54b-ddbf87c0d844.png align="center")

### `absoluteFill` :

Returns a style object that can be used to fill an entire component.

```javascript
const App = () => (
  <View style={styles.container}>
    <View style={styles.box1}>
      <Text style={styles.text}>1</Text>
    </View>
    <View style={styles.box2}>
      <Text style={styles.text}>2</Text>
    </View>
    <View style={styles.box3}>
      <Text style={styles.text}>3</Text>
    </View>
  </View>
);

const styles = StyleSheet.create({
  container: {
    flex: 1,
  },
  box1: {
    position: 'absolute',
    top: 40,
    left: 40,
    width: 100,
    height: 100,
    backgroundColor: 'red',
  },
  box2: {
    ...StyleSheet.absoluteFillObject,
    top: 120,
    left: 50,
    width: 100,
    height: 100,
    backgroundColor: 'blue',
  },
  box3: {
    ...StyleSheet.absoluteFillObject,
    top: 120,
    left: 120,
    width: 100,
    height: 100,
    backgroundColor: 'green',
  },
  text: {
    color: '#FFF',
    fontSize: 80,
  },
});

export default App;
```

*OUTPUT:*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1675631471142/aea85a22-1d1e-481c-b913-9307dc012da3.png align="center")

### `compose`:

Composes multiple style objects into a single style object.

## **Conclusion**

Whether you’re looking to build a relatively basic or complex mobile app, styling in React Native is as simple as writing CSS for a web application. You can read more about available react-native props in the [React Native docs](https://reactnative.dev/docs/view-style-props#!).

---

Thank you! for reading, please leave your comments if any ✌️

Connect with the author:

[LinkedIn](https://www.linkedin.com/in/moeenulislam/)

[Twitter](https://twitter.com/moeenulislam_)