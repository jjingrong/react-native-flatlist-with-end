# react-native-flatlist-with-end

A simple wrapper over React Native's FlatList to render a component at the end of the list

Works on both iOS and Android

# Installation

- Run `npm i react-native-flatlist-with-end --save`
- `import FlatListWithEnd from 'react-native-flatlist-with-end'`

# Usage

Just sub in `FlatListWithEnd` in place of `FlatList` from react-native.
Optionally, you can add a prop `renderEndComponent`. It expects a function that returns a component.

# Example
```
<FlatListWithEnd
  scrollEnabled
  data={data}
  keyExtractor={(item, index) => index}
  renderItem={({ item }) => {
    return (
      <View>
        <Text>
          {item.text}
        </Text>
      </View>
    );
  }}
  renderEndComponent={() => {
    return (
      <View style={{ paddingVertical: 15 }}>
        <Text style={{ textAlign: 'center' }}>
          End of list
        </Text>
      </View>;
    );
  }}
/>
```

# API


Props              | Type     | Optional | Default     | Description
----------------- | -------- | -------- | ----------- | -----------
renderEndComponent  | Function | true | See [here](https://github.com/jjingrong/react-native-flatlist-with-end/blob/master/README.md#endcomponent)  | Custom function that returns a component to show 


# EndComponent

`DefaultRenderEndComponent` in [index.js](https://github.com/jjingrong/react-native-flatlist-with-end/blob/master/index.js)
```
() => {
  return <View style={{ paddingVertical: 15 }}><Text style={{ textAlign: 'center' }}>End of list</Text></View>;
}
```

# Contributing

Feel free to open issues/PRs. This is implemented as a quick fix as there doesn't seem to be any libraries that implements this, but I realised that some others may find it useful too :)
