# React Native Country Code Picker

## ![npm](https://img.shields.io/npm/v/@digieggs/rn-country-code-picker?color=%23CC3534&style=for-the-badge) ![NPM](https://img.shields.io/npm/l/@digieggs/rn-country-code-picker?style=for-the-badge) ![npm](https://img.shields.io/npm/dw/@digieggs/rn-country-code-picker?style=for-the-badge)

A searchable dropdown component to select a country code for your phone number input.

<img src="https://github.com/DIGIEGGS/rn-country-code-picker/blob/main/screenshot/picker.gif?raw=true" width="300">

## For Managed Workflow users using Expo

This component is not supported in the managed workflow for expo for the time being.

## Getting started

`npm install @digieggs/rn-country-code-picker --save`

or

`yarn add @digieggs/rn-country-code-picker`

Also you need to manually install `react-native-svg` library for the icons in the component

`npm install react-native-svg --save`

or

`yarn add react-native-svg`

### For react-native@0.60.0 or above

As [react-native@0.60.0](https://reactnative.dev/blog/2019/07/03/version-60) or above supports autolinking, so there is no need to run linking process.
Read more about autolinking [here](https://github.com/react-native-picker/cli/blob/master/docs/autolinking.md).

#### iOS

CocoaPods on iOS needs this extra step

```
npx pod-install
```

#### Android

No additional step is required.

## Usage

First of all, import the component.

```javascript
import { CallingCodePicker } from 'rn-country-code-picker';
```

Then use it like this.

```javascript
const [selectedCountry, setSelectedCountry] = useState<ICountry>({
    callingCode: '90',
    name: 'Turkey',
    flag: '',
  }); // Give the default values to show an initial country

return (
  CallingCodePicker
    {...{ selectedCountry }}
    onCountrySelect={country => setSelectedCountry(country)}
  />
);
```

## Props

- [`selectedCountry`](#selectedCountry)
- [`onCountrySelect`](#onCountrySelect)
- [`togglerContainerStyle`](#containerStyle)
- [`togglerContainerStyle`](#pickerTogglerLabelStyle)
- [`listContainerStyle`](#listContainerStyle)
- [`searchInputStyle`](#searchInputStyle)
- [`listStyle`](#listStyle)
- [`pickerItemLabelStyle`](#pickerItemLabelStyle)

---

# Reference

## Props

### `selectedCountry`

An object containing the selected country info.

| Type     | Required |
| -------- | -------- |
| ICountry | Yes      |

---

### `onCountrySelect`

Callback for when an item is selected. This is called with the following parameters:

- `country`: an object containing the selected country info

| Type     | Required |
| -------- | -------- |
| function | Yes      |

---

### `togglerContainerStyle`

Style to apply to the toggler container container. (for ex. you can give absolute positioning to align it inside the input.)

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `togglerLabelStyle`

Style to apply to the picker toggler label.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `listContainerStyle`

Style to apply to the list container.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `searchInputStyle`

Style to apply to the search input.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `listStyle`

Style to apply to the FlatList component.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

### `pickerItemLabelStyle`

Style to apply to each of the item labels.

| Type      | Required |
| --------- | -------- |
| StyleProp | No       |

---

## Credits

- https://www.countryflags.io/ (for the flags)
- https://restcountries.eu/ (fetched the info in the countries.json from this api)
