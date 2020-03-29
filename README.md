# Products
Me learning GraphQL, inspired by a [great tutorial](https://dev.to/dotnet/how-you-can-build-a-web-api-using-graphql-net-core-and-entity-framework-1ago)

## Prerequisites
* A running Sql Server on "localhost"
    * The following sql user must be permissioned for the service operations:
        * username: user1
        * password: Password1!


## Running
```bash
cd Products.SI
dotnet run
```

## Examples
GraphQL query for sellers with their items:
```graphql
query {
  sellers {
    name,
    items {
     description 
    }
  }
}
```
GraphQL mutation for new seller which retrieves only his id:
```graphql
mutation {
  addSeller(name: "New boy") {
    id
  }
}

```

## Future plans
* Write a Dockerfile for the service
* Write a docker-compose.yml file which start the service alongside with an sql server (don't forget to change the connection string)
* Write unit tests
* Write integration tests
