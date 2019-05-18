# Schema to Validator

Build a Validator from a schema such as a JSON schema or GraphQL schema (type definition)

## Install

- npm: `npm install schema-to-validator -S`
- yarn: `yarn add schema-to-validator`

## Quickstart

```ts
import { buildValidator } from "@schema-validator/api";
import { builder as yupBuilder, types as yupTypes } from "@schema-validator/yup-builder";

const onComplete = (result ) => console.log('DONE', result)
const onError = (err) => console.error('ERROR', err)

const config = {
  validator: {
    name: "my-yup-validator",
    type: "yup"
  },
  schema: {
    type: "json"
  },
  builders: {
    yup: {
      builder: yupBuilder
      types: yupTypes
    }
  },
  // logging: true
  events: {
    onComplete,
    onError
  }
};

const schema = {
  // json schema
};

const obj = {
  name: "mike"
};

const validator = buildValidator({
  schema,
  config
});

const valid = validator.validateSync(obj);
```

### Yup example

### JSON Schema

### GraphQL Schema

### Forg example

## Advanced

## Development

## Test

## License
