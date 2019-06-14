# swagger-typescript-node-template

A template for swagger-codegen-cli that produces typescript that pass `@typescript-eslint` (the defaults for React)

### Usage

swagger-codegen-cli allows you to specify your own template with `-t`.

After downloading this template folder, pass it as an argument to the cli.

```
java -jar swagger-codegen-cli.jar generate -i some_api.yaml -l typescript-node -o some/output/folder --additional-properties supportsES6=true -t ./swagger-typescript-node-template/
```

### Fixes

- Change import statements to `import name from 'package'`
- Change type casts from `<type>Object` to `Object as <type>`
- Remove unneeded string concatenations in the template file
- Updated equality tests to use `===` when needed
