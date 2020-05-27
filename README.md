[![npm version](https://img.shields.io/npm/v/places-autocomplete.svg?style=flat)](https://www.npmjs.com/package/places-autocomplete) [![Bundlephobia](https://badgen.net/bundlephobia/minzip/places-autocomplete)](https://bundlephobia.com/result?p=places-autocomplete)

## Places Autocomplete

A custromized UI for Google Maps Places Autocomplete.

### Browser document object is requered.

### Sample
<img src="https://raw.githubusercontent.com/rgbutov/places-autocomplete/master/sample/sample.png" height="200">

### Installation
#### Node
```bash
npm i -s places-autocomplete
```
#### Script tag
```html
<script src="/path/to/places-autocomplete.min.js"></script>
```

### Usage
```js
// _init module, you need API_TOKEN from google console
const paInput = new placesAutocomplete('<API_TOKEN>');
const placeConfig = {
  // _specify country for autocomplete
  countryCode: 'us',
  // _type of autocomplition: (cities), (regions): https://developers.google.com/maps/documentation/javascript/places-autocomplete
  autocompleteType: ['(cities)'],
  // _use only place name
  onlyName: true,
  // _inputs list with additional filter places like city, state, country
  filterInputs: []
} 
// _after dropdown selected callback
const afterPlaceSelected = (place_id, place_name) => {
  console.log(place_id, place_name);
}

const placeInput = document.getElementById('dcity');
// bind input with autocompletetion to input
paInput.bindInput({
    input: placeInput, 
    config: placeConfig,
    afterSelected: afterPlaceSelected
});
```

### License
Places Autocomplete is MIT licensed.