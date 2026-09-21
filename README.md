![JSON TO TS](https://image.ibb.co/fTb60k/icon.png)

# Json to TS

### Convert json object to typescript interfaces

> A maintained fork of [MariusAlch/json-to-ts](https://github.com/MariusAlch/json-to-ts),
> which has had no release since April 2024. Published as
> [`@unabandoned/json-to-ts`](https://www.npmjs.com/package/@unabandoned/json-to-ts);
> the API is unchanged from upstream.

# Example

### Code

```javascript
const JsonToTS = require('@unabandoned/json-to-ts')

const json = {
  cats: [
    {name: 'Kittin'},
    {name: 'Mittin'}
  ],
  favoriteNumber: 42,
  favoriteWord: 'Hello'
}

JsonToTS(json).forEach( typeInterface => {
  console.log(typeInterface)
})
```

### Output:

```typescript
interface RootObject {
  cats: Cat[];
  favoriteNumber: number;
  favoriteWord: string;
}
interface Cat {
  name: string;
}
```

## Converter
- Array type merging (**Big deal**)
- Union types
- Duplicate type prevention
- Optional types
- Array types

# Setup

```sh
$ npm install --save @unabandoned/json-to-ts
```
