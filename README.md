# Get Started

Starting point https://www.apollographql.com/docs/apollo-server/v1/example/

## Run server
node version `v10.15.3`

1. install server dependencies `npm install`
2. run server locally `node index.js`

## Generate client schema
make sure local server is running

1. download [apollo-cli](https://www.npmjs.com/package/apollo) `npm install -g apollo` 
3. generate client schema `apollo schema:download --endpoint=http://localhost:3000/graphql` 

# Notes

Failed to generate client schema when using `Long` type, changed `Long` to `Int` resolved the issue.
```
/Users/mac/github/ostelco-nodejs-graphql-example/node_modules/graphql/validation/validate.js:89
    throw new Error(errors.map(function (error) {
    ^

Error: Unknown type "Long".

Unknown type "Long".
    at assertValidSDL (/Users/mac/github/ostelco-nodejs-graphql-example/node_modules/graphql/validation/validate.js:89:11)
    at Object.buildASTSchema (/Users/mac/github/ostelco-nodejs-graphql-example/node_modules/graphql/utilities/buildASTSchema.js:78:34)
    at Object.buildSchemaFromTypeDefinitions (/Users/mac/github/ostelco-nodejs-graphql-example/node_modules/graphql-tools/dist/generate/buildSchemaFromTypeDefinitions.js:23:28)
    at makeExecutableSchema (/Users/mac/github/ostelco-nodejs-graphql-example/node_modules/graphql-tools/dist/makeExecutableSchema.js:26:29)
    at Object.<anonymous> (/Users/mac/github/ostelco-nodejs-graphql-example/index.js:26:16)
    at Module._compile (internal/modules/cjs/loader.js:701:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:712:10)
    at Module.load (internal/modules/cjs/loader.js:600:32)
    at tryModuleLoad (internal/modules/cjs/loader.js:539:12)
    at Function.Module._load (internal/modules/cjs/loader.js:531:3)
```
