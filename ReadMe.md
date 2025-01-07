# react-native-phonefield

`react-native-phonefield` is a React Native component for a customizable phone number input with country code selection and validation.

## Description

`react-native-phonefield` provides an intuitive and user-friendly way to input and validate phone numbers in React Native applications. It supports automatic country code detection, customizable styles, and additional features to ensure seamless integration into your project.

## Installation

You can install `react-native-phonefield` using either npm or yarn:

### Using npm:

```bash
npm install react-native-phonefield
```

### Using yarn:

```bash
yarn add react-native-phonefield
```

## Usage

Here's an example of how to use the `RNPhoneInput` component:

```javascript
import React from 'react';
import { View } from 'react-native';
import RNPhoneInput from 'react-native-phonefield';

const MyComponent = () => {
  return (
    <View>
      <RNPhoneInput
        placeholder="Enter your phone number"
        onChangeText={(value) => console.log(value)}
        onSelectCountryCode={(value) => console.log(value)}
      />
    </View>
  );
};

export default MyComponent;
```

## Props

### `RNPhoneInputProps`

| Prop                 | Type                                          | Description                                                  |
|----------------------|-----------------------------------------------|--------------------------------------------------------------|
| `onChangeText`       | `(value: string) => void`                    | Callback triggered when the text input value changes.        |
| `defaultCountry`     | `CountryCode`                                | The default country code for the phone input.               |
| `defaultValue`       | `string`                                     | The initial value displayed in the text input field.         |
| `containerStyle`     | `StyleProp<ViewStyle>`                       | Custom style for the container of the phone input component. |
| `placeholder`        | `string`                                     | Placeholder text displayed when the text input is empty.     |
| `inputProps`         | `TextInputProps`                             | Additional props passed to the underlying TextInput component.|
| `textInputStyle`     | `StyleProp<TextStyle>`                       | Custom style for the text input field.                      |
| `onSelectCountryCode`| `(value: Omit<EachCountry, 'countryCode', 'callingCode'>) => void` | Callback triggered when a country code is selected. |
| `downArrowIcon`      | `React.ReactNode`                            | Custom React element or icon rendered as the dropdown arrow. |
| `placeholderColor`   | `ColorValue`                                 | Custom color for the placeholder text.                      |
| `iconContainerStyle` | `StyleProp<ViewStyle>`                       | Custom style for the container of the dropdown arrow icon.  |
| `codeTextStyle`      | `StyleProp<TextStyle>`                       | Custom style for the text displaying the country code.      |

## `RNPhoneInputRef`

### Methods

| Method            | Type                            | Description                                      |
|-------------------|---------------------------------|------------------------------------------------|
| `isValidNumber`   | `(value: string) => boolean`   | Validates if the given phone number is valid.  |
| `onChangeText`    | `(value: string) => void`      | Updates the text value of the input.           |
| `defaultCountry`  | `(code: CountryCode) => void`  | Sets the default country code.                 |
| `defaultValue`    | `(text: string) => void`       | Sets the default text value for the input.     |

## License

MIT
