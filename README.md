# GraphQL and REST API Gateway Example 

This is a fork of the [brunocramos/graphql-example](https://github.com/brunocramos/graphql-example) GraphQL example.  This code contains an example of an [API Gateway](http://microservices.io/patterns/apigateway.html) written in NodeJS.  It was written to demonstrate how to combine both a [GraphQL](http://graphql.org/) API with traditional [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) endpoints.

## Installation

Installation requires that you clone (or otherwise download) the repository.  It relies on [Yarn](https://yarnpkg.com/lang/en/) to install package dependencies, so you may need to [install it](https://yarnpkg.com/en/docs/install) to complete the installation process.  

Generally, the installation steps should be:


```
git clone git@github.com:fireproofsocks/graphql-example.git
cd graphql-example
yarn install
yarn run start
````

You should see the following message:
```
Running GraphQL API server at http://localhost:4000/graphql
```

At which point you can point your browser to your GraphQL endpoint at [http://localhost:4000/graphql] and explore it.


## Example GraphQL Queries

Looking up a user and their name by their `_id`:
```
{
  users(_id:1) {
    _id
    name
  }
}
```

Or omit the `_id` from the results:
```
{
  users(_id:1) {
    name
  }
}
```

You can also list all users:

```
{
  users {
    name
  }
}
```