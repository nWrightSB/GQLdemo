# GQLdemo

Smartbear demo GraphQL server

* Server returns link info that has been submitted by users, documentation is accessible in the IDE - uses simple MongoDB to store links. No AUTH layer implemented.

# install
- clone repo
- ensure NPM is installed and up to date, as well as MongoDB running
- cd into repo
- `npm install`
- `node ./src/index.js`

# usage
 - IDE: [ip]/graphiql
- Once server is running, currently there are two actions it performs, create and read
- Get all links:
`
{
  allLinks {
    id
    url
    description
  }
}
`
- Add new link:
`
mutation {
  createLink(
    url: "[url value]",
    description: "[description string]",
  ) {
    id
    url
    description
  }
}
`
