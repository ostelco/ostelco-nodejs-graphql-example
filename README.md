# Get Started

Starting point https://www.apollographql.com/docs/apollo-server/v1/example/

## Run server
1. install server dependencies `npm install`
2. run server locally `node index.js`

## Generate client schema
make sure local server is running

1. download [apollo-cli](https://www.npmjs.com/package/apollo) `npm install -g apollo` 
3. generate client schema `apollo schema:download --endpoint=http://localhost:3000/graphql` 
