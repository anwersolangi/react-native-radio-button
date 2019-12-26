# React Native Radio Button

React Native Radio Button is a Simple Custom Made Component Which Can Be Used In Any React Native project and without requiring any third party Library. React native Radio button is made with React native APIs. It is a mockup of Radio Button.


## Getting Started

Installing this Component is really easy as git clone and paste. There is No Need to download any third party API. Its simple as Download, Upload and Import.

### Installing

Follow These Simple Steps to Import and Make Radio Button In React Native.

```diff
+   Download RadioButton.js and Paste it in Your Project
```

Second Step

```js
import RadioButton.js in Component, make two State: checked and key(Where Data Stored).
```
See Below Example To Understand it Better

## Using Radio Button In Component

Use RadioButton in component like below Example

```jsx
import React, {useState} from 'react';
import RadioButton from '../src/Components/RadioButton';
import {View, Text, StyleSheet , } from 'react-native';


const FilterScreen = props => {
 
  const [gender, setGender] = useState('male');
  const [femaleCheck, setFemaleCheck] = useState(false);
  const [maleCheck, setMaleCheck] = useState(true);

  const maleRadioHandler = () => {
    if(femaleCheck){
      setFemaleCheck(false);
      setMaleCheck(true);
      setGender('male');
    } else {
      setMaleCheck(true);
      setGender('male');
    }
  }


  const femaleRadioHandler = () => {
    if(maleCheck){
      setMaleCheck(false);
      setFemaleCheck(true);
      setGender('female');
    } else {
      setFemaleCheck(true);
      setGender('female');
    }
  }

  const onPressHandler = async() => {
    console.log(gender);
  }

    return (
      <View style={styles.container}>
        <View style={{...styles.blockContainer, alignItems: 'center', flexDirection: 'row', marginHorizontal: 15, paddingHorizontal: 10}}>
        <View style={styles.headingContainer}><Text style={styles.headingText}>Gender:</Text></View>
        <Text style={styles.radioText}>Male: </Text>
       <RadioButton  onPress={maleRadioHandler} checked={maleCheck} />
       <Text style={styles.radioText}>Female: </Text>
       <RadioButton checked={femaleCheck} onPress={femaleRadioHandler} />
        </View>
      <Button title="Done" onTouch={onPressHandler} />
      </View>
    )
}


const styles = StyleSheet.create({
  container: {

    flex: 1,
    backgroundColor: '#f6f8fa'
  },
  blockContainer: {
    backgroundColor: '#fff',
    width: '97%',
    marginLeft: 6,
    elevation: 3,
    borderRadius: 10,
    marginVertical: 5,
    marginHorizontal: 5,
    paddingVertical: 10,
    paddingHorizontal: 5
  },
  headingText: {
    fontSize: 19,
    fontWeight: '400'
  },
  textContainer: {
    flexDirection: 'row',
    justifyContent: 'space-between',
    marginLeft: 10
  },
  headingContainer: {
    justifyContent: 'center',
    alignItems: 'center',
  },
  text: {
    fontSize: 18,
    
  },
  radioText: {
    marginHorizontal: 5,
    fontSize: 15
  },
  
})

export default FilterScreen;
```

## Built With

* [TouchableOpacity](https://facebook.github.io/react-native/docs/touchableopacity) - React Native Component
* [View](https://facebook.github.io/react-native/docs/view) - React Native Component
* [StyleSheet](https://facebook.github.io/react-native/docs/stylesheet) - React Native API

These are the only Components and APIs used To make this Component


## Authors

* **Anwer Solangi** - *Initial work* - [Anwer Solangi](https://github.com/anwersolangi)
