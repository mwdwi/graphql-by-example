# What is GraphQL
GraphQL is a query language and a server-side runtime (typically served over HTTP)

## GraphQL is a query language
GraphQL is a language for querying data. Unlike most query languages (such as SQL), you don’t use GraphQL to query a particular type of data store (such as a MySQL database). Instead, you use GraphQL to query data from any number of different sources.

The structured way in which we make requests presents two types of operations: queries and mutations.

![gql](https://user-images.githubusercontent.com/85268031/155038062-3ef746ad-c872-4c1b-a830-7e3947a4360d.png)

Queries that fetch data are synonymous to GET calls in REST, while mutations signal that we’d like to invoke a change the in system, similar to REST’s POST or DELETE methods.

## Runtime
The runtime part points to the fact that a GraphQL API runs on a server.

In a GraphQL API, we shape our data within a strictly typed schema, telling it how to resolve data when asked for. To GraphQL, where data comes from doesn’t matter. It could be from a database, micro-service, or even an underlying RESTful API.

GraphQL is data source agnostic.

![gql2](https://user-images.githubusercontent.com/85268031/155049912-361cd5af-9d5a-45ee-9e1f-8e4f4e4fa8bb.png)


## Served over HTTP
GraphQL is typically served over HTTP. This means operations are just plain ol’ strings, and we don’t need a special tool to query data from a GraphQL server.

## How does it work?
### Design your GraphQL schema
On the server, we create a GraphQL schema based on the data we need to build our app UIs. If we were building a job board, it’s here that we’d model out the Job, Company, and Location types.

### Connect your resolvers to data sources
For each type, we write the resolver functions, connecting the data to our graph. Perhaps we get the Job data from an external API. And maybe we get the Location data from the Google Maps API.

![gql3](https://user-images.githubusercontent.com/85268031/155049929-fdaa9436-1e32-4cbc-94b4-a5f465ab234e.png)

